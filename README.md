
# Project: Using Random Forests Algorithm in Machine Learning to predict the properties of Galaxies from their Spectral Energy Distribution (SED)
### Author: Vishal Verma

### Description: This is my final project for the course'Machine Learning for Scientists'

### Course: Machine Learning for Scientists
### Course Instructor: Viviana Acquaviva

**Aim: To use machine learning to analyze the spectral energy distribution of 2000 galaxies and predict four key properties - Stellar Mass, Amount of Dust, Age and Tau (a parameter related to star formation rate).**

**The Dataset: Is a simulated dataset of 2000 galaxies**** each of which are at a redshift of z=1 (corresponding to a time 5 billion years ago). The wavelength range of the spectra is between 1000 - 100,000 Angstroms. Therefore this dataset encompasses most of the EM radiation in the UV-Infrared. We have measurements for **2000 wavelengths** in the mentioned range which are spaced logarithmically, meaning the points closer to 1000 angstroms are more close packed compared to points closer to 100,000 angstroms if we were to plot them on a linear scale. This is well suited for our purposes since most of the important information is in the smaller wavelengths. The input features include flux measurements (in MicroJansky) at these wavelengths. **This is a supervised regression learning problem as we have learning data on the four parameters (stellar mass, amount of dust, age and tau) that we are trying to predict.**

Units: 

Input Features: Wavelenghts (Angstrom), Flux (microJansky)

Output Features: Stellar Mass (log Solar Masses), Amount of Dust (Magnitude of Obscuration), Age (Gyr) and Tau (Gyr)

### Machine Learning Algorithm Used: Random Forests (RF)

### Motivation for picking this algorithm:
    
**1. Extremely robust and powerful algorithm for a regression problem like this one.
2. Intrinsically build to avoid overfitting and reduce variance by bootstrapping and selecting a random number of features to split at each node.
3. Easy to interpret and vary the hyperparameters for optimization.**

Method: We will evaluate each of these 4 parameters individually using Random Forests.

### Key Results

1. Using the mean of every ten features reduced the dataset size by a factor of 10 while still preserving the results.

2. The algorithm worked great for estimating the Amount of Dust and Stellar Mass (Test Scores 0.978 and 0.935 respectively)
   
3. For Age and Tau the test scores were poor (0.057 and 0.076 respectively)

4. Feature Engineering (by working with the logarithms of Age and Tau) had a great effect on the test scores (Improved to 0.696 and 0.619 respectively) thus highlighting the importance of this step.

### Further Improvements for Future

1. Test Scores and Variance issues for Tau and Age can still be improved, perhaps adding more Data can further improve results by about 10%.

2. We could also explore other Machine Learning algorithms. Would be interesting to try SVM and boosting methods on the same problem and then finally Neural Networks as well. Lasso Regression also seems like a good idea for this problem because of the large number of features and Lasso's inherent ability to set the coefficients of uninmportant features to zero.






