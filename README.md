# COVID-19 Data Visualizations :chart_with_upwards_trend::bar_chart::chart_with_downwards_trend:  

Set of data visualizations for COVID-19 data from [Johns Hopkins CSSE department](https://github.com/CSSEGISandData/COVID-19). Charts of time series trends are inspired by the plot from this article in the [Financial Times](https://www.ft.com/coronavirus-latest), graphics by [John Burn-Murdoch](https://twitter.com/jburnmurdoch).  

The file `covid_visualization.ipynb` contains a set of functions for extracting key pieces of data from the JHU dataset:  

## Functions  

```python
covidData(country, output=1, start=100)
```  

#### Extracts time series data of interest for a specific country  

