Z 1.12.2019 převede na 20201201 vše nad sloupcem "Date"

```
[
  {
    "op": "core/column-addition",
    "description": "Create column DAYS at index 2 based on column Date using expression grel:if(value.split(\".\")[0].toNumber() <= 9, 0 + value.split(\".\")[0] , value.split(\".\")[0] )",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "newColumnName": "DAYS",
    "columnInsertIndex": 2,
    "baseColumnName": "Date",
    "expression": "grel:if(value.split(\".\")[0].toNumber() <= 9, 0 + value.split(\".\")[0] , value.split(\".\")[0] )",
    "onError": "set-to-blank"
  },
  {
    "op": "core/column-addition",
    "description": "Create column MONTHS at index 2 based on column Date using expression grel:if(value.split(\".\")[1].toNumber() <= 9, 0 + value.split(\".\")[1] , value.split(\".\")[1] )",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "newColumnName": "MONTHS",
    "columnInsertIndex": 2,
    "baseColumnName": "Date",
    "expression": "grel:if(value.split(\".\")[1].toNumber() <= 9, 0 + value.split(\".\")[1] , value.split(\".\")[1] )",
    "onError": "set-to-blank"
  },
  {
    "op": "core/column-addition",
    "description": "Create column YEAR at index 2 based on column Date using expression grel:if(value.split(\".\")[2].toNumber() < 9, 0 + value.split(\".\")[2] , value.split(\".\")[2] )",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "newColumnName": "YEAR",
    "columnInsertIndex": 2,
    "baseColumnName": "Date",
    "expression": "grel:if(value.split(\".\")[2].toNumber() < 9, 0 + value.split(\".\")[2] , value.split(\".\")[2] )",
    "onError": "set-to-blank"
  },
  {
    "op": "core/text-transform",
    "description": "Text transform on cells in column Date using expression grel:cells[\"YEAR\"].value + cells[\"MONTHS\"].value + cells[\"DAYS\"].value",
    "engineConfig": {
      "facets": [],
      "mode": "row-based"
    },
    "columnName": "Date",
    "expression": "grel:cells[\"YEAR\"].value + cells[\"MONTHS\"].value + cells[\"DAYS\"].value",
    "onError": "keep-original",
    "repeat": false,
    "repeatCount": 10
  },
  {
    "op": "core/column-removal",
    "description": "Remove column YEAR",
    "columnName": "YEAR"
  },
  {
    "op": "core/column-removal",
    "description": "Remove column MONTHS",
    "columnName": "MONTHS"
  },
  {
    "op": "core/column-removal",
    "description": "Remove column DAYS",
    "columnName": "DAYS"
  }
]
```
