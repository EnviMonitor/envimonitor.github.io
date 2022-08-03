---
layout: page
---

## PERK

`PERK` – an [R][R] package with in-built application to predict and visualize environmental concentration and risk using pharmaceutical prescription data collected at fine spatial resolution 

Recent scientific advancements enabled us to identify and quantify a wide range of pharmaceutical drugs in the natural environment and helped us to evaluate their impacts on exposed aquatic environmental species and humans [1, 2]. However, quantification of several pharmaceutical drugs is still very limited, partly because of the limitations in analytical method development.  

Predicting these pharmaceuticals’ environmental concentrations using different modelling approaches is an important aspect in the assessment of their environmental risk. Specific guidelines were developed and issued by European Agency for the Evaluation of Medicinal Products and United States Food and Drug Administration for predicted environmental concentration (PEC) of pharmaceuticals for human use in different environmental matrices [3-5]. These guidelines help to prioritise the risk from drugs that are already in use and calculate the potential impact of a new pharmaceutical drugs may have on the environment once released. 

PERK acronym for Predicting Environmental concentrations and RisK assessment, is an R package with in-built application tool, aims to facilitate automated modelling and reporting of predicted environmental concentrations of a comprehensive set of pharmaceuticals derived from a wide range of therapeutic classes with different mode of action.  

The tool helps users to input their measured concentration, to compare the predicted and measured concentrations of the APIs by means of the PEC/MEC ratio, to establish whether the predicted equations used tend to underestimate or overestimate measured values [6]. 

It provides a consistent interactive user interface in a familiar dashboard layout, enabling users to visualise predicted values and compare with their measured values without any hassles. Users can download data and graphs generated using the tool in .csv or publication ready images. 

## Data sources: 

### Prescription Data 

For England, the tool uses the prescription data from PrAna7, an R package to calculate and visualize England NHS prescribing data. The data used in PrAna are as follows, 

- [**Prescribing data and Practice information**][NHS digital] are from the monthly files published by the [NHS Business Service Authority][NHSBSA], used under the terms of the Open Government Licence. 

- **BNF codes and names** are also from the NHS Business Service Authority's Information Portal, used under the terms of the Open Government Licence. 

- [**dm+d weekly release data**][dm+d] is also from the NHS Business Service Authority's Information Portal, used under the terms of the Open Government Licence. 

### WWTP Data 

The following dataset are provided from WWTP collaborators, 

- **Catchment map** used to define the boundaries and capture the GP Practices inside the catchments for the prescription data calculations. 

- **Daily flow data** used to calculate the load and population equivalent. 

- **Population Equivalent** i.e., number of inhabitants per catchment zone. 

- **Site information** required to predict information such as recovery percentage. 

- **Water quality** parameters to predict population equivalent. 

### API properties 

- **Metabolites and Excretion factors** collected from literatures and data repositories such as Drug bank. 

- **Recovery percentage** collected from literatures, calculated from measured concentration from previous experiments, predicted using WWTP site information. 

- **Physiochemical properties** collected from literatures and data repositories. 

- **Ecotoxicity data** collected from literatures and data repositories. 

## Acknowledgments: 

This work is a part of the Wastewater Fingerprinting for Public Health Assessment (ENTRUST) project funded by Wessex Water and EPSRC IAA (grant no. EP/R51164X/1). 

## References: 

1.	Webb, S.;  Ternes, T.;  Gibert, M.; Olejniczak, K., Indirect human exposure to pharmaceuticals via drinking water. Toxicology Letters 2003, 142 (3), 157-167. 
2.	Crane, M.;  Watts, C.; Boucard, T., Chronic aquatic environmental risks from exposure to human pharmaceuticals. Science of The Total Environment 2006, 367 (1), 23-41. 
3.	(EMA), E. M. A. Guideline On The Environmental Risk Assessment Of Medicinal Products For Human Use EMEA/CHMP/SWP/4447/00 corr 2 2006, p. 1-12. https://www.ema.europa.eu/documents/scientific-guideline/guideline-environmental-risk-assessment-medicinal-products-human-use-first-version_en.pdf (accessed May 30, 2019). 
4.	(EMA), E. M. A. Environmental risk assessment of medicinal products for human use draft EMEA/CHMP/SWP/4447/00 Rev. 1 2018, p. 1-48. https://www.ema.europa.eu/documents/scientific-guideline/draft-guideline-environmental-risk-assessment-medicinal-products-human-use-revision-1_en.pdf (accessed September 13, 2021). 
5.	Administration, U. S. F. a. D. Guidance for industry: Environmental assessment of human drug and biologics applications. CMC 6. Revision 1. 1998. https://www.fda.gov/down loads/Drugs/Guidances/ucm070561.pdf. (accessed September 13, 2021). 
6.	He, K.;  Borthwick, A. G.;  Lin, Y.;  Li, Y.;  Fu, J.;  Wong, Y.; Liu, W., Sale-based estimation of pharmaceutical concentrations and associated environmental risk in the Japanese wastewater system. Environment International 2020, 139, 105690. 
7.	Kishore Kumar, J.;  James, G.;  Sue, G.;  Ruth, B.; Barbara, K.-H., BMC Medical Informatics and Decision Making 2021. 


## Disclaimer
We accept no liability for any errors in the data or its publication here: use this data at your own risk. You should not use this data to make individual prescribing decisions.

[R]: https://www.r-project.org/
[NHS digital]: https://digital.nhs.uk/organisation-data-service/data-downloads/gp-data
[NHSBSA]: https://applications.nhsbsa.nhs.uk/infosystems/welcome
[dm+d]: https://isd.digital.nhs.uk/trud3/user/guest/group/0/pack/6
