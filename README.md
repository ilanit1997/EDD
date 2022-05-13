# EDD
Epoch wise double descent based on paper https://arxiv.org/abs/2108.12006

These are the results of a project we did in ML2 course (097209) at the 'The Technion – Israel Institute of Technology'.


## Main results:
#### 1. Practical : remove EDD by PCA
* Based on Running Resnet18 on CIFAR10 
* code based on https://github.com/mohammadpz/Epoch_wise_Double_Descent
* In contrast to above, we took a subset of categories and preformed PCA to remove EDD which above showed. 


#### 2. Therotical : remove EDD by replacing last layer weights with theoretical converged
* We implemented the second method mentioned in the paper using a simple Fully connected net and a synthetic dataset. 
* This method was supposed to eliminate the double descent by replacing the weights of the last layer with converged weights, and continue training. 
* We show that for a specific input, it indeed eliminated the double descent, but these results vary from run to run, where for some runs there is no convergence at all (not show here).

## Plots:
### 1. Practical : remove EDD by PCA
#### CIFAR10 projected to different number of components
<img src="https://github.com/ilanit1997/EDD/blob/main/pca%20projs.JPG" width="800" height="800">

#### Accuracy
<img src="https://github.com/ilanit1997/EDD/blob/main/pca%20results%202.JPG" width="700" height="400">

#### Error
<img src="https://github.com/ilanit1997/EDD/blob/main/pca%20results%202.JPG" width="700" height="400">

### 2. Therotical : remove EDD by converged weights

#### Loss with/without the method
<img src="https://github.com/ilanit1997/EDD/blob/main/method%202%20results.JPG" width="700" height="400">

