# Hot-Lapper

This project aims to implement an automated machine learning system capable of predicting an F1 driver's lap sector time by automating the full machine learning process: data cleaning and analysis, model tuning, and feature and model selection.


More specifically, the user is able to input a set of: 
* Lap Sectors 
    * Sector 1, Sector 2, Sector 3 or Full Lap
* F1 Drivers
* Event Sessions
    * Free Practice 1, Free Practice 2, Free Practice 3, Qualifying or Race
* Grand Prixs
* Years

The system will perform EDA and develop a predictive model for each inputted sector, for each inputted driver, for each inputted event session, for each inputted Grand Prix for each inputted year.


## Running 
Input your desired values using the variables with the SELECTED_EXPERIMENT title and simply run the Jupyter Notebook!


## Installation
Use Python 3.12.5 and create a virtual environment. Then, run the below command to install the necessary packages:

```
pip install -r requirements.txt
```

#### Possible Errors

If you're on Mac OS, XGBoost may return an error along the lines of: 
```
You are running 32-bit Python on a 64-bit OS
```
A possible fix is to install Homebrew and run 
```
brew install libomp
```


## Issues
1. Some data retrieved from the FastF1 API contains null values that the code isn't properly handling. If the notebook crashes out because of null values, sorry!

2. Boruta tries to set the n_estimator attribute for the inputted model. However, multilayer perceptrons have no such attribute! In this case, an untuned XGBoost model is used as a substitute.

3. When a code cell produces a lot of graphs, the first few graphs tend to not render.

