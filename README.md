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

## Summary
* The dataset was heavily dominated by FMD incidents in Africa and Asia.
* Culling appears to be the preferred method to prevent the spread of FMD outbreaks in Europe.
* Additional data is required to perform regression analyses on worlwide data (e.g. healthy flock count).

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
* Cluster analysis to group related variables (e.g. New outbreaks, Cases, Deaths), and plot on a choropleth map.

## Overview of the dataset
The majority of FMD outbreaks and cases occurred in Africa and Asia, with as few as 3 European countries reporting outbreaks since 2005.

<img src = 'https://drive.google.com/uc?id=1jt9cwg6YEwzh510e6ZfpmeSB74YtD331'>

## Results
Asia experienced a spike in new outbreaks around 2022, coupled by an increase in cases and vaccinated. There was an inexplicably high slaughter rate in Africa that same year, despite the lack of new FWD cases on the continent. Counts
were low across Europe and the Americas.

<img src = 'https://drive.google.com/uc?id=1CKTJVX-taw5N0PAMC7qHsUV3NNQr8xjJ'>


### The top 5 highest slaughtering count events in the dataset occurred in South Africa between 2021-2022.

<img src = 'https://drive.google.com/uc?id=1-0jQr56Jgou70rgFkQEwXzV57dBFGZny'>


Baselining provides a different outlook on the data as trends in Europe and America become visible. There was a very clear spike in 'cases' and 'killed and disposed of' in Europe

<img src = 'https://drive.google.com/uc?id=1CKTJVX-taw5N0PAMC7qHsUV3NNQr8xjJ'>

Some variables are strongly correlated within world regions.'Cases' and 'killed and disposed of are perfectly positively correlated in Europe, as was indicative from the baselined time-series plot.

<img src = 'https://drive.google.com/uc?id=1zmud3qE-K764Xiyc9cUy1lqM4BPrtq86'>

A linear regression model revealed the 'case' count predicts 99.8% of variance in 'killed and disposed of' in Europe. In other words, the 3 European countries that have reported FMD outbreaks in the past 20 years have dealt with the outbreaks through culling en-masse.

<img src = 'https://drive.google.com/uc?id=1-8VmFZr2jAMQYo-PnWEPitq6BvvkuZrQ'>

Choropleth maps provide a nice persective on trends across neighbouring countries. For example, most outbreaks are occuring across neighbouring Asian countries.

<img src = 'https://drive.google.com/uc?id=1s6d97Kls5Z6U7svjdJETS0GD410TWjgw'>

## Discussion

Some of the main take-home points are:

* The majority of FMD cases and outbreaks occur in Asia.
* The inexplicably high slaughtering count in South Africa could be followed up on.
* European countries have dealt with FMD outbreaks through mass culling.

## Limitations

More data is required to perform more advanced regression analyses. A random forest model using 'Susceptible' and 'Vaccinated' as features and 'New outbreaks' as a predictor yielded an $r^{2}$ value of .46. Additional variables such as 'flock count' could improve the model's performance.

## Datasets: raw, cleaned, grouped

The raw dataset was sourced from the WOAH's animal information system
 at https://wahis.woah.org/#/dashboards/qd-dashboard.

[Clean data](https://drive.google.com/file/d/1_7HGF96LRCa3UUsiVRKSwSh6lf4mswRV/view?usp=drive_link)

[Data summed and grouped by world region for time-series ploting](https://drive.google.com/file/d/1EG-H1wYbE5k1kQ1nsgEmhity_JAHODQK/view?usp=sharing)

[Data summed and grouped by country for choropleth maps](https://drive.google.com/file/d/1hHRCTFCBasPDwvNNhQSMXMGOKVBAUt50/view?usp=sharing)

