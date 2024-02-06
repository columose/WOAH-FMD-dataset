{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": [],
      "mount_file_id": "1LuTWa_lxlyARBfEr0KkiP6dJd3s20KfL",
      "authorship_tag": "ABX9TyNRKOsJtmPZbPIMhg28clpB",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/columose/WOAH-FMD-dataset/blob/main/README.md\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "# **World Organisation of Animal Health: Foot and mouth disease dataset**"
      ],
      "metadata": {
        "id": "n1iPh6MoP_It"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Table of Contents**\n",
        "\n",
        "* [Summary](#scrollTo=6xFtcNjNQjcK&line=2&uniqifier=1)\n",
        "* [Objectives](#scrollTo=4uFRNw_hGeER&line=3&uniqifier=1)\n",
        "* [Methods](#scrollTo=aJtUrB7kz4Em&line=1&uniqifier=1)\n",
        "* [Overview of dataset](#scrollTo=rdqd6y9sC7zD&line=5&uniqifier=1)\n",
        "* [Results (in brief)](#scrollTo=oaMx_7mG4hHQ&line=29&uniqifier=1)\n",
        "* [Discussion](#scrollTo=sENhhtW3EWLy&line=8&uniqifier=1)\n",
        "* [Limitations](#scrollTo=sENhhtW3EWLy&line=8&uniqifier=1)\n",
        "* [Datasets: raw, cleaned, grouped](#scrollTo=-1Y7e33ZLqzt&line=1&uniqifier=1)"
      ],
      "metadata": {
        "id": "g1lWLf5CQLB9"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Summary**\n",
        "* The dataset was heavily dominated by FMD incidents in Africa and Asia.\n",
        "* Culling appears to be the preferred method to prevent the spread of FMD outbreaks in Europe.\n",
        "* Additional data is required to perform regression analyses on worlwide data (e.g. healthy flock count).\n",
        "\n",
        "\n",
        "\n"
      ],
      "metadata": {
        "id": "6xFtcNjNQjcK"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Objectives**\n",
        "\n",
        "Analyse FMD dataset to explore regional trends over time, determine the efficacy of vaccinations on case and death count, and eluciate the most effective methods for dealing with FMD outbreaks."
      ],
      "metadata": {
        "id": "4uFRNw_hGeER"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Methods**\n",
        "\n",
        "* Dataset cleaning.\n",
        "* Descriptive statistics.\n",
        "* Time-series analysis of countries grouped by world region.\n",
        "* Plotting outliers.\n",
        "* Baselining count data to detect trends in world regions with fewer counts accross variables.\n",
        "* Correlation matrices within world regions to explore relationships between variables.\n",
        "* Post-hoc regression analysis to determine whether 'cases' in Europe can predict 'killed and disposed of' (culling).\n",
        "* Create choropleth maps for each FMD variable to understand trends between neighbouring countries.\n",
        "* Cluster analysis to group related variables (e.g. New outbreaks, Cases, Deaths), and plot on a choropleth map.\n",
        "\n",
        "\n"
      ],
      "metadata": {
        "id": "aJtUrB7kz4Em"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Overview of the dataset**\n",
        "\n",
        "\n",
        "The majority of FMD outbreaks and cases occurred in Africa and Asia, with as few as 3 European countries reporting outbreaks since 2005.\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1jt9cwg6YEwzh510e6ZfpmeSB74YtD331)"
      ],
      "metadata": {
        "id": "rdqd6y9sC7zD"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Results (in brief)**\n",
        "\n",
        "Asia experienced a spike in new outbreaks around 2022, coupled by an increase in cases and vaccinated. There was an inexplicably high slaughter rate in Africa that same year, despite the lack of new FWD cases on the continent. Counts\n",
        "were low across Europe and the Americas.\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1CKTJVX-taw5N0PAMC7qHsUV3NNQr8xjJ)\n",
        "\n",
        "\n",
        "The top 5 highest slaughtering count events in the dataset occurred in South Africa between 2021-2022.\n",
        "\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1-0jQr56Jgou70rgFkQEwXzV57dBFGZny)\n",
        "\n",
        "\n",
        "Baselining provides a different outlook on the data as trends in Europe and America become visible. There was a very clear spike in 'cases' and 'killed and disposed of' in Europe\n",
        "\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1CKTJVX-taw5N0PAMC7qHsUV3NNQr8xjJ)\n",
        "\n",
        "\n",
        "Some variables are strongly correlated within world regions.'Cases' and 'killed and disposed of are perfectly positively correlated in Europe, as was indicative from the baselined time-series plot,\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1zmud3qE-K764Xiyc9cUy1lqM4BPrtq86)\n",
        "\n",
        "A linear regression model revealed the 'case' count predicts 99.8% of variance in 'killed and disposed of' in Europe. In other words, the 3 European countries that have reported FMD outbreaks in the past 20 years have dealt with the outbreaks through culling en-masse.\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1-8VmFZr2jAMQYo-PnWEPitq6BvvkuZrQ)\n",
        "\n",
        "Choropleth maps provide a nice persective on trends across neighbouring countries. For example, most outbreaks are occuring across neighbouring Asian countries.\n",
        "\n",
        "![link text](https://drive.google.com/uc?id=1s6d97Kls5Z6U7svjdJETS0GD410TWjgw)\n",
        "\n"
      ],
      "metadata": {
        "id": "oaMx_7mG4hHQ"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Discussion**\n",
        "\n",
        "Some of the main take-home points are:\n",
        "\n",
        "\n",
        "* The majority of FMD cases and outbreaks occur in Asia.\n",
        "* The inexplicably high slaughtering count in South Africa could be followed up on.\n",
        "* European countries have dealt with FMD outbreaks through mass culling.\n",
        "\n",
        "\n"
      ],
      "metadata": {
        "id": "sENhhtW3EWLy"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Limitations**\n",
        "\n",
        "More data is required to perform more advanced regression analyses. A random forest model using 'Susceptible' and 'Vaccinated' as features and 'New outbreaks' as a predictor yielded an r squared value of .46. Additional variables such as 'flock count' could improve the model's accuracy."
      ],
      "metadata": {
        "id": "QCw0o0sRFpEB"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "**Datasets: raw, cleaned, grouped**\n",
        "\n",
        "The raw dataset was sourced from the WOAH's animal information system\n",
        " at https://wahis.woah.org/#/dashboards/qd-dashboard.\n",
        "\n",
        "[Clean data](https://drive.google.com/file/d/1_7HGF96LRCa3UUsiVRKSwSh6lf4mswRV/view?usp=drive_link)\n",
        "\n",
        "[Data summed and grouped by world region for time-series ploting](https://drive.google.com/file/d/1EG-H1wYbE5k1kQ1nsgEmhity_JAHODQK/view?usp=sharing)\n",
        "\n",
        "[Data summed and grouped by country for choropleth maps](https://drive.google.com/file/d/1hHRCTFCBasPDwvNNhQSMXMGOKVBAUt50/view?usp=sharing)"
      ],
      "metadata": {
        "id": "-1Y7e33ZLqzt"
      }
    }
  ]
}