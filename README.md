## Integrated Analysis of Microarray and Clinical Data for Predicting Neuroblastoma Patient Outcomes
* Author:Isil Erbasol Serbes (12.10.2023)

Reference paper: Zhang, W., Yu, Y., Hertwig, F., Thierry-Mieg, J., Zhang, W., Thierry-Mieg, D., Wang, J., Furlanello, C., Devanarayan, V., Cheng, J. and Deng, Y., 2015. Comparison of RNA-seq and microarray-based models for clinical endpoint prediction. Genome biology, 16(1), pp.1-12.
https://genomebiology.biomedcentral.com/articles/10.1186/s13059-015-0694-1?report=reader (research paper)
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE49710 (information related to dataset)


Introduction:

In this analysis, I leveraged two datasets:

    * Microarray Data: allProbIntensities_rawdata_final.csv
        This dataset contains microarray probes obtained from neuroblastoma patients.

    * Clinical_meta_Data: clinical_data_for_assessment_final.csv
        This dataset comprises clinical data for neuroblastoma patients.

Objective:

The primary aim of this analysis is to assess the performance of machine learning model(s) in predicting the following critical clinical endpoints (targets) for neuroblastoma patients using a combination of microarray data and clinical data:

    * INSS Stage (class)
        Predicting the INSS stage for each patient.

    * High-Risk Classification (class)
        Determining whether a patient is at high risk for neuroblastoma.

    * Death from Disease(class)
        Predicting the likelihood of a patient succumbing to the disease.

    * Progression (class)
        Forecasting the progression of the disease in patients.

This analysis will help us understand the predictive capabilities of machine learning models (classifiers) in the context of neuroblastoma prognosis by integrating molecular and clinical data.

#### Planned steps for the analysis
1) EDA (Explanatory Data Analysis)
Understand the datasets: Getting insights into the data's structure, distribution, and key features.
2) Data preprocessing (steps in between can change) - this data preprocessing will be individual for each clinical endpoints
Make the datasets ready for analysis
   * Data spliting (train-test (20%))
   * Imputing missing data
   * Handling imbalance dataset
   * Dealing with outliers
   * Filtering unnecessary features
   * Normalisation
3) Perform unsupervised learning 
Unsupervised learning techniques will be employed to explore patterns, clusters, and relationships within the data, helping us determine if it's amenable to subsequent supervised learning for predictive modeling and classification tasks.
   * Due to nonlinear nature of microarray data, planing to use UMAP
   * Combine the UMAP with a clustering algorithm 
4) Feature selection with Stratified cross validation
5) Hyperparameter optimisation
6) Model training and evaluation
Evaluating the model is essential for assessing its performance and generalizability.

