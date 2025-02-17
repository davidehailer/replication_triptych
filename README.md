# Replication package for "Evaluating Probabilistic Classifiers: The Triptych"

Timo Dimitriadis and Alexander I. Jordan

## Overview & contents

The code in this replication material generates the 13 figures and 2 tables for
the paper "Evaluating Probabilistic Classifiers: The Triptych".
Each figure is generated separately by its corresponding script file
`Figure[xx]*.R`.

The main contents of the repository are the following:

- `R/`: folder of R code containing the triptych functions
- `plots/`: folder of generated plots as PDF files
- `data-raw/`: folder of raw data files and the functions for processing them
- `data/`: folder of processed data files
- `Figure[xx]*.R`: R scripts to create the respective figures


The content of Tables 1 and 2 is printed to the console by running
`Figure_01_Triptych_C1Flares.R` and the content of Table 3 is obtained by running
`Figure_10_Triptych_SPF.R`.


## Data availability and provenance

### Solar Flare Forecasts

The prepared forecast-observation data are located at `data/C1_flares.rda` and `data/M1_flares.rda`, for the classes C1.0+ and M1.0+ of solar flare intensity. These files are generated by the script `data-raw/prepare_SolarFlares.R` using the pre-processed data files `SF.FC.C1.rda` and `SF.FC.M1.rda` from Dimitriadis and Jordan (2021, https://doi.org/10.5281/zenodo.4699945). That replication package contains a description of the pre-processing of the original data on solar flares from Leka and Park (2019, https://doi.org/10.7910/DVN/HYP74O).


### SPF Forecasts for Economic Recessions

The prepared forecast-observation data are located at `data/spf.gpd.long.rda`. They are also available from Dimitriadis and Jordan (2021, https://doi.org/10.5281/zenodo.4699945), a replication package that contains a description of the pre-processing of the original data from the Federal Reserve Bank of Philadelphia (https://www.philadelphiafed.org/surveys-and-data/).


### Fragile Family Challenge

The Fragile Family Challenge (FFC) is a scientific mass collaboration where 160
teams built predictions for six variables, where we analyze two binary ones (eviction and
job training). The prepared forecast and outcome data are located in the `data/` folder, as files `FFC_Eviction.rda` and `FFC_JobTraining.rda`.

The forecasts (submissions) of the 160 teams together with the
realizations originate from Salganik et al (2020, https://doi.org/10.7910/DVN/CXSECU), located in the `data/derived/submissions.csv.zip` file. The 9 benchmark forecasts have to be generated separately by obtaining data files from
https://opr.princeton.edu/archive/ as described in Salganik et al (2020).
We prepare the FFC data using these two (in this repository unavailable) files within the script `prepare_FragileFamilyChallenge.R`.


## Instructions & computational requirements.

The analysis files `Figure[xx]*.R` can be run individually, in any order. Set the working
directory to the root of the replication package, or open the `.Rproj` file
using RStudio.

The software versions that were used to run these analyses are

- R 4.2.2
  - `geomtextpath` (0.1.1)
  - `ggrepel` (0.9.2)
  - `murphydiagram` (0.12.2)
  - `lubridate` (1.9.0)
  - `patchwork` (1.1.2)
  - `pROC` (1.18.0)
  - `readr` (2.1.3)
  - `reliabilitydiag` (0.2.1)
  - `dplyr` (1.0.10)
  - `tidyr` (1.2.1)
  - `ggplot2` (3.4.0)
  - `stringr` (1.5.0)
  - `calibrationband` (0.2.1)

For a convenient package setup in a (local) R session, use the `checkpoint` package (https://cran.r-project.org/package=checkpoint) with the command `checkpoint("2023-01-23")` (or source the file `checkpoint.R`) before running any of the analysis scripts.

## References

Dimitriadis T, Jordan AI. 2021. Replication package for "Stable reliability diagrams for probabilistic classifiers" (v1.0.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.4699946

Leka KD, Park S. 2019. A Comparison of Flare Forecasting Methods II: Data and Supporting Code. Harvard Dataverse, V1, UNF:6:yz1noMojlzL7SZM+9flXhQ== [fileUNF]. https://doi.org/10.7910/DVN/HYP74O

Salganik M, Lundberg I, Kindel A, McLanahan S. 2020. Replication materials for "Measuring the predictability of life outcomes using a scientific mass collaboration". Harvard Dataverse, V3, UNF:6:Cj8wiioSf8JGyRLcDo5d3w== [fileUNF]. https://doi.org/10.7910/DVN/CXSECU
