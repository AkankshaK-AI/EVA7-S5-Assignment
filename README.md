# EVA7-S5-Assignment
Have created a Neural Network model with 99.4% accuracy utilizing all the basic steps of Regularization(Batch Norm, Dropout, GAP), Image augmentation and LR

**Step 1:**
Target:
1) Get the set-up right
2) Set Transforms
3) Set Data Loader
4) Set Basic Working Code
5) Set Basic Training  & Test Loop

Results:
Parameters: 194,884
Best Training Accuracy: 99.29
Best Test Accuracy: 98.98

Analysis:
A large model with more than 150k parameters
Model is over-fitting. Train accuracy is more than Test


**Step 2:**

Target:
1) Reduce parameters as it is a large model.
2) Include regularization techniques to reduce overfitting
3) To reduce the size of the big kernel which will help in reducing the parameters


Results:
Parameters: 6,070
Best Training Accuracy: 98.33(14th epoch)
Best Test Accuracy: 98.60(12th epoch)

Analysis:
Parameters are reduced.
Model is under-fitting. Since the parameters are reduced drastically(from 194k to 6k), we see the model performance impacted.



**Step 3:**

Target:
1) Increase parameters slightly(around 10k) to improve model performance
2) Perform Max Pooling at RF=5


Results:
Parameters: 10,790
Best Training Accuracy: 98.94
Best Test Accuracy: 99.30

Analysis:
Parameters are increased.
Model is still under-fitting. 
Seeing image samples, we can see that we can add slight rotation. 




**Step 4:**

Target:
1) To perform image augmentation
2) To improve model performance to fix underfitting


Results:
Parameters: 10,790(image augmentation doesnt add parameters)
Best Training Accuracy: 99.33(epoch 14th)
Best Test Accuracy: 99.40(epoch 11th)

Analysis:
Dropout was dropped to improve model performance. Removing it helped!
Model performance is good. We have acchieved our target of 99.4%. 
Train and Test accuracy gap has reduced drastically hence model is a good one!  
