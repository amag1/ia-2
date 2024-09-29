Any data obtained via measurements at regular intervals.
## Propiedades
1. Period: time steps at which the series is observed
2. Frequency: frequency at which the series is observed
3. Trend: long term change in the mean of the data
4. Stationarity: when time series properties remain constant over time
5. Regularity: whether the series is captured at regular intervals
6. Seasonality: regular and predictable changes
7. Autocorrelation: correlation with past observations

## Tasks
Típicamente las queremos usar para **predecir**, pero también se puede usar para:
- Clasificación
- Detección de eventos (hotword detection "OK, Google")
- Detección de anomalías

## RNN
Las redes neuronales tradicionales no tienen memoria -> no hay estado entre inputs
Una [[RNN]] tiene **estado** como un loop interno