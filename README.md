# Inception_V1
Implementação da rede neural convolucional Inception V1 utilizando tensorflow 2.  <br/>
Artigo de referência Inception V1: https://arxiv.org/pdf/1409.4842v1.pdf  <br/>
Artigo de referência Batch Normalization: https://arxiv.org/pdf/1502.03167v3.pdf <br/>
Código de referência: https://github.com/tensorflow/models/blob/master/research/slim/nets/inception_v1.py <br/>
Artigo mais exemplos de códigos: https://paperswithcode.com/paper/going-deeper-with-convolutions  <br/>

# Resultado do treinamento
Foram treinados dois modelos. Um sem Batch Normalization(BN) e outro com Batch Normalization(BN). <br/>

| Inception V1  | Acurácia sem BN | Acurácia Com BN |
| ------------- | --------------- | --------------- | 
|  softmax 0    |     89.02%      |      87.08%     |
|  softmax 1    |     89.84%      |      97.54%     | 
|  softmax 2    |     98.76%      |      96.58%     |

<br/><br/>
| Inception V1  |   Loss sem BN   |   Loss Com BN   |
| ------------- | --------------- | --------------- | 
|  softmax 0    |     0.5322      |      0.7147     |
|  softmax 1    |     0.3873      |      0.6366     | 
|  softmax 2    |     0.0662      |      0.1775     |

<br/><br/>
| Inception V1  | Taxa de erro sem BN | Taxa de erro Com BN |
| ------------- | ------------------- | ------------------- | 
|  softmax 0    |       10.98%        |       12.92%        |
|  softmax 1    |       10.16%        |        2.46%        | 
|  softmax 2    |        1.24%        |        3.42%        |

<br/><br/>
Para treinar a rede foi utilizado o dataset Mnist com 10.000 imagens para treinamento. <br/><br/>
![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/bdec97aa-a6a8-4784-94b4-7f48da80215c) <br/>
(Gráfico do treinamento do modelo sem Batch Normalization.) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/4977f246-b089-402f-b568-27c2f5ecd7d2)
(Gráfico do treinamento do modelo com Batch Normalization.) <br/><br/><br/>

# Resultado dos testes
Para testar o modelo foram utilizadas 5.000 imagens.
## Modelo sem Batch Normalization
Acurácias das funções de softmax:  <br/>
    softmax 0: 0.8902000188827515  <br/>
    softmax 1: 0.8984000086784363  <br/>
    softmax 2: 0.9876000285148621  <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/41a4a7fd-0674-4f78-ae9e-e9383601f1c5)  <br/>
(Matriz de confusão para uma das funções de softmax. taxa de erro de 1.24%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/763d4936-1b01-459c-b686-7af941a6b3ad)  <br/>
(Matriz de confusão para uma das funções de softmax. taxa de erro de 10.16%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/bc3b1fba-8b91-4141-a028-ac1a57c5c923)  <br/>
(Matriz de confusão para uma das funções de softmax. taxa de erro de 10.98%)

## Modelo com Batch Normalization
Acurácias das funções de softmax:  <br/>
    softmax 0: 0.8708000183105469  <br/>
    softmax 1: 0.9753999710083008  <br/>
    softmax 2: 0.9657999873161316  <br/><br/><br/>
    
![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/4d93f8d4-2fee-49db-9a7f-f392ff963fb9) <br/>
(Matriz de confusão para uma das funções de softmax. taxa de erro de 3.42%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/32fd00c3-850f-4404-bfa9-723b91f5e0d3) <br/>
(Matriz de confusão para uma das funções de softmax. taxa de erro de 2.46%) <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/0cd2e9fe-8e91-47b3-a73e-a47a09ce60a2) <br/>
(Matriz de confusão para uma das funções de softmax. taxa de erro de 12.92%) <br/><br/><br/>
