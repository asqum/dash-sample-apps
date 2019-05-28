# Dash-mapd-demo

## About this app

A sample dash app which updates real-time visual analytics by constantly queries from a remote Omnisci(MapD) SQL Engine. 

## About this dataset

The public dataset using in this app, "flight_2008_7M" includes every single record of US airline flights, known by Bureau of Transportation Statistics in the year 2008. By default, it could be loaded from `insert_sample_data` script during Omnisci server installation. A [jupyter notebook](https://github.com/plotly/dash-mapD-demo/blob/dev/flights_data_clean.ipynb) has been included to showcase tabular structure and query results from this dataset.

## Requirements

* Python 3
* Omnisci server installation [Guide to install Omnisci](https://www.omnisci.com/docs/latest/4_docker.html) 

## How to run this app

To run this app, you will need a self-hosted Omnisci SQL engine running on `localhost:6274` with the default logins. [follow this guide](https://github.com/plotly/dash-mapD-demo/blob/dev/docker/README.md) to install a test database locally by dockerfile.

We suggest you to create a virtual environment for running this app with Python 3. Clone this repository 
and open your terminal/Command Prompt in root folder.

```
cd dash-mapd-demo
python3 -m virtualenv venv

```
In Unix system:
```
source venv/bin/activate

```
In Windows: 

```
venv\Scripts\activate
```

Install all required packages by running:
```
pip install -r requirements.txt
```

Run this app locally by:
```
python app.py
```

Click on individual state from choropleth map to visualize state-specific flight delays in other plots and datatable, drag along time-series, click on 
single bar or drag along scatters to know flight details in the table. 

## Screenshot & Screencast

![Screenshot1](img/screenshot.png)

![Animated1](img/mapd-demo-gif.gif)

## Resources

* [Dash](https://dash.plot.ly/)
* [Omnisci Core](https://www.omnisci.com/platform/core)
* [PymapD Python Client](https://pymapd.readthedocs.io/en/latest/)
* Inspired by [Omnisci Demo app](https://www.omnisci.com/demos/flights/#/dashboard/4?_k=ks7460).