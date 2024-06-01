#  **MEMBERSHIP INFERENCE ATTACK**
##  **CODE DESCRIPTION**
### 1. task0_resnet34_cifar10

### 2. task1_mobilenetv2_cifar10
   
### 3. task2_resnet34_tinyimagenet
Dataset: Tiny ImageNet (The dataset for this notebook was saved on the drive)\
Target Model: Resnet34\
In this notebook, the shadow model was trained using the shadow.p dataset and saved. After training the shadow model, the dataset for the attack model was generated (member and non-member confidence). A neural network-based binary classifier (Attack model) was trained using the dataset generated from the shadow model. The confidence scores of the eval.p dataset was then obtained by feeding it into the target model. This confidence score was then passed through the attack model and the resulting accuracy was more than 90%. 

### 4. task3_mobilenetv2_tinyimagenet:
Dataset: Tiny ImageNet (The dataset for this notebook was saved on the drive)\
Target Model: MobileNetV2\
In this notebook, the shadow model was trained using the shadow.p dataset and saved. After training the shadow model, the dataset for the attack model was generated (member and non-member confidence). A neural network-based binary classifier (Attack model) was trained using the dataset generated from the shadow model. The confidence scores of the eval.p dataset was then obtained by feeding it into the target model. This confidence score was then passed through the attack model and the resulting accuracy was more than 80%. Similarly, the confidence score for test.p was obtained and evaluated by the attack model and the resulting prediction was submitted for evaluation.



