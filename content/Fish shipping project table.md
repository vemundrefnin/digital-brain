---
title: Fish shipping project table
publish: false
tags: 
- master-thesis 
- shipping 
- aqua
- cis5250 
---
| Field             | Description                                                                                                                                                    | Dataset source                                                                       |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Year              |                                                                                                                                                                |                                                                                      |
| Shiptype category | A number representing which shiptype category the data on this row is based on.                                                                                |                                                                                      |
| Track count       | The number of tracks reported. Sometimes a track is only one coordinate other times it is multiple coordinates over a longer time-period. For example 2 hours. | Kystverket - AIS (powered by BarentsWatch)                                           |
| Track km          | The distance the ships have traveled in kilometres.                                                                                                            | Kystverket - AIS (powered by BarentsWatch)                                           |
| Departures        | The number of reported departures.                                                                                                                             | Kystverket - SafeSeaNet                                                              |
| Cargo movement    | Cargo times the kilometers the cargo is moved. This is calculated per ship and summed up in total for each year.                                               |                                                                                      |
| Live stock        | Atlantic Salmon Live stock 31.12. According to Fiskedirektoratet this should be quality check and therefore correct.                                           | Fiskedirektoratet - sta-laks-mat-11-beh-bevegelse.xlsx -> My restructured .xlsx file |
| Input             | Atlantic Salmon Input.                                                                                                                                         | Fiskedirektoratet - sta-laks-mat-11-beh-bevegelse.xlsx -> My restructured .xlsx file |
| Output            | Atlantic Salmon Output.                                                                                                                                        | Fiskedirektoratet - sta-laks-mat-11-beh-bevegelse.xlsx -> My restructured .xlsx file |
| Losses            | Atlantic Salmon Losses.                                                                                                                                        | Fiskedirektoratet - sta-laks-mat-11-beh-bevegelse.xlsx -> My restructured .xlsx file |

