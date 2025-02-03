# Description: This is my work on the final course project 'Machine Learning for Scientists'

### Project: Using Machine Learning to Predict the properties of Galaxies from their Spectral Energy Distribution (SED)
### Author: Vishal Verma


### Course: Machine Learning for Scientists
### Course Instructor: Viviana Acquaviva

Aim: To use machine learning to analyze the spectral energy distribution of 2000 galaxies and predict four key properties - Stellar Mass, Amount of Dust, Age and Tau (a parameter related to star formation rate).

The Dataset: Is a simulated dataset of 2000 galaxies each of which are at a redshift of z=1 (corresponding to a time 5 billion years ago). The wavelength range of the spectra is between 1000 - 100,000 Angstroms. Therefore this dataset encompasses most of the EM radiation in the UV-Infrared. We have measurements for 2000 wavelengths in the mentioned range which are spaced logarithmically, meaning the points closer to 1000 angstroms are more close packed compared to points closer to 100,000 angstroms if we were to plot them on a linear scale. This is well suited for our purposes since most of the important information is in the smaller wavelengths. The input features include flux measurements (in MicroJansky) at these wavelengths. This is a supervised regression learning problem as we have learning data on the four parameters (stellar mass, amount of dust, age and tau) that we are trying to predict.

Units: 

Input Features: Wavelenghts (Angstrom), Flux (microJansky)
Output Features: Stellar Mass (log Solar Masses), Amount of Dust (Magnitude of Obscuration), Age (Gyr) and Tau (Gyr)

Machine Learning Algorithm Used: Random Forests (RF)

Motivation for picking this algorithm:
    
1. Extremely robust and powerful algorithm for a regression problem like this one.
2. Intrinsically build to avoid overfitting and reduce variance by bootstrapping and selecting a random number of features to split at each node.
3. Easy to interpret and vary the hyperparameters for optimization.



Method: We will evaluate each of these 4 parameters individually using Random Forests.