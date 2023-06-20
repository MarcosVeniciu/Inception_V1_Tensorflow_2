# Inception_V1
Implementation of the Inception V1 convolutional neural network using TensorFlow 2.  <br/>
Reference Article Inception V1: https://arxiv.org/pdf/1409.4842v1.pdf  <br/>
Batch Normalization reference Article: https://arxiv.org/pdf/1502.03167v3.pdf <br/>
Reference code: https://github.com/tensorflow/models/blob/master/research/slim/nets/inception_v1.py <br/>
Article more code examples: https://paperswithcode.com/paper/going-deeper-with-convolutions  <br/>

# Training Results
Two models were trained: one without Batch Normalization (BN) and another with Batch Normalization (BN). <br/>

| Inception V1  | Accuracy without BN | Accuracy with BN |
| ------------- | ------------------ | ---------------- | 
|  softmax 0    |      89.02%        |      87.08%      |
|  softmax 1    |      89.84%        |      97.54%      | 
|  softmax 2    |      98.76%        |      96.58%      |

<br/>

| Inception V1  | Loss without BN | Loss with BN |
| ------------- | --------------- | ------------ | 
|  softmax 0    |     0.5322      |    0.7147    |
|  softmax 1    |     0.3873      |    0.6366    | 
|  softmax 2    |     0.0662      |    0.1775    |

<br/>

| Inception V1  | Error Rate without BN | Error Rate with BN |
| ------------- | --------------------- | ------------------ | 
|  softmax 0    |       10.98%          |       12.92%       |
|  softmax 1    |       10.16%          |        2.46%       | 
|  softmax 2    |        1.24%          |        3.42%       |

<br/><br/>
The Mnist dataset with 10,000 images was used to train the network. <br/><br/>
![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/bdec97aa-a6a8-4784-94b4-7f48da80215c) <br/>
(Training graph for the model without Batch Normalization.) <br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/4977f246-b089-402f-b568-27c2f5ecd7d2)
(Training graph for the model with Batch Normalization.) <br/><br/>

# Test Results
5,000 images were used to test the model.
## Model without Batch Normalization
Accuracy of softmax functions:  <br/>
    softmax 0: 0.8902000188827515  <br/>
    softmax 1: 0.8984000086784363  <br/>
    softmax 2: 0.9876000285148621  <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/41a4a7fd-0674-4f78-ae9e-e9383601f1c5)  <br/>
(Confusion matrix for one of the softmax functions. Error rate of 1.24%) <br/><br/><br/>



![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/763d4936-1b01-459c-b686-7af941a6b3ad)  <br/>
(Confusion matrix for one of the softmax functions. Error rate of 10.16%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/bc3b1fba-8b91-4141-a028-ac1a57c5c923)  <br/>
(Confusion matrix for one of the softmax functions. Error rate of 10.98%)

## Model with Batch Normalization
Accuracy of softmax functions:  <br/>
    softmax 0: 0.8708000183105469  <br/>
    softmax 1: 0.9753999710083008  <br/>
    softmax 2: 0.9657999873161316  <br/><br/><br/>
    
![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/4d93f8d4-2fee-49db-9a7f-f392ff963fb9) <br/>
(Confusion matrix for one of the softmax functions. Error rate of 3.42%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/32fd00c3-850f-4404-bfa9-723b91f5e0d3) <br/>
(Confusion matrix for one of the softmax functions. Error rate of 2.46%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/0cd2e9fe-8e91-47b3-a73e-a47a09ce60a2) <br/>
(Confusion matrix for one of the softmax functions. Error rate of 12.92%) <br/><br/><br/>
 
