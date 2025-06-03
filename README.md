# DSE: 230 SP2025 Final

# Contents 
- **Dataset/** contains the raw (.csv) and preprocessed (.arff) data that was from WISDM (Wireless Sensor Data Mining) lab dataset from UCI ML Repository. The data set was downloaded from here <https://archive.ics.uci.edu/dataset/507/wisdm+smartphone+and+smartwatch+activity+and+biometrics+dataset>
- **EDA_raw.ipynb:** Contains EDA for the raw data. 
- **EDA_arff.ipynb:** Contains EDA for of the .arff files. Ultimately, we used the raw data in lieu of this data. 
- **Generate_Features.ipynb:** This notebook cointains the similar code as EDA_raw.ipynb but without the outputs and plots and some exploration. It also creates a .csv for each sensor, features_{sensor}.csv. These files are used in the classification notebook.
- **features_phone_a.csv, features_phone_g.csv, features_watch_a.csv, features_watch_g.csv:** data files for classification
- **Activity_Classification(LOSO-LR).ipynb:** Classification using  Leave-One-Subject-Out and Linear Regression method.
- **Activity_Classification(LOSO-RF).ipynb:** Classification using  Leave-One-Subject-Out and Random Forest method.
- **Activity_Classification(LOSO-RF-Sub).ipynb:** Classification using  Leave-One-Subject-Out, Random Forest, and substitue method.
- **Activity_Classification(LOSO-watch_a).ipynb:** Classification using  Leave-One-Subject-Out on watch acceleration data.
- **DSE230_Final_Project_Biometrics_SP2025.pdf:** Summary of the project's results. 

# How to run 
The EDA_raw and EDA_arff notebooks are stand alone EDA notebooks. Ensure the path to the dataset source directory of the datasets is correct after downloading. Variable named "path" in all notebooks should be pointed to the correct place according to adjacent comments. The EDA notebooks do not need to be ran before runnning a classifier as the result is already in this repository in the form of features_{sensor}.csv files.

As explained in the dataset description, ARFF files are data in interval format that were designed for Weka machine learning tool. There exists an EDA to explore this data in this repository but this project only uses the raw data for analysis.

To run the classification models ensure the features_{sensor}.csv files are present. If not, run Generate_Features.ipynb. This notebook will create those 4 csv files. 

The classification notebooks will update some libraries (dask, pandas, scikit-learn) with pip to ensure the code will run properly with working versions.

All notebooks in this repository was intended to be run in a Jupyter Notebook environment with Spark installed.


# Results
The results of the EDA process, data preparation, and analysis are discussed in the report PDF titled "DSE230_Final_Project_Biometrics_SP2025.pdf".


# Authors 
Thomas Brehme, Duy Nguyen, Grant Wagener 

