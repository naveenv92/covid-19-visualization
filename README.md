# COVID-19 Data Visualizations :chart_with_upwards_trend::bar_chart::chart_with_downwards_trend:  

Set of data visualizations for COVID-19 data from [Johns Hopkins CSSE department](https://github.com/CSSEGISandData/COVID-19). Charts of time series trends are inspired by the plot from this article in the [Financial Times](https://www.ft.com/coronavirus-latest), graphics by [John Burn-Murdoch](https://twitter.com/jburnmurdoch).  

The file `covid_visualization.ipynb` contains a set of functions for extracting key pieces of data from the JHU dataset. Feel free to use or adapt these functions for your specific use case:  

## Functions  

```python
covidData(country, output=1, start=100)
```  

#### Extracts time series data of interest for a specific country  

`country` &ndash; string with country name of interest  
`output` &ndash; type of output (`1` for confirmed cases, `2` for recovered cases, `3` for deaths, `4` for net (open) cases &ndash; default `1`)  
`start` &ndash; number of cases after which to report data (<i>e.g.</i> starting after the n<sup>th</sup> case &ndash; default `100`)  

&nbsp;  

```python
doubling_rate(country, output=1)
```  

#### Returns the projected doubling rate as well as the most recent doubling event  

The growth rate (<i>r</i>) is calculated from the difference in cases between the most recent data point and two days prior:  

<p align='center'>
	<i>x<sub>n</sub> = x<sub>n – 2</sub> &middot; (1 + r)<sup>2</sup></i>
</p>  

From the value of <i>r</i>, the projected number of days for doubling (<i>n</i>) can be calculated:  

<p align='center'>
	<i>(1 + r)<sup>n</sup> = 2</i>
</p>  

`country` &ndash; string with country name of interest  
`output` &ndash; type of output (`1` for confirmed cases, `2` for recovered cases, and `3` for deaths &ndash; default `1`)   