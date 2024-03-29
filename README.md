# World Organisation for Animal Health: Foot and mouth disease (FMD) dataset project

## Table of Contents
* [Summary](#Summary)
* [Objectives](#Objectives)
* [Methods](#Methods)
* [Overview of the dataset](#Overview-of-the-dataset)
* [Results (in brief)](#Results)
* [Discussion](#Discussion)
* [Limitations](#Limitations)
* [Datasets: raw, cleaned, grouped](#Datasets-raw-cleaned-grouped)
* [Python scripts](#Python-scripts)
* [Tableau dashboard](#Tableau-dashboard)

## Summary
* The dataset was heavily dominated by FMD incidents in Africa and Asia.
* Culling appears to be the preferred method to prevent the spread of FMD outbreaks in Europe.
* Additional data is required to perform regression analyses on worlwide data (e.g. animal population).

## Objectives
Analyse FMD dataset to explore regional trends over time, determine the efficacy of vaccinations on case and death count, and eluciate the most effective methods for dealing with FMD outbreaks.

## Methods
* Dataset cleaning.
* Descriptive statistics.
* Time-series analysis of countries grouped by world region.
* Plotting outliers.
* Baselining data to detect trends in world regions with fewer counts across variables.
* Correlation matrices within world regions to explore relationships between variables.
* Post-hoc regression analysis to determine whether 'cases' in Europe can predict 'killed and disposed of' (culling).
* Create choropleth maps for each FMD variable to understand trends between neighbouring countries.
* Cluster analysis to group countries with similar counts on a variable (e.g. vaccination rate), and plot on a choropleth map.

## Overview of the dataset
The majority of FMD outbreaks and cases occurred in Africa and Asia, with as few as 3 European countries reporting outbreaks since 2005.

![Overview](https://github.com/columose/WOAH-FMD-dataset/blob/cd31ba06298a63a29355a8b38817a9349e28c23e/Figure%20output/Country%20count.png)


## Results
Asia experienced a spike in new outbreaks around 2022, coupled by an increase in cases and vaccinated. There was an inexplicably high slaughter rate in Africa that same year, despite the lack of new FWD cases on the continent. Counts
were low across Europe and the Americas.

![time-series](https://github.com/columose/WOAH-FMD-dataset/blob/9dd73bfb0fddca4963bdc32ad5e24c45e9770cea/Figure%20output/Grouped%20time-series%20plot.png)

The top 5 highest slaughtering count events in the dataset occurred in South Africa between 2021-2022.

![slaughtering](https://github.com/columose/WOAH-FMD-dataset/blob/9dd73bfb0fddca4963bdc32ad5e24c45e9770cea/Figure%20output/Top%205%20slaughtering.png)


Baselining provides a different outlook on the data as trends in Europe and America become visible. There was a very clear spike in 'cases' and 'killed and disposed of' in Europe

![baselining](https://github.com/columose/WOAH-FMD-dataset/blob/9dd73bfb0fddca4963bdc32ad5e24c45e9770cea/Figure%20output/Baselined%20time-series.png)

Some variables are strongly correlated within world regions.'Cases' and 'killed and disposed of' are perfectly positively correlated in Europe, as was indicative from the baselined time-series plot.

![region-heatmaps](https://github.com/columose/WOAH-FMD-dataset/blob/9dd73bfb0fddca4963bdc32ad5e24c45e9770cea/Figure%20output/World%20regions%20correlation%20matrices.png)

A linear regression model revealed the 'Cases' count predicts 99.8% of variance in 'killed and disposed of' in Europe. In other words, the 3 European countries that have reported FMD outbreaks in the past 20 years have dealt with the rise in cases by increasing culling rates.

![regression](https://github.com/columose/WOAH-FMD-dataset/blob/9dd73bfb0fddca4963bdc32ad5e24c45e9770cea/Figure%20output/Regression%20between%20Cases%20and%20Killed%20and%20disposed%20of%20in%20Europe.png)

Choropleth maps provide a nice persective on trends across neighbouring countries. For example, most outbreaks are occuring across neighbouring Asian countries.

![choropleth](https://github.com/columose/WOAH-FMD-dataset/blob/9dd73bfb0fddca4963bdc32ad5e24c45e9770cea/Figure%20output/Choropleth%20original.png)

## Discussion

Some of the main take-home points are:

* The majority of FMD cases and outbreaks occur in Asia.
* The inexplicably high slaughtering count in South Africa could be followed up on.
* European countries have dealt with increases in FMD cases through mass culling.

## Limitations

More data is required to perform more advanced regression analyses. A random forest model using 'Susceptible' and 'Vaccinated' as features and 'New outbreaks' as a target yielded an $r^{2}$ value of .46. Additional variables such as 'animal population' and 'mean temperature per month' could improve the model's performance.

## Datasets: raw, cleaned, grouped

* The raw dataset was sourced from the [WOAH's animal information system](https://wahis.woah.org/#/dashboards/qd-dashboard).

* [Clean data](https://drive.google.com/file/d/1_7HGF96LRCa3UUsiVRKSwSh6lf4mswRV/view?usp=drive_link)

* [Data summed and grouped by world region for time-series ploting](https://drive.google.com/file/d/1EG-H1wYbE5k1kQ1nsgEmhity_JAHODQK/view?usp=sharing)

* [Data summed and grouped by country for choropleth maps](https://drive.google.com/file/d/1hHRCTFCBasPDwvNNhQSMXMGOKVBAUt50/view?usp=sharing)

## Python scripts
All of the processing scripts for this project can be retrieved from the repository. Click on the 'Open in Colab' icon for better legibility, as each notebook cell becomes condensed when copying from Google Colab to Github.

## Tableau dashboard
The main findings are summarised using an interactive dashboard in [Tableau public](https://public.tableau.com/app/profile/colum.s./viz/WOAHFMDproject/Dashboard).
