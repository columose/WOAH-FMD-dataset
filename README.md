# World Organisation of Animal Health: Foot and mouth disease dataset project

## Table of Contents
* Summary
* Objectives
* Methods
* Overview of dataset
* Results (in brief)
* Discussion
* Limitations
* Datasets: raw, cleaned, grouped

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
* Baselining count data to detect trends in world regions with fewer counts accross variables.
* Correlation matrices within world regions to explore relationships between variables.
* Post-hoc regression analysis to determine whether 'cases' in Europe can predict 'killed and disposed of' (culling).
* Create choropleth maps for each FMD variable to understand trends between neighbouring countries.
* Cluster analysis to group related variables (e.g. New outbreaks, Cases, Deaths), and plot on a choropleth map.

## Overview of the dataset
The majority of FMD outbreaks and cases occurred in Africa and Asia, with as few as 3 European countries reporting outbreaks since 2005.

<img src = 'https://drive.google.com/uc?id=1jt9cwg6YEwzh510e6ZfpmeSB74YtD331'>

## Results(in brief)
Asia experienced a spike in new outbreaks around 2022, coupled by an increase in cases and vaccinated. There was an inexplicably high slaughter rate in Africa that same year, despite the lack of new FWD cases on the continent. Counts
were low across Europe and the Americas.

<img src = https://drive.google.com/uc?id=1CKTJVX-taw5N0PAMC7qHsUV3NNQr8xjJ>


The top 5 highest slaughtering count events in the dataset occurred in South Africa between 2021-2022.


<img src = https://drive.google.com/uc?id=1-0jQr56Jgou70rgFkQEwXzV57dBFGZny>


Baselining provides a different outlook on the data as trends in Europe and America become visible. There was a very clear spike in 'cases' and 'killed and disposed of' in Europe


<img src = https://drive.google.com/uc?id=1CKTJVX-taw5N0PAMC7qHsUV3NNQr8xjJ>


Some variables are strongly correlated within world regions.'Cases' and 'killed and disposed of are perfectly positively correlated in Europe, as was indicative from the baselined time-series plot,

<img src = https://drive.google.com/uc?id=1zmud3qE-K764Xiyc9cUy1lqM4BPrtq86>

A linear regression model revealed the 'case' count predicts 99.8% of variance in 'killed and disposed of' in Europe. In other words, the 3 European countries that have reported FMD outbreaks in the past 20 years have dealt with the outbreaks through culling en-masse.

<img src = https://drive.google.com/uc?id=1-8VmFZr2jAMQYo-PnWEPitq6BvvkuZrQ>

Choropleth maps provide a nice persective on trends across neighbouring countries. For example, most outbreaks are occuring across neighbouring Asian countries.

<img src = https://drive.google.com/uc?id=1s6d97Kls5Z6U7svjdJETS0GD410TWjgw>
