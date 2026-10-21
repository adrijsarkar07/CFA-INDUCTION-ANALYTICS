# Data source and dictionary

The notebook downloads the [UCI Beijing PM2.5 dataset (ID 381)](https://archive.ics.uci.edu/dataset/381/beijing+pm2+5+data) with `fetch_ucirepo(id=381)`. Citation: Chen, S. (2015), DOI [10.24432/C5JS49](https://doi.org/10.24432/C5JS49), CC BY 4.0.

The source has 43,824 hourly observations from 2010-01-01 to 2014-12-31. PM2.5 was measured at the US Embassy in Beijing; weather was recorded at Beijing Capital International Airport. Their spatial mismatch limits interpretation.

| Column | Meaning | Unit / role |
|---|---|---|
| `year`, `month`, `day`, `hour` | Calendar components | Used to construct timestamp; month/hour inform engineered inputs |
| `PM25` | Renamed source `pm2.5` | Target, µg/m³ |
| `DEWP` | Dew point | °C |
| `TEMP` | Air temperature | °C |
| `PRES` | Pressure | hPa |
| `cbwd` | Combined wind direction | Categorical |
| `Iws` | Cumulated wind speed, as defined by the source | Source reports m/s; not an instantaneous reading |
| `Is` | Cumulated hours of snow | hours |
| `Ir` | Cumulated hours of rain | hours |
| `timestamp` | Derived date and hour | Datetime; not directly supplied to the model |

The submitted AirCast CSVs are **model results**, not the original pollution data. No raw Beijing CSV was included among these attachments. Housing, MNIST and Anscombe files are unrelated sample datasets and are excluded from this repository.

The notebook currently downloads the data each run. Keeping a source snapshot with its acquisition date and checksum is a possible reproducibility improvement; a local snapshot is not yet loaded by the current code.
