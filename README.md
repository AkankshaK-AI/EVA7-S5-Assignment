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
A large model with more than 194k parameters.
A large kernel(7*7) is used in the 8th convolution layer(FC) which is contributing towards the large parameters.
Model is over-fitting. Train accuracy is more than Test.



**Step 2:**

Target:
1) Reduce the number of parameters as it is a large model.
2) Reduce the size of the big kernel which will help in reducing the parameters
3) Include regularization techniques to reduce overfitting


Results:
Parameters: 6,070
Best Training Accuracy: 98.33(14th epoch)
Best Test Accuracy: 98.60(12th epoch)

Analysis:
Parameters are reduced from 194k to 6k resulting from:
(a)Reducing the parameters in the convoltuion layers
(b)Using a Gap layer at the end which helped reduce the kernel size of 7*7. 
This helped in reducing the model parameters. 

Model is under-fitting now. This could be due to 2 factors:
(a) Since the parameters are reduced drastically(from 194k to 6k), the model performance may have been impacted.
(b) The regularization techniques implemented of Batch Norm and Dropout may be causing the underfitting. We shall see in the next steps.



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
2) To include Step LR
3) To improve model performance to fix underfitting


Results:
Parameters: 10,790(image augmentation doesnt add parameters)
Best Training Accuracy: 99.33(epoch 14th)
Best Test Accuracy: 99.40(epoch 11th)

Analysis:
(1) Dropout was removed to improve model performance. Removing it helped!
Tried retaining **Dropout** and tweaking the LR at the below:
(a) 0.01(best train 98.91, test 99.31 thrice- underfitting w/o reaching target even once)
(b) 0.02(best train 98.85, test 99.36 - underfitting w/o reaching target even once)
(c) 0.03(best train 98.94, test 99.33 - underfitting w/o reaching target even once)
None of the LRs seemed to work. Removing the Dropout improved underfitting.

(2) Adding LR step didnt help the accuracy. Tried with the following LRs at step LR 6:
(a) LR 0.01 (best train 98.92, test 99.37 - underfitting w/o reaching target even once)
(b) LR 0.02 (best train 98.90, test 99.46 - underfitting with reaching target once at 14th epoch)
The model was underfitting and the loss and accuracy graphs looked inconsistent hence Step LR was dropped. 


(3) After dropping Step LR and Dropout, the Model performance has improved. We have acchieved our target of 99.4% with no underfitting.
Train and Test accuracy gap has reduced drastically hence model is working!   
