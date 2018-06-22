# ExcelToArray
Read excel data to AHK array

### Usage
`arr := ExcelToArray(FileName, nSheet, last_row, last_column)`
- `FileName` - The excel file path.
- `nSheet` - (Optional) Sheet number. Default is 1.
- `last_row` - (Optional) Last row number.
- `last_column` - (Optional) Last column number.

Example of output array:
```Json
[
  [
    "a1",
    "b1",
    "c1"
  ],
  [
    "a2",
    "b2",
    "c2"
  ]
]
```

Note: This function uses `sheet.Range(cell_begin, cell_end).FormulaR1C1` (instead of `.Value`) to read the data, it can avoids the numbers such as `1.2` converted into `1.200000`. But if your cells have formula, the formula code will be read, not the actual value.
