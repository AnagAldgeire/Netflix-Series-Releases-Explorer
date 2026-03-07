# Netflix Series Releases Explorer

#### 🔗 Interactive visualization: https://anagaldgeire.github.io/Netflix-Series-Releases-Explorer/DataViz-Netflix.html

#### 📊 Dataset (CSV version used for this project): https://docs.google.com/spreadsheets/d/e/2PACX-1vToADOwlxU25FIlsv2VLQ0oQcmi6tQtW3wA99gW0MQNBbTq0Vv6_CeJA6rJKLgySw/pub?gid=1159166045&single=true&output=csv

## Project Overview

The Netflix Series Releases Explorer is an interactive data visualization system designed to explore patterns in Netflix series releases over time and around the world. The project focuses on identifying trends in genre distribution and production types among TV series available on the platform.

The visualization was developed using a modified dataset derived from the **Netflix Movies and TV Shows** dataset created by **@Arpita-deb**.
Original dataset repository available in this link: https://github.com/Arpita-deb/netflix-movies-and-tv-shows

## Original Dataset

The original dataset compiled by **Arpita Deb** contains metadata about titles available on Netflix, including both movies and TV series. The dataset aggregates information from publicly available sources such as IMDb and other online film and television databases.

Key characteristics of the dataset include:

- Covers Netflix titles up until May 2022 (limitation: it doesn't reflect most current contents and trends).
- Includes both Netflix Original productions and acquired titles.
- Contains information on movies and TV series, however it does not cover the entire contents of Netflix.
- Provides metadata such as: Title; Type (movie or show); Release year; Genre; IMDb ratings; Runtime; Country of production; Age certification; IMDb identifiers

This dataset serves as the starting point for the visualization system presented in this project.

## Dataset Modifications

For the purpose of this visualization, several transformations and filters were applied to the original dataset.
- Only entries classified as TV Shows were kept.
- Only series with a release year from 2010 onward were included, corresponding to the period in which Netflix began expanding its streaming platform and original content strategy.
- The following columns from the original dataset were not used in this project: age-certification, IMDb votes, IMDb score, Index, Runtime, ID


Also, the original genre column was reorganized into a two-level classification system:

**Genre (main category):**
- Fiction
- Factual
- Entertainment

**Subgenre:**
- Documentary
- Animation
- Drama
- Comedy
- Reality
- Reality Competition
- Talk Show
- Stand Up
- Game Show

This classification was created by detecting keywords already present in the dataset, such as "drama", "animation", "comedy", "documentation", and "reality".

In some cases, manual adjustments were necessary, as the original dataset could contain broad classifications (for example, simply “reality”) while the content more accurately corresponded to a more specific subgenre such as reality competition or game show.

⚠️ Because of the scale of the dataset and the semi-manual classification process, some classification errors may still exist.

## Data Cleaning

- Series titles that were not written in English and lacked sufficient metadata (such as IMDb references, genre information, or country data) were removed to ensure consistent classification.
- The Title column was standardized to uppercase for visual consistency.
- The Country column was converted from country codes to full country names.
- The IMDb ID column was converted into the full IMDb URL.

## Notes
This project is intended primarily as an exploratory data visualization exercise. While efforts were made to clean and standardize the dataset, the transformations described above may introduce minor inconsistencies.

Users should therefore treat the dataset as an analytical approximation rather than a definitive catalog of Netflix releases.
