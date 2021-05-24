# firearmStats

This repository contains data, its transformation and exploration in terms of firearm ownership rates, firearm and police death rates and freedom indices per country for 2017. The goal with this little project is to search for potential global trends that relate firearm ownership, violence and personal freedom. The analysis is strictly descriptive, as the data, in the format used, is too diverse to grant any robust modeling. However, the simple bar and scatter plots and correlation heatmaps still help us answer the main questions posed:

- Is there evidence for correlation between the firearm and police death rates with firearm ownership rates? - *Short answer: NO.*
- Are there trends in the death rates by firearm and police with respect to how developed a country is? - *We find that three "freedom index" groups can be distringuished in terms of the range of recorded rates, with the US being a strong outlier among high-freedom index countries.*
- Does firearm ownership grant more personal freedom? - *The data does not show significant correlation between firearm ownership and freedom indices. However, some interesting insights are made regarding the US, which prompt further analysis.*

The raw data sets used can be found in raw_data/ and include the follwing:
- IHME-GBD data set - the data set is generated using the GBD Results tool, (citation: Global Burden of Disease Collaborative Network. Global Burden of Disease Study 2019 (GBD 2019) Results. Seattle, United States: Institute for Health Metrics and Evaluation (IHME), 2020. Available from http://ghdx.healthdata.org/gbd-results-tool.). Contains firearm-related, police-related and other death rates per country, per year for years 2013-2019, grouped by age group, sex and cause.
- global gun ownership - downloaded from Wikipedia https://en.wikipedia.org/wiki/Gun_ownership / the Small Arms Survey for 2017
- freedom index - data from the latest report of the Cato Institute, downloaded from Kaggle https://www.kaggle.com/gsutters/the-human-freedom-index?select=hfi_cc_2020.csv (most recent year available in the data set is 2017)

These are transformed into the project_data/ set which contains rates and values from each dataset for 2017, transformed such that each country has a unique country code and value per column.

All code is contained in the firearmStats_world notebook, which requires
- numpy
- pandas
- matplotlib
- seaborn
- itertools
for successful execution.
