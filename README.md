# Snow Depth Analysis in Lombardia from June 2023 to June 2024

Project for the "Health Information Systems" course, held at Università degli Studi di Brescia (Italy).

The main objective is this project is to analyze the evolution of snow depth in
Lombardy region in the period going from June 2023 to June 2024. The analysis is
carried out in the following way:

- Graph the trend of snow depth during the selected time period across all
provinces, and make comparisons.
- Compare the accumulation of snow at different altitudes.
- Visualize the evolution of snow depth due to multiple factors like precipitations, temperature, solar irradiance, and relative humidity.

## How to replicate

The original datasets for the sensor readings have not been uploaded due to their gargantuan size, with the exception of the sensors and stations dataset.

In the current state, only the `*analysis.Rmd` notebooks can be executed, since they rely on the already processed datasets (which can be found in the `processed_dataset` folder).

In order to execute also the `*readings.Rmd` notebooks, the original datasets have to be downloaded from [ARPA Lombardia](https://www.dati.lombardia.it/stories/s/auv9-c2sj) website and put within the `arpa_dataset` folder, for all the following reading types:

- **Altezza Neve (cm):** snow height, [readings from 2021](https://www.dati.lombardia.it/Ambiente/Altezza-neve-dal-2021/uqbu-tt6m)
- **Precipitazione (mm):** precipitation, [readings from 2021](https://www.dati.lombardia.it/Ambiente/Precipitazioni-dal-2021/pstb-pga6)
- **Temperatura dell’aria (°C):** air temperature, [readings from 2021](https://www.dati.lombardia.it/Ambiente/Temperatura-dal-2021/w9wd-u6jh)
- **Umidità Relativa (%):** relative humidity, [readings from 2021](https://www.dati.lombardia.it/Ambiente/Umidit-relativa-dal-2021/823w-fh4c)
- **Radiazione Globale (W/m2):** solar irradiance, [readings from 2021](https://www.dati.lombardia.it/Ambiente/Radiazione-Globale-dal-2021/cxym-eps2)

The website providing these readings allows to filter them based on the date of
recording, thus allowing to download only the necessary readings collected from
June 2023. Despite this, at the time of collection, all datasets did not provide data
up to June 2024. In fact, most of them contained data up until February 2024.

This required the introduction of an additional dataset, with the same format of
the previous datasets, which includes data from the last seven months for all types
of readings, all collected in this single dataset in uncompressed tabular format:

- **Dati sensori meteo:** weather sensor data, [readings from last seven months](https://www.dati.lombardia.it/Ambiente/Dati-sensori-meteo/647i-nhxk)

Eventually, the current weather sensor data will be merged with the previous dataset, which means it work be necessary anymore to merge "current" data with "historic" data. The code sections that handle these operations will need to be disabled.