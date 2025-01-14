---
layout: page
---

<!-- badges: start -->
  [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
  [![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
  [![CRAN status](https://www.r-pkg.org/badges/version/PrAna)](https://CRAN.R-project.org/package=PrAna)
<!-- badges: end -->
  
# PrAna

[`PrAna`](https://pranaviz.github.io/) aims to aggregate and normalise England’s national level prescription data, for all groups of drugs. The name is an acronym for _**Pr**escription **Ana**lysis_

## Background

During the last decade, wide range of **active pharmaceutical ingredients (APIs)** have been identified and quantified in aquatic environment across several studies and indicated their impacts on exposed environmental species and humans. For the prediction of total amount of the APIs released to the environment, information about APIs consumption data is vital. Globally, several methods were reported to estimate the APIs consumption data based on the national prescription data, manufacturers, importers and dispenser’s data.

In the UK, national prescription data provided by [National Health Service][NHS digital] was used to calculate the consumption data. This data is freely accessible and consist of individual files for each month. With the large file with over 10 million records every month, the data from the NHS cannot be used for the direct calculation of the prescription levels of different APIs. Re-organisation and processing of the files is required before to do any exploration or analysis and to speed up the data reading. 

The aim of `PrAna` is to aggregate and normalize prescription data to calculate total prescribed quantity of different APIs, using open source statistical software [R language][@R-base]. 

Apart, from the calculation of the total prescribed quantity of an API or a group of APIs, specified to a postcode or region, We have also developed, _an open interactive web-based tool_, `PrAnaViz` with the processed dataset for the period `2015` to `2019`.

`PrAnaViz` facilitates users **to visualise, explore and report** different spatiotemporal and long-term prescription trends for wider use. 


## Workflow

Below is an overview of the workflow:

- **Data Preparation**: Download monthly [NHS prescription datasets][NHSBSA] and Dictionary of medicines and devices release files [(dm+d)][dm+d].
- **Data Conversion**: Aggregation and conversion of the locally stored datasets into practice wise dataset achieved using the functions in `PrAna`.
- **Visualise and Analyse the data**: Visualise and analyse the processed dataset using the in-built ShinyApp `PrAnaViz`.
- **Database service**: Linking of the processed dataset to the `PrAnaViz` can be achieved by uploading the processed dataset to a local or a remote database service, for example, [_MySQL._][MySQL]
- **Download images and processed data**: Users can download processed data as **_.csv_** file and publication ready image **_.eps_** and **_.pdf_** files.

## Data sources

- Prescribing data and Practice information are from the monthly files published by the [NHS Business Service Authority][NHSBSA], used under the terms of the Open Government Licence.
- BNF codes and names are also from the [NHS Business Service Authority's Information Portal][NHSBSA], used under the terms of the Open Government Licence.
- [dm+d weekly release data][dm+d] is also from the NHS Business Service Authority's Information Portal, used under the terms of the Open Government Licence.


## Get this package

`PrAna` can be installed as any other R package, as follows,

To install the development version of PrAna from GitHub:
```
install.packages("devtools")
library(devtools)
install_github("jkkishore85/PrAna")
```
However, since it is dependent on some other software tools some extra steps are required for the installation. Please see the installation section in the handbook <!--[handbook-inst] -->for more information.

However, for a better guide to get started it is recommended to read the tutorial. <!--]  [tutorial].-->

<!--
## Shiny App Docker
A R Shiny application that allows you to generate and visualise prescription data genereated using PrAna.

### Run App locally in Docker container
To run the app in an isolated environment install docker here. Then navigate to project root directory and build the container image by executing the following in you CLI:

```
docker build -t my-shinyapp-image . 
```
This might take a couple of minutes. After the image is build start the container by running:

```
docker run -d --name my-shiny-app -p 3838:3838 my-shinyapp-image
```

Open a browser and enter localhost:3838 to access the app.

### Stop the App
To stop the container enter:
```
docker stop my-shiny-app
```
If you want to delete the container execute:
```
docker rm my-shiny-app -f
```
--> 
## Acknowledgements

This package was built as a part of the **Wastewater Fingerprinting for Public Health Assessment (ENTRUST)** project funded by **University of Bath**, **Wessex Water** and **EPSRC IAA** _(grant no. EP/R51164X/1)_. 

## Disclaimer
We accept no liability for any errors in the data or its publication here: use this data at your own risk. You should not use this data to make individual prescribing decisions.

[R]: https://www.r-project.org/
<!--[tutorial]: https://kishorejagadeesan.com/PrAna/handbook_bd/pranaviz.html -->
[NHS digital]: https://digital.nhs.uk/organisation-data-service/data-downloads/gp-data
<!--[handbook-inst]: https://kishorejagadeesan.com/PrAna/handbook_bd/install.html -->
[NHSBSA]: https://applications.nhsbsa.nhs.uk/infosystems/welcome
[dm+d]: https://isd.digital.nhs.uk/trud3/user/guest/group/0/pack/6
[dm+d2]: https://isd.digital.nhs.uk/trud3/user/guest/group/0/pack/6/subpack/239/releases
[MySQL]: https://www.mysql.com/
