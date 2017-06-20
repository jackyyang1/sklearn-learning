# k-means 和 knn 区别

### knn

数据集 label 已经标号，每次有一个未知点x，寻找它最邻近的K个点，进行投票，确定未知点x属于哪一个数据集。

没有明显的前期训练过程。

属于监督学习的分类算法，有对应类别的输出。

### k-means

原始数据杂乱无章，没有label，假设数据集合可以分为k个簇。

有明显的前期训练过程。

属于无监督学习的聚类算法，无对应类别的输出。

# 相同点

都用到了NN算法，一般用KD树实现。

### 优点

* 收敛速度快
* 聚类效果优
* 算法可解释性强
* 主要需要调参的是簇数K

### 缺点

* K值不好把握
* 对于不是凸的数据集不好收敛
* 如果隐含类别的数据不均衡，则聚类效果不佳
* 采用迭代方法，得到的结果只是局部最优
* 对噪音和异常点比较敏感



# sklearn

KMeans，传统算法。

MiniBatchMeans，增加batch\_size 参数



### n\_clusters

k值

#### 评估标准：

无监督标准没有样本输出，没有直接的聚类评估方法。但可以从簇内的稠密程度和离散程度来评估聚类效果。

常见的方法有轮廓系数Silhouette Coefficient和Calinski-Harabasz Index。

Calinski-Harabasz Index，对应sklearn的metrics.calinski\_harabaz\_score，类别内部数据的协方差越小越好，类别之间的协方差越大越好，这样分数会高


























