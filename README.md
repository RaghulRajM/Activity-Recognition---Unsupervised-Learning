# Activity-Recognition---Unsupervised-Learning

### Problem Statement

With the advancement in IOT, sensors analytics have played a huge role in day to day activities. Sudden spike in the availability and usage of smart watches is a great example for this. Application of sensors analytics living beings to track their actions and vital signs has huge set of problem pool, namely – Calorie tracker, early warning for life threatening diseases, protection of endangered species, improve sports person’s abilities etc.
The current problem can be considered as the base for all the above mentions applications of sensor analytics on living things. Certain experiments were carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz were captured. The experiments have been video-recorded to label the data manually. (http://www.youtube.com/watch?v=XOEN9W05_4A)
As it can be seen in the video, different actions have unique patterns in the signals which were captured. Thus, the dataset can be used as a test bed to see the practical effect of all the clustering algorithms learned in Unsupervised L1 course.  Since data also has the target variable, y, thus it will be very helpful to compare the clustering results with the actual outcome, apart from standard cluster performance metrics like silhouette score etc.

### Tasks to do: -
Combine all the walking activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS) as single activity and build a 4-cluster model and profile it.
Build a 6-cluster model for all the activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) and profile it.
Experiment with all the clustering techniques introduced in Unsupervised L1 course and K-Means.
(Kindly divide the data into 70-30 train-test split to evaluate the cluster outcome with the target variable)
Compare at least 3 clustering techniques based on the outcome and profiling.
Number of features to be used is upto you and for every clustering technique used, the features used can differ. But you have to provide reasons for using those features in a particular model.
Profiling a clustering model is nothing but extensive documentation about the process and the results. You can either create a document or a PowerPoint deck with following information for each model: -
Train and test instance size
Columns used and no. of models
Parameters used
For the first 3 points, the reasons are also required
Clustering performance evaluation metrics (https://scikit-learn.org/stable/modules/clustering.html#clustering-performance-evaluation)
Since, luckily we have the target variable here, therefore Accuracy, Precision and Recall scores too apart from the performance evaluation metrics mentioned above.
The inference made form the last 2 points are required

### Data Description
As mentioned above, this is an experimental data. The data has 561 features, apart from the action label and the identifier for the subject on whom the experiment was conducted
For each record it is provided: -
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.
The dataset includes the following files: -
'activity_labels.txt': Links the class labels with their activity name.
'X_experiment.txt': Experiment set.
'y_experiment.txt': Experiment labels.
'subject.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30.
'features.txt': List of all features.

### Feature information: -
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 
Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also, the magnitude of these three-dimensional signals was calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 
Finally, a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 
These signals were used to estimate variables of the feature vector for each pattern ('-XYZ' is used to denote 3-axial signals in the X, Y and Z directions):
-  tBodyAcc-XYZ
-  tGravityAcc-XYZ
-  tBodyAccJerk-XYZ
-  tBodyGyro-XYZ
-  tBodyGyroJerk-XYZ
-  tBodyAccMag
-  tGravityAccMag
-  tBodyAccJerkMag
-  tBodyGyroMag
-  tBodyGyroJerkMag
-  fBodyAcc-XYZ
-  fBodyAccJerk-XYZ
-  fBodyGyro-XYZ
-  fBodyAccMag
-  fBodyAccJerkMag
-  fBodyGyroMag
-  fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 
-  mean(): Mean value
-  std(): Standard deviation
-  mad(): Median absolute deviation 
-  max(): Largest value in array
-  min(): Smallest value in array
-  sma(): Signal magnitude area
-  energy(): Energy measure. Sum of the squares divided by the number of values. 
-  iqr(): Interquartile range 
-  entropy(): Signal entropy
-  arCoeff(): Autorregresion coefficients with Burg order equal to 4
-  correlation(): correlation coefficient between two signals
-  maxInds(): index of the frequency component with largest magnitude
-  meanFreq(): Weighted average of the frequency components to obtain a mean frequency
-  skewness(): skewness of the frequency domain signal 
-  kurtosis(): kurtosis of the frequency domain signal 
-  bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.
-  angle(): Angle between to vectors.

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:
-  gravityMean
-  tBodyAccMean
-  tBodyAccJerkMean
-  tBodyGyroMean
-  tBodyGyroJerkMean

### Points to Note:
Features are normalized and bounded within [-1,1].\
The units used for the accelerations (total and body) are 'g's (gravity of earth -> 9.80665 m/seg2).
The gyroscope units are rad/seg.

### Reference
[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. A Public Domain Dataset for Human Activity Recognition Using Smartphones. 21th European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning, ESANN 2013. Bruges, Belgium 24-26 April 2013.
