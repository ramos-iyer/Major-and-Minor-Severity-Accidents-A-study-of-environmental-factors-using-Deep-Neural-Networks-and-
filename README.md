# Major-and-Minor-Severity-Accidents-A-study-of-environmental-factors-using-Deep-Neural-Networks-and-
Owing to the increase in number of vehicles and infrastructure, the need for severity analysis in road accidents has gained a fundamental importance. This research aims to create a severity detection system for major and minor accidents depending on the length of the road. In order to achieve this, the environmental factors of weather, road demographics, accident situation factors and nearby landmarks has been taken into consideration. The literature survey shows that the implementation of feature importance on a per class basis along with the model as a whole has not been widely explored. The implemented Stratified K-Fold Deep Neural Network performs better than traditional ensemble models with an accuracy of more than 89% for both, Major and Minor accidents. Along with this, to gain more information from the neural network and how it predicts, SHAP (Shapely Additive Explanations) has been applied to gain overall importance. These feature importance scores have been further explored on a per class basis using the data itself and extraction of SHAP scores for each class. The findings from this research can be used by the main four stakeholders in an accident - transportation safety planners, hospitals, medical agencies and insurance companies for proactive action and purposes.

Download the US_Accidents data from the link given below - 
https://smoosavi.org/datasets/us_accidents

Extract the tar.gz file and store the .csv file in Data --> US_Accidents folder.

Make sure that the .csv file name is 'US_Accidents_Dec19.csv'



NOTE - Do not change the tree structure of the folders as this may cause the code to break.


When Executing the code files, please execute only in the sequence given below - 

1) Data Merging and Preparation.ipynb

2) Feature Selection and Processing.ipynb

3) Model Application.ipynb

The main software used for this project was the programming language Python (version 3.7.6) using which the various steps of data pre-processing, transformations, visualisations and machine learning models were applied. This distribution of python was installed on the machine using Anaconda2 (version 2020.02), which is an open source software that supports jupyter-notebooks, R, RStudio, Python, etc. Jupyter notebook was used as the Development environment for the implementation of the python code.

To ease the process of installation, you can also run the below commands in the Anaconda Prompt to create a new environment with jupyter-notebook, python and the
necessary packages. In order to do this, once you install Anaconda in your machine, follow the below steps to prepare the environment and run the code explained in the
forth-coming sections. 

NOTE : Install "Microsoft Visual C++ 14.0" in your machine as this is a pre-requisite for the package "SHAP" to function. The installation file is
provided in the following link -
https://aka.ms/vs/16/release/vs buildtools.exe

While installation, please select "Visual Studio Build Tools 2019" for installing
all necessary packages for the tool to function with SHAP.

 Step 1 : Open Start Menu -> Anaconda -> Anaconda Prompt
 Step 2 : Execute the below command and follow the instructions given on screen
in the Anaconda Prompt to create environment and install some of the necessary
packages given above -
"conda create -n rp python=3.7.6 catboost=0.23.2 lightgbm=2.3.1 matplotlib=3.2.2
numpy=1.18.5 pandas=1.0.5 plotly=4.8.2 pyspark=3.0.0 scikit-learn=0.23.1 shap=0.35.0
jupyter"
 Step 3 : Once the environment in created, navigate to the environment in Anaconda
Prompt by executing the command -
"conda activate rp"
 Step 4 : Install the osmnx package by executing the below command -
"conda install -c conda-forge osmnx=0.15.1"
 Step 5 : Install the tensor
ow and xgboost packages by executing the below com-
mand one after the other -
"pip install 'tensor
ow==2.2.0'"
"pip install 'xgboost==1.1.1'"
 Step 6 : Once the installation is complete navigate to the folder where the code
les have been downloaded in Anaconda Prompt and execute the below command
"jupyter notebook"
 NOTE : 'rp' is the name of the environment that is created in anaconda
