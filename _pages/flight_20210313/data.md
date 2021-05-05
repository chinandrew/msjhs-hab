---
title: "March 13, 2021 Data"
permalink: /flight20210313/data/
layout: single
excerpt: "Data from 2021-03-13 flight."
sidebar:
  nav: "data"
---

Data is available [here (`msjhshab_20210313.7z`, 4.5MB)]({{ site.url }}{{ site.baseurl }}/assets/data/flight20210313/msjhshab_20210313.7z) as a 7zip archive of CSV files.

Not all sensors were calibrated before flight due to inadequate reference environments. As a result, some of the values presented are the raw sensor reading or the voltage, which are still useful for observing changes in trends. For more information about the sensors flown, see the [Hardware - Sensors]({{ "/flight20210313/sensors/" | relative_url }}) page for this flight.


## Data dictionaries

10 files were generated from the sensors.

`accelerometer.csv`

|   | Column   | Description                                                        |
| - | -------- | ----------------------------------------------------------------- |
| 1 | time     | Timestamp captured by Arduino on board real time clock.            |
| 2 | time\_ms | Timestamp captured by Arduino on millisecond clock.                |
| 3 | accX     | Gravitation force (G’s) in X direction (sideways horizontal axis). |
| 4 | accY     | Gravitation force (G’s) in Y direction (perpendicular to X).       |
| 5 | accZ     | Gravitation force (G’s) in Z direction (vertical axis).            |
| 6 | gyroX    | Degrees per second in X direction.                                 |
| 7 | gyroY    | Degrees per second in Y direction.                                 |
| 8 | gyroZ    | Degrees per second in Z direction.                                 |
| 9 | temp(C)  | Empty, ignore this column.                                         |

`air_quality.csv`  

|   | Column          | Description                                                         |
| - | --------------- | ------------------------------------------------------------------- |
| 1 | time            | Timestamp captured by Arduino on board real time clock.             |
| 2 | time\_ms        | Timestamp captured by Arduino millisecond clock.                    |
| 3 | quality\_sensor | Raw sensor value, from 0 to 1023. Lower value means better quality. |

`altimeter.csv`

|   | Column         | Description                                                        |
| - | -------------- | ------------------------------------------------------------------ |
| 1 | time           | Timestamp captured by Arduino on board real time clock.            |
| 2 | altitude\_cm   | Altitude in centimeters, determined from pressure and temperature. |
| 3 | pressure\_pa   | Pressure in Pascals.                                               |
| 4 | temperature\_c | Temperature in Celsius.                                            |


`co2.csv`

|   | Column   | Description                                                    |
| - | -------- | -------------------------------------------------------------- |
| 1 | time\_ms | Timestamp captured by Arduino millisecond clock.               |
| 2 | co2\_V   | Sensor voltage. Lower value means higher concentration of CO2. |


`light.csv`  

|   | Column        | Description                                                     |
| - | ------------- | --------------------------------------------------------------- |
| 1 | time\_ms      | Timestamp captured by Arduino millisecond clock.                |
| 2 | light\_sensor | Raw sensor value, from 0 to 1023. Lower value means less light. |

`load_cell.csv`

|   | Column   | Description                                             |
| - | -------- | ------------------------------------------------------- |
| 1 | time     | Timestamp captured by Arduino on board real time clock. |
| 2 | time\_ms | Timestamp captured by Arduino millisecond clock.        |
| 3 | load\_g  | Weight measured in grams.                               |

`magnetometer.csv`

|   | Column   | Description                                      |
| - | -------- | ------------------------------------------------ |
| 1 | time\_ms | Timestamp captured by Arduino millisecond clock. |
| 2 | X        | nanoTesla strength in X axis direction.          |
| 3 | Y        | nanoTesla strength in Y axis direction.          |
| 4 | Z        | nanoTesla strength in Z axis direction.          |

`mq9.csv`

|   | Column      | Description                                                            |
| - | ----------- | ---------------------------------------------------------------------- |
| 1 | time        | Timestamp captured by Arduino on board real time clock.                |
| 2 | time\_ms    | Timestamp captured by Arduino millisecond clock.                       |
| 3 | mq9\_sensor | Raw sensor value, from 0 to 1023. Lower value means less LPG, CO, CH4. |	

`temphumiditybaro.csv`

|   | Column         | Description                                      |
| - | -------------- | ------------------------------------------------ |
| 1 | time\_ms       | Timestamp captured by Arduino millisecond clock. |
| 2 | temperature\_c | Temperature in Celsius.                          |
| 3 | humidity       | % relative humidity.                             |
| 4 | pressure\_pa   | Pressure in Pascals.                             |

`uv.csv`  

|   | Column     | Description                                             |
| - | ---------- | ------------------------------------------------------- |
| 1 | time       | Timestamp captured by Arduino on board real time clock. |
| 2 | uv\_sensor | Raw sensor value, from 0 to 1023. Lower value less UV.  |