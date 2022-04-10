# 构建两层神经网络分类器

要求：
数据集：MINIST；
不可使用pytorch，tensorflow等python package，可以使用numpy。

## 模型训练

1. 数据导入：划分训练集、验证集、测试集
2. 激活函数：定义Relu、Sigmod、Softmax作为激活函数，计算其导数
3. 网络构建：class NeuralNetwork初始化神经网络、前向传播、反向传播
4. 优化器SGD: class SGD实现学习率下降策略，采用weight_dacay实现L2正则化，完成参数更新
5. 模型保存和载入：保存和载入所训练的模型参数
6. 模型拟合：利用保存的模型参数、优化器获得训练的loss和accuracy

### 参数查找

1. 学习率查找范围为 [0.1, 0.05, 0.01]，隐藏层大小查找范围为[36, 64, 100]，正则化强度查找范围为[0, 0.01, 0.02]
2. 通过搜索得到最佳模型的超参数为：

```python
 'layer': [784, 100, 10],
 'learning_rate': 0.1,
 'weight_decay': 0
```
在验证集上的Accuracy为97.55%

### 测试

导入参数查找得到的最佳模型，进行测试，输出分类精度

```python
Test accuracy = 97.54 %
```

### 可视化

导入参数查找得到的最佳模型

1. 对每层的参数进行可视化
<img width="312" alt="weight1" src="https://user-images.githubusercontent.com/38133106/162612539-39d10f07-a161-4721-9cf8-9dae396e0a4a.png">
<img width="302" alt="weight2" src="https://user-images.githubusercontent.com/38133106/162612543-6265e8d1-c95d-4106-9b9a-3f1163365ab2.png">

2. 对模型的Loss和Accuracy可视化
<img width="305" alt="Loss" src="https://user-images.githubusercontent.com/38133106/162612549-47464eee-d329-43d6-b69d-c6276d49a40c.png">

<img width="324" alt="Accuracy" src="https://user-images.githubusercontent.com/38133106/162612547-f95720bf-64b8-4ace-88ad-7c64d245e58b.png">


 ## 模型链接
 
以下百度云链接包含了27个模型的参数结果。
链接：https://pan.baidu.com/s/1dOUQdJY4GOCCMcBkF-IqbA 
提取码：qi12
