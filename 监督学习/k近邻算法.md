# K近邻算法
KNN

通过计算待分类样本与训练集中各个样本的距离，找到距离最近的k个样本，然后根据这k个样本的类别或值来预测待分类样本的类别或值

## KNN基本原理

1.计算距离，计算待分类样本和训练集中每个样本的距离，欧式距离，曼哈顿距离等

2. 选择k个最近邻，

3. 投票或平均，分类问题投票，回归问题平均值

## KNN 的特点

简易易理解，无需训练，对数据分布无假设，计算复杂度搞，需要选择合适的k值

```python
from sklearn.neighbors import KNeighborsClassifier

knn = KNeighborsClassifier(n_neighbors=3)
knn.fit(X_train, y_train)
y_pred = knn.predict(X_test)
```
交叉验证或者可视化的方法选择最佳的k值

