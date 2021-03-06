# bert

## 说明
参考 [bert-as-service](https://github.com/hanxiao/bert-as-service),只保留生成embedding的代码。

- 想要了解具体的bert实现，请参考 [google-bert](https://github.com/google-research/bert)

- 已经预训练好的模型，请访问 [模型链接](https://github.com/google-research/bert#pre-trained-models).

## 使用

由于github文件大小限制，模型文件上传不了，需自行下载！
**环境**

``python3.6`` ``tf>1.11.0`` 
本机在mac上，python3.6，Tensorflow=1.12.0下运行成功，模型使用的是chinese_L-12_H-768_A-12

**测试**
```bash
python3 app.py
```
token后的结果为：
```
{'input_ids': [[101, 156, 10986, 1962, 7410, 1557, 8013, 102, 0, 0], [101, 2582, 720, 1215, 1450, 8043, 102, 0, 0, 0]], 'input_mask': [[1, 1, 1, 1, 1, 1, 1, 1, 0, 0], [1, 1, 1, 1, 1, 1, 1, 0, 0, 0]], 'input_type_ids': [[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]]}
```
每个字（中英文会有些不一样）的字向量的结果为：
```
[[ 0.32057902  0.24202809  0.2541557  ...  0.20263498  0.6716434
  -0.44200176]
 [ 0.29238474  0.9817248   0.8073269  ... -0.60760117 -0.47178632
  -0.4586985 ]
 [ 0.98668313  0.16165426  0.3832808  ... -0.12513126  0.2904796
  -0.27908644]
 ...
 [-0.04917896 -0.03079737  0.04156147 ... -0.01933306  0.05342017
  -0.05265636]
 [-0.03597467  0.10591426  0.18550058 ... -0.45721024  0.08414445
  -0.8926494 ]
 [-0.02865382  0.05233088  0.17591827 ... -0.4366305  -0.17922227
  -0.89913315]]
  
  [[ 1.0479005e-01  7.3439270e-01  3.8874063e-01 ...  6.8628770e-01
   8.2020587e-01  6.7148171e-04]
 [ 2.0819670e-01  6.8765157e-01  1.8640351e-01 ...  3.2885015e-01
  -1.7083383e-01 -5.8352238e-01]
 [ 2.1026824e-01  6.6219294e-01  4.8657697e-01 ...  1.2565545e+00
   3.8487002e-01 -5.1607740e-01]
 ...
 [ 6.4796191e-03  2.0019138e-01 -2.6513118e-01 ... -3.4045702e-01
  -8.5869491e-02 -3.8626540e-01]
 [-1.8027518e-03  1.7195117e-01 -3.0354312e-01 ... -2.5821635e-01
  -1.1416042e-01 -4.2028350e-01]
 [-5.4810565e-02  1.6658526e-02 -1.5580910e-01 ... -1.4111766e-01
  -3.8496125e-01 -5.7737166e-01]]
```
比如测试的`NLP`，在词典里面没有，分成 `n` + `lp`
mdzz

时间消耗：
```
cost time: 8.301791191101074
```

有时间研究下bert原理，欢迎探讨
emlo、gpt、bert

微信
`YC990800269`


