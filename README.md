# CO2 Trends Analysis 1930-2021

An interactive dashboard of carbon dioxide emissions by continent and country, built with Panel and hvPlot.

### Dataset Attribution

The carbon emissions dataset used in this project is sourced from Our World in Data and is available at the following URL:

- Dataset: [Our World in Data CO₂ and Greenhouse Gas Emissions dataset](https://ourworldindata.org/co2-and-greenhouse-gas-emissions)

The included copy, `owid-co2-data.csv`, covers 1930 to 2021, with one row per country or region per year. It includes total emissions, emissions per person, emissions by fuel source, population, and GDP. Emissions are measured in million tonnes of CO₂.

### What's in the dashboard

All of the work is in [`GCB-2022.ipynb`](GCB-2022.ipynb). A year slider, running from 1960 to 2021 in 5-year steps, controls every chart:

- **CO₂ emissions over time by continent.** A line chart and a matching table, switchable between total emissions and emissions per person.
- **CO₂ vs. GDP per person.** A scatterplot with one point per country for the selected year. GDP per person is calculated from the dataset's GDP and population.
- **CO₂ sources by continent.** A bar chart comparing emissions from coal, oil, and gas for the selected year.

Missing values are filled with 0 before charting, so a country with no data for a year shows up as zero.

### How to run

```bash
pip install pandas numpy panel hvplot jupyter
jupyter notebook GCB-2022.ipynb
```

To open the full dashboard in your browser instead:

```bash
panel serve GCB-2022.ipynb --show
```

### Technologies

**[Python](https://www.python.org/)**

**[pandas](https://pandas.pydata.org/)**

**[Panel](https://panel.holoviz.org/)**

**[hvPlot](https://hvplot.holoviz.org/)**
