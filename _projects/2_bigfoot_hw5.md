# Homework 5: Exploring Bigfoot Reports

For this assignment, I looked at when Bigfoot reports were made and
the weather conditions connected to them. These are reported sightings,
so the data does not prove that Bigfoot exists.

## Plot 1: Reports by Season

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_seasons.json" style="width: 100%"></vegachart>

My first plot shows how the number of Bigfoot reports differs across
the four seasons. I cleaned up extra spaces in the season column,
removed missing values and labels outside the four seasons, and
counted the reports for each season using Pandas. I used a bar chart
because it makes the differences easy to compare. Season is a nominal
variable on the x-axis, and the number of reports is a quantitative
variable on the y-axis. I kept the seasons in calendar order and
started the count axis at zero so the bars show the differences fairly.
I chose one green color since I am only comparing counts and do not
need color to represent another variable. Summer has the most reports,
but that could also be related to people spending more time outside.

## Plot 2: Weather Conditions

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_weather.json" style="width: 100%"></vegachart>

My second plot looks at daily high temperature and humidity for the
reports that have weather data. I converted both columns to numbers,
removed rows with missing values, and kept reports with a recognized
season and humidity between zero and one. Each dot represents one
report. I used quantitative encodings for both axes, with temperature
in degrees Fahrenheit on the x-axis and humidity on the y-axis.
Humidity is shown as a percentage from zero to 100%. I let the
temperature axis start above zero to make better use of the space
because this is a scatterplot. I used purple for all the dots since
color does not represent a separate variable. The dots are partly
transparent so overlapping reports are easier to see. This shows the
conditions connected to the reports, but it does not mean those
conditions caused the sightings.

## Interactivity

I added a dropdown to the second plot so users can switch between
Spring, Summer, Fall, and Winter. It starts with Spring selected.
This makes it easier to look at one season without all the other
reports covering the plot. Users can also hover over a dot to see
its temperature, humidity, and season. The dropdown is saved with
the Altair chart, so it works directly on this webpage.

## Data and Analysis

[The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv)

[The Analysis — Python Notebook](https://github.com/shoirathi10/shoirathi10.github.io/blob/main/python_notebooks/Workbook.ipynb)
