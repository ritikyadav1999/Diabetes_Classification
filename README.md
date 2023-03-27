# CSGO Round Winner Prediction
Task_6 of Kaiburr Assessment


### 1. Problem Statement 
####  To predict the Rounder winner of CSGO either it can be Terrorist or Counter Terrorist

### 2. DataSet
#### DataSet Link : https://raw.githubusercontent.com/insignificantGuy/Kaggle-Datasets/main/csgo_round_snapshots.csv
The dataset consists of round snapshots from about 700 demos from high level tournament play in 2019 and 2020. Warmup rounds and restarts have been filtered, and for the remaining live rounds a round snapshot has been recorded every 20 seconds until the round is decided. Following its initial publication, It has been pre-processed and flattened to improve readability and make it easier for algorithms to process. The total number of snapshots is 122411. Snapshots are i.i.d and should be treated as individual data points, not as part of a match.These features or values includes time_left, ct_score, bomb_planted, ct_armor, t_armor,etc. Total of 96 Feature are given to predict the round Winner

![Loading the Dataset](https://user-images.githubusercontent.com/122474267/227891623-88205789-1e28-42ec-a3d4-a49603c868c9.png)


### 3. Requirement
1. Google Collab for Online
2. Jupyter Notebook and python for running the project locally on the machine

### 4. Method
The methodology consists roughly of two chronological steps. First the data is thoroughly explored and dimensionality reduction is applied. Secondly a suitable and  optimized model is applied to our problem. The work-flow of these two steps are carried out in the python-notebooks mentioned above.

### 4.1 Data exploration
Initial exploration and analysis of the dataset.Features and Labels are extracted.
![Data exploration and finding null values1](https://user-images.githubusercontent.com/122474267/227891666-4cce9a00-0983-4a06-8f1d-dd04c8cd4303.png)
![Data exploration and finding null values2](https://user-images.githubusercontent.com/122474267/227891691-4f7b4f35-e925-48d9-82ec-82e4ffe41ff7.png)



### 4.2 Distributions and relationship
First the distributions of the different attributes and their relationship to the target are inspected by the means of histograms and correlation.

### 4.3 Splitting and standardize the data

At this stage we drop missing data and preprocess the data for efficient performance and best results, We use Standard Scaler from sklearn.preprocessing library to scale the data.Using this mode standarization normal distribution is achieved.Then the  data is separated into an training set and a test set in ratio 80:20. The test set wont be used at any point, this set will eventually simulate new data used to evaluate the final model.

![Data preprocessing](https://user-images.githubusercontent.com/122474267/227891778-1032a959-0a30-47c6-aa42-f2cf8ee98960.png)

![Splitting the data in training and testint set](https://user-images.githubusercontent.com/122474267/227891955-35189dd2-51bc-4d32-825d-11711a414ec4.png)



### 5. Model Selection
KNN (K nearest Neighbour) model is selected.

![Fitting the data to the model](https://user-images.githubusercontent.com/122474267/227891829-89ae9e8f-aa8c-4e65-8ea1-3a3bec7d18fd.png)


### 6. Evaluate models using Confusion Matrixes and validation data
Confusion matrix is generated to closely observe the performace of the model.

### 7. Test
Finally we test the final model on the held out test-set.

### Result
Accuracy of 84 percent is achieved

![Generating the Confusion Matrix and results](https://user-images.githubusercontent.com/122474267/227891879-051067d8-b576-43ef-ac22-c081be3da51a.png)







