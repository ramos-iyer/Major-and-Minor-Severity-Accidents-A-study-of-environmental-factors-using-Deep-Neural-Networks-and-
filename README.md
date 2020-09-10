# Major-and-Minor-Severity-Accidents-A-study-of-environmental-factors-using-Deep-Neural-Networks-and-

# Masters in Data Analytics Project - Research Thesis 

## Project: Major and Minor Severity Accidents: A study of environmental factors using Deep Neural Networks and Sensitivity Analysis

## Table of Contents

- [Overview](#overview)
- [Methodology](#method)
- [Components](#components)
  - [Data Merging and Preparation](#data)
  - [Feature Selection and Processing](#feature)
  - [Model Application](#model)
- [Running the Code](#running)
- [Screenshots](#screenshots)
- [System Configuration steps](#config)
- [File Descriptions](#files)
- [Credits and Acknowledgements](#credits)

***

<a id='overview'></a>

### Overview

Owing to the increase in number of vehicles and infrastructure, the need for severity analysis in road accidents has gained a fundamental importance. This research aims to create a severity detection system for major and minor accidents depending on the length of the road. In order to achieve this, the environmental factors of weather, road demographics, accident situation factors and nearby landmarks has been taken into consideration. The literature survey shows that the implementation of feature importance on a per class basis along with the model as a whole has not been widely explored. The implemented Stratified K-Fold Deep Neural Network performs better than traditional ensemble models with an accuracy of more than 89% for both, Major and Minor accidents. Along with this, to gain more information from the neural network and how it predicts, SHAP (Shapely Additive Explanations) has been applied to gain overall importance. These feature importance scores have been further explored on a per class basis using the data itself and extraction of SHAP scores for each class. The findings from this research can be used by the main four stakeholders in an accident - transportation safety planners, hospitals, medical agencies and insurance companies for proactive action and purposes.

<a id='method'></a>

### Methodology

The below image shows the methodology followed in order to implement this project and gather the insights from the data:

<a id='components'></a>

### Components
There are three components to this project:

<a id='data'></a>

#### Data Merging and Preparation
File _'Data Merging and Preparation.ipynb'_ :

- Imports the `US Accidents` dataset
- Uses Address information to extract the `Road Demographics` data
- Merges `US Accidents` and `Road Demographics` data using the Street Name
- Exports the data into a csv file

<a id='feature'></a>

#### Feature Selection and Processing
File _'Feature Selection and Processing.ipynb'_ :

- Imports the `merged` dataset
- Uses the Severity information to transform the data and split into two categories: Minor and Major Accidents
- Performs Pre-Procesing and Transformation on both the categories of accidents
- Gneerates 4 categories for each type of accident (Major and Minor) using the length of the road
- Applies Random Forest to perform feature selection for both the Minor and Major Accidents
- Exports the feature selected data into a csv file

<a id='model'></a>

#### Model Application
File _'Model Application.ipynb'_ :

- Imports the `feature selected` dataset
- Applies the SKDNN model along with other traditional ensemble models for benchmarking purposes
- Generates the evaluation metrics for all models for comparison
- Applies SHAP on the SKDNN model to generate the feature importance for both Major and Minor accidents
- Uses SHAP scores to generate the feature importance on a per class basis for both Major and Minor accidents

<a id='running'></a>

### Running the Code

Download the US_Accidents data from the link given below - 
https://smoosavi.org/datasets/us_accidents

Extract the tar.gz file and store the .csv file in Data --> US_Accidents folder.

Make sure that the .csv file name is 'US_Accidents_Dec19.csv'

NOTE - Do not change the tree structure of the folders as this may cause the code to break.

When Executing the code files, please execute only in the sequence given below - 

1) Data Merging and Preparation.ipynb

2) Feature Selection and Processing.ipynb

3) Model Application.ipynb

<a id='screenshots'></a>

### Screenshots

<a id='config'></a>

### System Configuration Steps

The main software used for this project was the programming language Python (version 3.7.6) using which the various steps of data pre-processing, transformations, visualisations and machine learning models were applied. This distribution of python was installed on the machine using Anaconda2 (version 2020.02), which is an open source software that supports jupyter-notebooks, R, RStudio, Python, etc. Jupyter notebook was used as the Development environment for the implementation of the python code.

To ease the process of installation, you can also run the below commands in the Anaconda Prompt to create a new environment with jupyter-notebook, python and the
necessary packages. In order to do this, once you install Anaconda in your machine, follow the below steps to prepare the environment and run the code. 

NOTE : Install "Microsoft Visual C++ 14.0" in your machine as this is a pre-requisite for the package "SHAP" to function. The installation file is provided in the following link -

https://aka.ms/vs/16/release/vs_buildtools.exe

While installation, please select "Visual Studio Build Tools 2019" for installing all necessary packages for the tool to function with SHAP.

1) Step 1 : Open Start Menu -> Anaconda -> Anaconda Prompt

2) Step 2 : Execute the below command and follow the instructions given on screen in the Anaconda Prompt to create environment and install some of the necessary packages given above -

"conda create -n rp python=3.7.6 catboost=0.23.2 lightgbm=2.3.1 matplotlib=3.2.2
numpy=1.18.5 pandas=1.0.5 plotly=4.8.2 pyspark=3.0.0 scikit-learn=0.23.1 shap=0.35.0
jupyter"

3) Step 3 : Once the environment in created, navigate to the environment in Anaconda Prompt by executing the command -

"conda activate rp"

4) Step 4 : Install the osmnx package by executing the below command -

"conda install -c conda-forge osmnx=0.15.1"

5) Step 5 : Install the tensorflow and xgboost packages by executing the below command one after the other -

"pip install 'tensorflow==2.2.0'"

"pip install 'xgboost==1.1.1'"

6) Step 6 : Once the installation is complete navigate to the folder where the code files have been downloaded in Anaconda Prompt and execute the below command 

"jupyter notebook"

NOTE : 'rp' is the name of the environment that is created in anaconda

<a id='files'></a>

### File Descriptions

Below are the files and the folders that are part of the project implementation:

1. Data:
- Feature Selected Data:
  - US_Accidents_Road_DR_PS_Major.csv: Contains the data for Major accidents after Pre-Processing and Feature Selection
  - US_Accidents_Road_DR_PS_Minor.csv: Contains the data for Minor accidents after Pre-Processing and Feature Selection
 
- Merged Data:
  - US_Accidents_Road.csv: Contains the data after Pre-Processing and Merging is performed on the `US Accidents` and `Road Demographics` datasets.

2. Data Merging and Preparation.ipynb: Contains the code for Data Pre-Processing and Merging

3. Feature Selection and Processing.ipynb: Contains the code for performing Transformations and Feature Selection on the merged data

4. Model Application.ipynb: Contains the code to implement the SKDNN and other traditional ensemble models on Major and Minor accidents along with SHAP on the Feature selected data

<a id='credits'></a>

### Credits and Acknowledgements

* [S.Moosavi](https://www.themoviedb.org/) for providing the `US_Accidents` data used for this project.
* [OSM(Open Street Maps)](https://osmnx.readthedocs.io/en/stable/) for providing the `Road Demographics` data used for this project.
* [NCI](https://www.ncirl.ie/) for the guidance as part of their full-time masters in data analytics course subject 'Research Thesis'
