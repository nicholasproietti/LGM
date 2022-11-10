# PHYS 549 Group Project: Estimating exoplanet radii with Kepler light curves
**Authors:  Bolu Feng, Nick Proietti, Deekshit Vedula**
<br/>
**Team Name: Little Green Men (LGM)**
<br/>
<br/>
This repository is a shared workspace for the PHYS 549 group project by LGM. The goal of this project is to establish a link between
light curve features in existing data collected by the *Kepler* mission and exoplanet radii estimates through neural networks.

## Regression analysis of exoplanet radii using neural networks
### Required files
1. KIC_FIRST_100.csv
2. KOI.csv


LC_FFT_CNN is the file in which we are trying to remove dominat frequencies from the LC and train it using a CNN (In progress)

XGB_Kepler is the file in which we have used a XGB Regressor to train using KOI parameters to predict exoplanet radius
