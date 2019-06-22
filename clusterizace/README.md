# Clusterizace

Problematiku clusterizace jsem detailně prezentoval ne SEO Restartu 2019. Veškeré postupy jsem popsal v mém blogpostu: https://www.zatkovic.cz/aks-na-maximum-automatizace/.
Zde jsem se rozhodl uložit vybrané skripty, které jsem v článku popisoval. 

## Zisk nejhledanějšího klíčového slova

**Vstupní data:**

| Keyword | Keyword-bu | Search |
|---------|------------|--------|
| letni saty | letní šaty | 100 |
| letni saty | letní saty | 50  |
| letni saty | letni šaty | 10  |

```JSON
[
  {
    "op": "core/row-reorder",
    "description": "Reorder rows",
    "mode": "row-based",
    "sorting": {
      "criteria": [
        {
          "errorPosition": 1,
          "caseSensitive": false,
          "valueType": "string",
          "column": "Keyword",
          "blankPosition": 2,
          "reverse": false
        }
      ]
    }
  },
  {
    "op": "core/blank-down",
    "description": "Blank down cells in column Keyword",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Keyword"
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Keyword-bu",
    "columnName": "Keyword-bu",
    "keyColumnName": "Keyword",
    "separator": "☼"
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Search",
    "columnName": "Search",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Search using expression value.toString()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Search",
    "expression": "value.toString().replace('.0', '')",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/column-addition",
    "description": "Create column Index at index 3 based on column Search using expression jython:array = value\narray = array.split(',')\n\nx = 0\nmax = 0\nindex = 0\n\nwhile x < len(array):\n array[x] = int(array[x])\n if max < array[x]:\n  max = array[x]\n  index = array.index(max)\n x = x + 1\n\nreturn index",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "newColumnName": "Index",
    "columnInsertIndex": 3,
    "baseColumnName": "Search",
    "expression": "jython:array = value\narray = array.split(',')\n\nx = 0\nmax = 0\nindex = 0\n\nwhile x < len(array):\n array[x] = int(array[x])\n if max < array[x]:\n  max = array[x]\n  index = array.index(max)\n x = x + 1\n\nreturn index",
    "onError": "set-to-blank"
  },
  {
    "op": "core/column-removal",
    "description": "Remove column Keyword",
    "columnName": "Keyword"
  },
  {
    "op": "core/column-addition",
    "description": "Create column Keyword at index 1 based on column Keyword-bu using expression grel:forEach(value.split('☼'),v,v).get(cells['Index'].value)",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "newColumnName": "Keyword",
    "columnInsertIndex": 1,
    "baseColumnName": "Keyword-bu",
    "expression": "grel:forEach(value.split('☼'),v,v).get(cells['Index'].value)",
    "onError": "set-to-blank"
  }
]

```

**Výstupní data:**

| Keyword-bu | Keyword | Search | Index |
|---------|------------|--------|-------|
| letní šaty☼letní saty☼letni šaty | letní šaty | 100, 50, 10 | 0 |

Nyní je dobré provést ruční kontrolu, že se všechna klíčová slova správně napárovala. Věřím, že to pro vás nebude problém, protože by tam neměla být chybka. 😊 Jestliže chcete nyní pročistit výsledný dataset, tak satačí spustit následující skript:

```JSON
[
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Search using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Search",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/column-removal",
    "description": "Remove column Index",
    "columnName": "Index"
  },
  {
    "op": "core/row-removal",
    "description": "Remove rows",
    "engineConfig": {
      "facets": [
        {
          "type": "list",
          "name": "Keyword-bu",
          "expression": "isBlank(value).toString()",
          "columnName": "Keyword-bu",
          "invert": false,
          "selection": [
            {
              "v": {
                "v": "true",
                "l": "true"
              }
            }
          ],
          "selectNumber": false,
          "selectDateTime": false,
          "selectBoolean": false,
          "omitBlank": false,
          "selectBlank": false,
          "omitError": false,
          "selectError": false
        }
      ],
      "mode": "row-based"
    }
  },
  {
    "op": "core/column-reorder",
    "description": "Reorder columns",
    "columnNames": [
      "Keyword",
      "Keyword-bu",
      "Search"
    ]
  }
]
```

**Výstupní data:**

| Keyword | Keyword-bu | Search | 
|---------|------------|--------|
| letni šaty | letní šaty☼letní saty☼letni šaty | 160 |
