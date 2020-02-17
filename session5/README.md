The goal of this excercise is to design & train a model on MNIST data with the following constraints:
1. Number of Params: Less than 10K
2. Epochs: Less than or equal to 15
3. Accuracy: 99.4%

The approach was to have a step by step process to reach the end goal:

Iteration 1 - File 1

Target:

Basics in place - data, transformations, training & test loop.
Design the model with following constrains: a. 10,000 params b. 15 Epocs
Result:

Total Params: 10,582
Best Training Accuracy: 99.51%
Best Test Accuracy: 99.21%
Analysis:

Model is able to learn with approx. 10k parameters, getting 99.4% with 10K params should be achivable with optimization
Model needs regularization, as there is a significant gap between test and training accuracies, given the MNIST dataset has low complexity.
After 8th/9th Epoch, the test accuracy fluctuates between and Max & Mix - indicator of not being able to converge, LR being high

Iteration 2 - File 2

Target:

Optimize for exactly less than 10,000 params
Result:

Total Params: 9,870
Best Training Accuracy: 99.42%
Best Test Accuracy: 99.27%
Analysis:

No reduction in ability to learn due to reduced number of parameters
Scope for imporovement through regulartization, data augmentation, LR tuning

Iteration 3 - File 3


Target:

Add Regulartization
Result:

Total Params: 9,870
Best Training Accuracy: 98.96%
Best Test Accuracy: 99.32%
Analysis:

After adding dropout, it is difficult for the model to learn
Test Accuracy is better than Training Accuracy
Not applying dropout to first two layers, is yeilding better test accuracy
Can use data augmentation (rotation) to make the model learn for patterns in titled images

Iteration 4 - File 4

Target:

Add Image Rotation
Result:

Total Params: 9,870
Best Training Accuracy: 98.70%
Best Test Accuracy: 99.37%
Analysis:

After adding image rotation there is an improvement in Test Accuracy
After 8th Epoch, the Test Accuracy is bouncing between 99.2X - 99.3x
Try LR scheduler


Iteration 5 - File 5

Target:

Add LR Scheduler
Result:

Total Params: 9,870
Best Training Accuracy: 98.71%
Best Test Accuracy: 99.41%
Analysis:

After adding LR scheduler, the test accuracy is more stabe in the range of 99.35% onwards.
