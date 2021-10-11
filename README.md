# README for DATA 512 A2 Project

## Goal
The goal of this project is to explore potential bias in Wikipedia articles of politicians by country. We're interested in finding out whether a country's population size has any relationship with the quality and coverage of its politicians' articles. 

To understand the results of the analysis, it's important to know how we define a "quality" article. Wikipedia articles have 6 different levels of quality:
* FA - Featured article
* GA - Good article
* B - B-class article
* C - C-class article
* Start - Start-class article
* Stub - Stub-class article

For our purposes we're considering "FA" and "GA" articles to be high quality. Given that definition, these are the metrics that we'll compare to country population:

* __Coverage__: High quality articles per population = (Number of FA or GA articles) / (Population)
* __Relative Quality__: Proportion of high quality articles = (Number of FA or GA articles) / (Number of total articles)

## Source data descriptions
Wikipedia data on politicians by country is from Figshare, and is available at this link with documentation: [politicians by country dataset](https://figshare.com/articles/dataset/Untitled_Item/5513449)

Data on world populations is published by the Population Reference Bureau. 
* Data is available [here](https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit#gid=283125346)
* Documentation and more information about the Population Reference Bureau is available [here](https://www.prb.org/international/indicator/population/table/)

Article quality predictions are pulled from the ORES REST API. See below for API documentation
* API documentation is available [here](https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context_revid_model)

## Reproducing this analysis using hcds-a2-bias.ipynb
This repository contains everything needed to reproduce this analysis. Using the source data listed above (which is also included in the repo), the juputer notebook hcds-a2-bias.ipynb will produce a combined dataset (described below) and 6 tables comparing the top and bottom ranked countries and regions by article coverage and relative quality.

## Column descriptions and provenance for the data generated in this analysis in wp_wpds_politicians_by_country.csv
* __country__: Country of the politician in the article, common to both the Wikipedia and World Population data
* __article_name__: Name of the politician the article is written about, from the Wikipedia data
* __revision_id__: The unique ID for the Wikipedia article, common to both the Wikipedia and ORES API data
* __article_quality_est.__: The quality estimate for the article pulled from the ORES API
* __population__: Population size for the country from the World Population data

## Writeup
Before starting this analysis, I expected 

What I encountered was

When would this still be useful, despite limitations