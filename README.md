# PHYS 549 Group Project: Estimating exoplanet radii with Kepler light curves
**Authors:  Bolu Feng, Nick Proietti, Deekshit Vedula**
<br/>
**Team Name: Little Green Men (LGM)**
<br/>
<br/>
This repository is a shared workspace for the PHYS 549 group project at Rice University by LGM. The goal of this project is to link
light curve features, exoplanet, and host star parameters in existing data collected by the *Kepler* mission with exoplanet radii estimates through regression using neural networks.

<p float="left">
  <img src="README_figures/cheops-transit-method.gif" width="340" />
  <img src="README_figures/Kepler.png" width="400" /> 
</p>

*Left*: A basic picture of the exoplanet transit method (Source: *The Planetary Society*). *Right*: Kepler Space Telescope (Source: *NASA*).

## Project Overview

For millennia, our solar system was the only known example of planets orbiting
a central star. The very idea of planets around other stars, or extrasolar planets
for short, would have changed the worldviews of many people throughout history.
Yet in 1992, the discovery of worlds outside our solar system, exoplanets,
have revolutionized the field of astronomy. Also known as extrasolar planets,
these bodies often orbit their stars with some being a part of entire planetary
systems. This revolution is now in full bloom, with new discoveries coming at a
rapid pace. The advancing science of extrasolar planets has dramatic implications
for our understanding of our place in the universe. The fact that planets
are common in the universe makes it seem more likely that we might someday
find life elsewhere, perhaps even intelligent life. Moreover, having many more
worlds to compare to our own vastly enhances our ability to learn how planets
work, which may help us better understand our home planet, Earth. It also
allows us to test the nebular theory of solar system formation in new settings.

However, we would like to learn more about these planets other than confirming
their existence. We would like to learn about the nature of these planets.
Our project focuses on learning the sizes, or radii, of existing exoplanet data
collected by the Kepler mission. By using Fourier transforms, neural networks,
and Kepler information about known exoplanets, we will analyze these signals
of exoplanetary systems, known as light curves, to unlock essential properties of
exoplanets, specifically by establishing a link between light curve features and
radii and constructing a distribution of their radii, and ultimately contribute
to the characterization of exoplanet demographics (e.g. are they Jupiter-like?
Earth-like? etc.).

### Main Codes
`LC_FFT_CNN` is the file in which we are trying to remove dominant frequencies from the LC and train it using a convolutional neural network (In progress)

`XGB_Kepler` is the file in which we have used an XGB Regressor to train using KOI parameters to predict exoplanet radius

`Light_Curve_Simulation` is the file in which we are trying to simulate an exoplanet transit light curve in Progress

`KOI_Regression.ipynb` - Illustrates the results of exoplanet radii predictions from the Kepler Object of Interest (KOI) table parameters using an MLP regressor

## Data used 
The KOI table can be found on the [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=cumulative), in addition to the [glossary for the data columns](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html). `data/KOI.csv` describes the current results of different searches of the Kepler light curves as of Sept. 27, 2018. `data/KOI_first_100.csv` describes the first 100 rows of `CANDIDATE` sources from the KOI table.
 
The Kepler light curves may be retrieved in several ways. For this project, the Kepler light curve data was formerly acquired through the [Mikulski Archive for Space Telescopes (MAST)](https://stdatu.stsci.edu/k2/data_search/search.php) and is currently acquired through the [lightkurve package](https://docs.lightkurve.org/). *lightkurve* offers a user-friendly way to analyze time series data on the brightness of planets, stars, and galaxies. The package is focused on supporting science with NASA’s Kepler and TESS space telescopes.

