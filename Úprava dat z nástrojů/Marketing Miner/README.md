## Úprava dat z nástroje Marketing Miner

### Spojení clustrů pro trendovost a vypočítání průměru

```
[
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Google Search Volume",
    "columnName": "Google Search Volume",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Google CPC",
    "columnName": "Google CPC",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column January",
    "columnName": "January",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column February",
    "columnName": "February",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column March",
    "columnName": "March",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column April",
    "columnName": "April",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column May",
    "columnName": "May",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column June",
    "columnName": "June",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column July",
    "columnName": "July",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column August",
    "columnName": "August",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column September",
    "columnName": "September",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column October",
    "columnName": "October",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column November",
    "columnName": "November",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column December",
    "columnName": "December",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Search Volume",
    "columnName": "Sklik Search Volume",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik CPC",
    "columnName": "Sklik CPC",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - January",
    "columnName": "Sklik Monthly Data - January",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - February",
    "columnName": "Sklik Monthly Data - February",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - March",
    "columnName": "Sklik Monthly Data - March",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - April",
    "columnName": "Sklik Monthly Data - April",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - May",
    "columnName": "Sklik Monthly Data - May",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - June",
    "columnName": "Sklik Monthly Data - June",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - July",
    "columnName": "Sklik Monthly Data - July",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - August",
    "columnName": "Sklik Monthly Data - August",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - September",
    "columnName": "Sklik Monthly Data - September",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - October",
    "columnName": "Sklik Monthly Data - October",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - November",
    "columnName": "Sklik Monthly Data - November",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/multivalued-cell-join",
    "description": "Join multi-valued cells in column Sklik Monthly Data - December",
    "columnName": "Sklik Monthly Data - December",
    "keyColumnName": "Keyword",
    "separator": ", "
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column January using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "January",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column May using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "May",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column April using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "April",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column March using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "March",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column February using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "February",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Google Search Volume using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Google Search Volume",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column August using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "August",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column July using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "July",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column June using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "June",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column November using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "November",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column October using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "October",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column September using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "September",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - January using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - January",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Search Volume using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Search Volume",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column December using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "December",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - April using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - April",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - March using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - March",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - February using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - February",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - July using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - July",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - June using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - June",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - May using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - May",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - October using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - October",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - September using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - September",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - August using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - August",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - December using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - December",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik Monthly Data - November using expression grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik Monthly Data - November",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum()",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Sklik CPC using expression grel:forEach(value.split(','),v,v.toNumber()).sum() / length(forEach(value.split(','),v,v.toNumber()))",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Sklik CPC",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum() / length(forEach(value.split(','),v,v.toNumber()))",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Google CPC using expression grel:forEach(value.split(','),v,v.toNumber()).sum() / length(forEach(value.split(','),v,v.toNumber()))",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Google CPC",
    "expression": "grel:forEach(value.split(','),v,v.toNumber()).sum() / length(forEach(value.split(','),v,v.toNumber()))",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  }
]
```

### Přejmenování defaultních sloupců
```
[
  {
    "op": "core/column-rename",
    "description": "Rename column Keyword to Klíčové slovo",
    "oldColumnName": "Keyword",
    "newColumnName": "Klíčové slovo"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Google to Pozice Google",
    "oldColumnName": "Google",
    "newColumnName": "Pozice Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Result feature to Rich snippet",
    "oldColumnName": "Result feature",
    "newColumnName": "Rich snippet"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Number of results to Počet výsledků Google",
    "oldColumnName": "Number of results",
    "newColumnName": "Počet výsledků Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Google Landing Page to Vstupní stránka na Google",
    "oldColumnName": "Google Landing Page",
    "newColumnName": "Vstupní stránka na Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Seznam.cz to Pozice Seznam",
    "oldColumnName": "Seznam.cz",
    "newColumnName": "Pozice Seznam"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Seznam.cz Number of results to Počet výsledků Seznam",
    "oldColumnName": "Seznam.cz Number of results",
    "newColumnName": "Počet výsledků Seznam"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Seznam.cz Landing Page to Vstupní stránka na Seznam",
    "oldColumnName": "Seznam.cz Landing Page",
    "newColumnName": "Vstupní stránka na Seznam"
  },
  {
    "op": "core/column-removal",
    "description": "Remove column Search type",
    "columnName": "Search type"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Best landing page - Google to \"Nejlepší\" vstupní stránka Google",
    "oldColumnName": "Best landing page - Google",
    "newColumnName": "\"Nejlepší\" vstupní stránka Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Best landing page - Seznam.cz to \"Nejlepší\" vstupní stránka Seznam",
    "oldColumnName": "Best landing page - Seznam.cz",
    "newColumnName": "\"Nejlepší\" vstupní stránka Seznam"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Number of Results - Google to Počet kandidátů Google",
    "oldColumnName": "Number of Results - Google",
    "newColumnName": "Počet kandidátů Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Number of Results - Seznam.cz to Počet kandidátů Seznam",
    "oldColumnName": "Number of Results - Seznam.cz",
    "newColumnName": "Počet kandidátů Seznam"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Google SERP Competition to Konkurenčnost Google",
    "oldColumnName": "Google SERP Competition",
    "newColumnName": "Konkurenčnost Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Seznam SERP Competition to Konkurenčnost Seznam",
    "oldColumnName": "Seznam SERP Competition",
    "newColumnName": "Konkurenčnost Seznam"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Google Search Volume to Hledanost Google",
    "oldColumnName": "Google Search Volume",
    "newColumnName": "Hledanost Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Google CPC to CPC Google",
    "oldColumnName": "Google CPC",
    "newColumnName": "CPC Google"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Sklik Search Volume to Hledanost Seznam",
    "oldColumnName": "Sklik Search Volume",
    "newColumnName": "Hledanost Seznam"
  },
  {
    "op": "core/column-rename",
    "description": "Rename column Sklik CPC to CPC Seznam",
    "oldColumnName": "Sklik CPC",
    "newColumnName": "CPC Seznam"
  }
]
```
