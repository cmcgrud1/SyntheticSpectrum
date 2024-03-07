# SyntheticSpectrum

Jupyter notebook is used to create synthetic data, complete with chromatic (wavelength dependent) noise, non-chromatic noise, and white-light noise. 
The systematic noise was created by randomly drawing from a GP distribution, where the GP was constructed to be correlated to auxiliary parameters (airmass, fwhm, sky flux, etc.).
500 of these synthetic data were then tested against two detrending techniques: PCA+GP (see https://ui.adsabs.harvard.edu/abs/2020A%26A...642A..98Y/abstract) and CMC+Polynomial regression (see https://github.com/cmcgrud1/TransSpecDetrend).

This is the basis for the work done in McGruder et. al. 2022 (https://ui.adsabs.harvard.edu/abs/2022AJ....164..134M/abstract), in which
We used this technique to determine the most appropriate detrending approach for specific data sets.

NOTE: The code for running the statistical tests on the synesthetic data will be posted in the future (currently on a hard drive in Cambridge, MA).  

Packages required (outside of standard anaconda):

batman - https://lkreidberg.github.io/batman/docs/html/index.html

george - https://george.readthedocs.io/en/latest/tutorials/first/

ldtk - https://github.com/hpparvi/ldtk/blob/master/README.md

ext_func - internal package used to create transit light curve models, with the quadratic limb darkening law. The directory contains a fast Mandel & Agol code implemented in Python/C 
