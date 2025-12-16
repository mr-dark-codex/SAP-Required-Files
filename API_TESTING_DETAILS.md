# API TESTING DETAILS: 
## Details:
- 1. If Gateslip or Vehtype or Plant(Optional) no could not provide, 
`String: Input Paramater "gateslip or plant or vehtype" is missing`
    <!-- it will show Invalid Parameter. -->

- 2. If Vehtype is Random 
`{}`

- 3. if Vehtype is Mismatched(within this LOADING, UNLOADING, where loading required, we put unloading, vice versa)
`{"VEHTYPE":"UNLOADING"}`

- 4. if PlantNo is Mismateched(from given provieded number)
`{
  "DRIVERNAME": "BALA saheb",
  "GATESLIP": 6205158601,
  "VEHICLE": "TS05UD4488",
  "ENTRYDATE": "2025-12-12",
  "ENTRYTIME": "11:20:20",
  "VEHTYPE": "LOADING"
}
Without Material Details
`

- 5. if plantNo is Missing
`String: Input Paramater "gateslip or plant or vehtype" is missing`

- 6. sap-client may have some important work but from this layer we could not judge, if we will not pass it still required data is showing

- 7. If gateslip is random / mismatched
`
{
  "GATESLIP": 12312312,
  "VEHTYPE": "LOADING"
}
`

- 8. If gateslip is valid [this is not for this plant], still it shows 
`
{
  "DRIVERNAME": "manish",
  "GATESLIP": 6205158602,
  "VEHICLE": "RJ01GD6129",
  "ENTRYDATE": "2025-12-12",
  "ENTRYTIME": "10:23:04",
  "VEHTYPE": "LOADING"
}
without Material Details, because DATA COMING FROM SAP is global, it fetch from GATESLIP NO. 
`

## DEALLOCATION API: 

Among three important fields, 
plant, vehtype, gateslip these are the fields

1. Only Vehtype is mismatched(like Loading required, put Unloading, or vice versa), others are correct
`
[
  {
    "WERKS": plant,
    "NAME1": "Poultry Feed- Inhouse-Tumkur",
    "UNIT1": "KG"
  }
]
`

2. Only Vehtype is random, others are correct
`
[
  {
    "WERKS": plant,
    "NAME1": "Poultry Feed- Inhouse-Tumkur",
  }
]
`

3. If Only Gateslip is not found, others are correct.
`
[
  {
    "WERKS": plant,
    "NAME1": "Poultry Feed- Inhouse-Tumkur",
    "UNIT1": "KG"
  }
]
`

4. Only Plant is incorrect, others are correct
`
[
  {
    "WERKS": plant,
    "GINUS": "BDRDISPGATEI",
    "ETWEIGHT": 12210,
    "LTWEIGHT": 42200,
    "UNIT1": "KG"
  }
]
`

5. Gateslip and plant are incorrect, othes are correct 
`
[
  {
    "WERKS": "plant",
    "UNIT1": "KG"
  }
]
`


6. Gateslip and plant and vehtype are incorrect
`
[
  {
    "WERKS": "plant",
    "UNIT1": "KG"
  }
]
`


7. plant and vehtype are incorrect, gateslip are correct 
`
[
  {
    "WERKS": "plant"
  }
]
`


6. all are correct  
`
[
  {
    "WERKS": "N421",
    "NAME1": "Poultry Feed- Inhouse-Tumkur",
    "GINUS": "BDRDISPGATEI",
    "ETWEIGHT": 12210,
    "LTWEIGHT": 42200,
    "UNIT1": "KG"
  }
]

`


