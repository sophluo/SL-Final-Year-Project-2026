This repository contains Jupyter notebooks with analysis for the final year project: "Modelling the tropospheric oxidising capacity of the hydroxyl ($OH$) radical using zero-dimensional box modelling and machine learning approaches."

**Background:**

The NASA Atmospheric Tomography (ATom) missions were a global-scale airborne campaign that took place between 2016 and 2018, targeting remote areas of the troposphere. It provided a range of in-situ measurements of key atmospheric species. This project focuses on the ATom-1 mission, which took place between June and August 2016. More information can be found [here](https://doi.org/10.1175/BAMS-D-20-0315.1).

The gas-phase hydroxyl ($OH$) radical is of particular importance and research interest due to its ability to react with (hence removing) pollutants such as $CO$ from the troposphere. Due to its short lifetime (~1 s), a steady-state approximation can be employed in which its source and sink (chemical production and loss) rates can be used to approximate $[OH]$:

$[OH]_{ss}=\frac{2k_1[O(^1D)][H_2O]}{k_2[CO]+k_3[CH_4]}$

This project aims to use the data from the ATom missions to model $[OH]$ and compare this with the measured $[OH]$. It will also use an alternative data-driven approach of machine learning, using the same set of features to compare with the box modelling approach. 

There are four notebooks:
- `ATom-1 updated box model - minimal.ipynb`: code for the box model with a minimal set of inputs. This corresponds to Section 8.1 in the report.
- `ATom-1 updated box model - with HOx and NOx reactions.ipynb`: extension of box model to include HOx and NOx chemistry. This corresponds to Section 9.3 in the report.
- `Machine learning`: code for the machine learning regression models. This corresponds to Section 10.1 in the report.
- `Machine learning - random split`: code that does a random train/test split as well as grid search for optimum hyperparameters. This corresponds to Section 10.2 in the report.

There are two `.csv` files:
- `MDS_atom1_2016_summer_with_no_no2_oh_ho2_full_js.csv` is the dataset containing measurements for the construction of the box model.
- `box_model_output.csv` contains pre-processed data from the file above as well as the outputs ($[OH]$) for the box model with a minimal set of input. This file is used for the machine learning approaches.

**How to run the code:**

Please run all cells to run the box model calculations and view the results. The first part of the box model notebooks is performing the appropriate calculations using rate constants and concentrations of various atmospheric species to find a steady-state approximation of $[OH]$; this is then followed by the plots used in the report, that visualise the results and compare with the ATom-1 measurement of $[OH]$.

<<<<<<< HEAD
For the machine learning notebooks, the box model output is read in as the pre-processed `.csv` file to save re-calculating $[OH]$ multiple times.
=======
For the machine learning notebooks, the box model output is read in as the pre-processed `.csv` file to save re-calculating $[OH]$ multiple times
>>>>>>> 9977db5c3e87895d707eaf3429ed816391f292ce
