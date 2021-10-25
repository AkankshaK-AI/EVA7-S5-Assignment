# EVA7-S5-Assignment
Have created a Neural Network model with 99.4% accuracy utilizing all the basic steps of Regularization(Batch Norm, Dropout, GAP), Image augmentation and LR

**Step 1:**
Target
Get the set-up right
Set Transforms
Set Data Loader
Set Basic Working Code
Set Basic Training  & Test Loop

Results:
Parameters: 194,884
Best Training Accuracy: 99.29
Best Test Accuracy: 98.98

Analysis:
A large model.
Model is over-fitting


**Step 2:**

Target
Reduce parameters as it was a large model.
Include regularization techniques to reduce overfitting
To reduce the size of the big kernel


Results:
Parameters: 6,070
Best Training Accuracy: 98.33(14th epoch)
Best Test Accuracy: 98.60(12th epoch)

Analysis:
Parameters are reduced.
Model is under-fitting. Since the parameters are reduced drastically, we see the model performance impacted.



**Step 3:**

Target
Increase parameters to improve model performance
Perform Max Pooling at RF=5


Results:
Parameters: 10,790
Best Training Accuracy: 98.94
Best Test Accuracy: 99.30

Analysis:
Parameters are increased.
Model is still under-fitting. 
Seeing image samples, we can see that we can add slight rotation. 




**Step 4:**

Target
To perform image augmentation
To improve model performance to fix underfitting


Results:
Parameters: 10,790(image augmentation doesnt add parameters)
Best Training Accuracy: 99.33(epoch 14th)
Best Test Accuracy: 99.40(epoch 11th)

Analysis:
Dropout was dropped to improve model performance. Removing it helped!
Model performance is good. We have acchieved our target of 99.4%. 
Train and Test accuracy gap has reduced drastically hence model is a good one!  
