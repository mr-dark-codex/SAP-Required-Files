# API URL Parameter 
## Allocation API:
`http://172.16.0.147:8001/sap/bc/rest/titogatepass?sap-client=786&gateslip=6204521954&plant=N421&vehtype=LOADING`

## Deallocation API:
`http://172.16.0.147:8001/sap/bc/rest/tito_weighment?sap-client=786&gateslip=6204521954&plant=N421&vehtype=LOADING`

`{
  "DRIVERNAME": "BANE SINGH",
  "GATESLIP": 6204521954,
  "VEHICLE": "MP04HE5040",
  "ENTRYDATE": "2025-07-03",
  "ENTRYTIME": "15:09:28",
  "VEHTYPE": "LOADING",
  "DO_QTY": 29.99,
  "TOT_COMPRTMNT_NO": 5,
  "COMP_1": 6,
  "COMP_2": 6,
  "COMP_3": 6,
  "COMP_4": 6,
  "COMP_5": 6,
  "TJ_DELIVERY": [
    {
      "VBELN": "8010322857",
      "POSNR": 1,
      "MATNR": " 21000004",
      "MAKTX": "Soya Refined Oil",
      "LFIMG": 30,
      "MEINS": "TO"
    }
  ]
}
`

#### fetchApi=http://172.16.0.147:8001/sap/bc/rest/TitoGatePass?sap-client=786&gateslip=6205158601&plant=N406&vehType=LOADING

gatename=MG_1
fetchApi=http://172.16.0.147:8001/sap/bc/rest/TitoGatePass?
sapApiUid=IBGTITO
sapApiPwd=Abis@2021
deallocationApi=http://172.16.0.147:8001/sap/bc/rest/tito_weighment?
deallApiUid=IBGTITO
deallApiPwd=Abis@2021
sapClientNo=786
plantNo=9406
readerIp=10.0.17.92


UP PLANT TITO: 
GATESLIP: 6201399659

http://172.16.0.147:8001/sap/bc/rest/TitoGatePass?sap-client=786&gateslip=6201399659&plant=N406&vehType=LOADING