# EVA7-S5-Assignment
Have created a Neural Network model with 99.4% accuracy utilizing all the basic steps of Regularization(Batch Norm, Dropout, GAP), Image augmentation and StepLR

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
1) Fix underfitting by:
(a) Increasing parameters slightly(around 10k) to improve model performance
(b) Work on the regularization techniques to fix underfitting

2) Perform Max Pooling at RF=5


Results:
Parameters: 10,790
Best Training Accuracy: 99.55(accuracy improved than last time)
Best Test Accuracy: 99.34 (accuracy improved)

Analysis:
Parameters have increased(6k to 10k).
Model is performing better- Accuracy has improved and under-fitting has been fixed. 
Correcting the Max Pooling location also helped with the model performance.
To further improve accuracy, looking at the image samples, we can add slight rotation. 




**Step 4:**

Target:
To perform image augmentation to further improve model performance


Results:
Parameters: 10,790(image augmentation doesnt add parameters)
Best Training Accuracy: 99.34
Best Test Accuracy: 99.40(epoch 7th), 99.41(epoch 12th), 99.44(epoch 13th)

Analysis:
With image augmentation, Model performance has improved drastically. It hit the target accuracy 3 times overall with 2 times consistently(epoch 12th and 13th).
Train and Test accuracy gap has narrowed hence model is working! 
We will try the Step LR and see  if the performance improves any further


**Step 5:**

Target:
To add StepLR to the model to see if it further improves the accuracy making it more consistent in the last few epochs


Results:
Parameters: 10,790(StepLR doesnt add parameters)
Best Training Accuracy: 99.32(lesser than the step 3)
Best Test Accuracy: 99.41(epoch 10th), 99.40(epoch 13th)

Analysis:
StepLR hasnt improved the model any further with it hitting the taregt accuracy only 2 times as opposed to 3 times in the step 3. 
The Train and Test accuracy gap is still narrow in the last few epochs. 
