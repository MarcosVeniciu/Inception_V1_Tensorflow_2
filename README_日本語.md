# Inception_V1
TensorFlow 2を使用したInception V1畳み込みニューラルネットワークの実装です。<br/>
Inception V1の参考論文: https://arxiv.org/pdf/1409.4842v1.pdf <br/>
バッチ正規化の参考論文: https://arxiv.org/pdf/1502.03167v3.pdf <br/>
参考コード: https://github.com/tensorflow/models/blob/master/research/slim/nets/inception_v1.py <br/>
さらなるコード例の記事: https://paperswithcode.com/paper/going-deeper-with-convolutions <br/>

# 学習結果
2つのモデルが学習されました。バッチ正規化（BN）なしのモデルとバッチ正規化（BN）ありのモデルです。<br/>

| Inception V1  | BNなしの正解率 | BNありの正解率 |
| ------------- | ---------------- | ----------------- |
|  softmax 0    |     89.02%       |      87.08%       |
|  softmax 1    |     89.84%       |      97.54%       |
|  softmax 2    |     98.76%       |      96.58%       |

<br/>

| Inception V1  | BNなしの損失   | BNありの損失   |
| ------------- | --------------- | --------------- |
|  softmax 0    |     0.5322      |      0.7147     |
|  softmax 1    |     0.3873      |      0.6366     |
|  softmax 2    |     0.0662      |      0.1775     |

<br/>

| Inception V1  | BNなしのエラー率   | BNありのエラー率   |
| ------------- | ------------------ | ------------------ |
|  softmax 0    |       10.98%       |       12.92%       |
|  softmax 1    |       10.16%       |        2.46%       |
|  softmax 2    |        1.24%       |        3.42%       |

<br/><br/>
ネットワークの学習には10,000枚のMnistデータセットが使用されました。<br/><br/>
![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/bdec97aa-a6a8-4784-94b4-7f48da80215c) <br/>
（バッチ正規化なしのモデルの学習グラフ）<br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/4977f246-b089-402f-b568-27c2f5ecd7d2)
（バッチ正規化ありのモデルの学習グラフ）<br/><br/>

# テスト結果
モデルのテストには5,000枚の画像が使用されました。
## バッチ正規

化なしのモデル
ソフトマックス関数の正解率: <br/>
    softmax 0: 0.8902000188827515 <br/>
    softmax 1: 0.8984000086784363 <br/>
    softmax 2: 0.9876000285148621 <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/41a4a7fd-0674-4f78-ae9e-e9383601f1c5) <br/>
（ソフトマックス関数の混同行列。エラー率1.24%）<br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/763d4936-1b01-459c-b686-7af941a6b3ad) <br/>
（ソフトマックス関数の混同行列。エラー率10.16%）<br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/bc3b1fba-8b91-4141-a028-ac1a57c5c923) <br/>
（ソフトマックス関数の混同行列。エラー率10.98%）<br/><br/><br/>

## バッチ正規化ありのモデル
ソフトマックス関数の正解率: <br/>
    softmax 0: 0.8708000183105469 <br/>
    softmax 1: 0.9753999710083008 <br/>
    softmax 2: 0.9657999873161316 <br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/4d93f8d4-2fee-49db-9a7f-f392ff963fb9) <br/>
（ソフトマックス関数の混同行列。エラー率3.42%）<br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/32fd00c3-850f-4404-bfa9-723b91f5e0d3) <br/>
（ソフトマックス関数の混同行列。エラー率2.46%）<br/><br/><br/>

![image](https://github.com/MarcosVeniciu/Inception_V1/assets/42542651/0cd2e9fe-8e91-47b3-a73e-a47a09ce60a2) <br/>
（ソフトマックス関数の混同行列。エラー率12.92%）<br/><br/><br/>
