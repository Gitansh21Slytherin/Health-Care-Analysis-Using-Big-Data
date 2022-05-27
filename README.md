# Health-Care-Analysis-Using-Big-Data
Medicine and health are the primary fields gaining importance in today's advancing world, where technology is frequently evolving. 
Analyzing and knowing the disease one is suffering from is a difficult task. Even if the disease is predicted correctly, 
it is difficult to acquire information from specialists of that particular disease. People often find it difficult, in this busy world, 
to take the time to visit a doctor. 

## Processing health care data using PySparks

To implement, we used google colab as our main platform in which we installed pyspark, and the environment is set. Then from pyspark, we imported pyspark and Spark context and spark conf. From spark sql, we imported the spark session.
 First, we imported our training dataset, which has the list of symptoms with around 113 symptoms and the last column as the type of prognosis. Then we got the schema of our data. For prediction, we used MLLIB, a library consisting of machine learning algorithms such as regression, classification, collaborative filtering ,clustering, dimensionality reduction, and other optimization primitives. We also used a multi-classification evaluator. 
 Next, we took our testing data, set up the pipeline, and introduced a string indexer that converts a single column into an index column and then is given to this pipeline. Vector assembler is used for which input and output columns were defined. The input columns were every column of the testing data except prognosis and prognosis index, and output columns were given as features. 
Vector Assembler is actually a transformer that combines a given list of columns into a single vector column. So, the final output data had a feature vector in it. A final data was prepared with features and prognosis index, this final data is split and with the help of Multi Classification Evaluator, we made the prediction. We used Logistic regression, Random Forest, and Decision tree for carrying out our predictions.


![image](https://user-images.githubusercontent.com/69135317/170732357-cb852bfd-cf95-4e51-a8f4-25302934aa9b.png)
# Setting up pipeline 
![image](https://user-images.githubusercontent.com/69135317/170732388-24005a95-7e70-4170-a7c7-61b80807488f.png)
# Transforming the target column 
![image](https://user-images.githubusercontent.com/69135317/170732426-5f749d18-e567-4ed9-8e6d-386e64616d1b.png)
![image](https://user-images.githubusercontent.com/69135317/170732441-0bf5adfc-c771-4f9d-aace-538e3d8fe43f.png)
# Results
The used algorithms from MLLIB Logistic regression gave us the perfect accuracy of 0.9. The time comparisons are shown in the below picture.

![image](https://user-images.githubusercontent.com/69135317/170732472-9c1b8984-d015-4031-adef-d89d7fa5b5bc.png)
