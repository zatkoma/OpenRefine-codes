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
