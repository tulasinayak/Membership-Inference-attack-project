#  **MEMBERSHIP INFERENCE ATTACK**
##  **CODE DESCRIPTION**
### 1. task0_resnet34_cifar10
Dataset: Cifar10 (The dataset for this notebook was saved on the drive)\
Target Model: Resnet34\
In this notebook, the shadow model was trained using the shadow.p dataset and saved. After training the shadow model, the dataset for the attack model was generated (member and non-member confidence). A neural network-based binary classifier (Attack model) was trained using the dataset generated from the shadow model. The confidence scores of the eval.p dataset was then obtained by feeding it into the target model. This confidence score was then passed through the attack model and the resulting accuracy was more than 68%. Similarly, the confidence score for test.p was obtained and evaluated by the attack model and the resulting prediction was submitted for evaluation.

### 2. task1_mobilenetv2_cifar10
Dataset: Cifar10 (The dataset for this notebook was saved on the drive)\
Target Model: MobileNetV2\
In this notebook, the shadow model was trained using shadow.p. The shadow model's architecture was chosen as the same as the target model(to behave similar to the target model). The shadow.p dataset was split into train and test, and trained accordingly. Later the dataset for the attack model was generated as follows : the confidence produced on training dataset by the shadow model was saved as feature and 1 as label(member), because this is the data that was used for training of the shdow model and gives inference about member confidences. Similarly test dataset was used to form non-member confidences(as test dataset was not a part of the training and thus is a non-member for shadow model). The entire dataset thus formed was then used to train the attack model, which is a binary classifier that takes confidence values as input and outputs the membership value. The attack model was then evaluated using eval.p by first getting confidence of the datapoints from the target model and then passing it through the attack model to get the membership value(0 or 1). The accuracy obtained was 65%. Finally the membership of datapoints was found by first obtaining confidence scores from the target model and then using it in the attack model to get the predicted labels and stored in a list. The final numpy list was saved and then submitted for evaluation.
   
### 3. task2_resnet34_tinyimagenet
Dataset: Tiny ImageNet (The dataset for this notebook was saved on the drive)\
Target Model: Resnet34\
In this notebook, the shadow model was trained using the shadow.p dataset and saved. After training the shadow model, the dataset for the attack model was generated (member and non-member confidence). A neural network-based binary classifier (Attack model) was trained using the dataset generated from the shadow model. The confidence scores of the eval.p dataset was then obtained by feeding it into the target model. This confidence score was then passed through the attack model and the resulting accuracy was more than 90%. 

### 4. task3_mobilenetv2_tinyimagenet:
Dataset: Tiny ImageNet (The dataset for this notebook was saved on the drive)\
Target Model: MobileNetV2\
In this notebook, the shadow model was trained using the shadow.p dataset and saved. After training the shadow model, the dataset for the attack model was generated (member and non-member confidence). A neural network-based binary classifier (Attack model) was trained using the dataset generated from the shadow model. The confidence scores of the eval.p dataset was then obtained by feeding it into the target model. This confidence score was then passed through the attack model and the resulting accuracy was more than 80%. Similarly, the confidence score for test.p was obtained and evaluated by the attack model and the resulting prediction was submitted for evaluation.



