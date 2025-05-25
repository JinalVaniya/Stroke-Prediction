 # Stroke Prediction Dataset: Binary Classification

- This dataset is used to predict whether a patient is likely to get a stroke based on the input features such as gender, ever smoked,  
bmi, and any other diseases. The dataset has 12 feature including target 'stroke', and 5110 instances. It is a binary classification problem.
- Features include, id which is unique for each instance, gender (male, female and other),age of the person, hypertension (0 for no, 1 for yes), heart_disease (0 for no, 1 for yes), ever_married (yes, no), work_type (children, govt_job, private, self-employed, never_worked), residence_type (rural or urban), avg_glucose_level, bmi, smoking_status (formely_smoked, smokes, unknown, never_smoked) and stroke (1 for yes, 0 for no). 
- The dataset has 201 null values in bmi feature, which is handled by inserting mean values in the null instance.
- gender has one faulty instance which has value of other, which was dropped.
- gender, ever_married, smoking_status, residence_type, and work_type are categorical features of dataset.
- categorical features were handled by using one-hot encoding using pandas library. After encoding categorical features all dataframes were concated and that original features were dropped along with id feature.
- Final features to train neural network on are 'Rural', 'Never_worked', 'Female', 'never_smoked', 'bmi', 'Self-employed', 'formerly_smoked', 'ever_married_yes', 'hypertension', 'avg_glucose_level', 'heart_disease', 'age', 'stroke'
- Correlation between each features and with target feature 'stroke' measured and 13 new features were selected which includes the least valued correlation features which are four, and features with highest correlation which are nine and created new dataframe to train neural network model.
- Features are divided into X and y dataset and scaled continuous values using StandardScaler, also, features data type is changed to float32.
- Dataset was split into 80/20. Neural network model is trained successfully, metris such as accuracy and confusion matrix are used to measure the performance of the dataset.
- The objective was to build an effective feedforward neural network (FNN) to accurately classify input data into one of two categories. architecture is consisting of three hidden layers. 
- The first hidden layer had 30 neurons, followed by a second hidden layer with 20 neurons and final hidden layer has 10 neurons. Each layer used ReLU activation functions, and the output layer configuration was adjusted based on the classification type. 
- Current model's performance is best out of all trained model.
- It has 67% training accuracy and 62% validation accuracy.
- Overall, the metrics demonstrated that a moderately deep network with appropriate regularization and task-specific loss functions provides a strong baseline for classification tasks using PyTorch.

References
https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset/data
https://docs.pytorch.org/tutorials/beginner/basics/buildmodel_tutorial.html
https://docs.pytorch.org/tutorials/beginner/pytorch_with_examples.html#nn-module
https://docs.pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html
