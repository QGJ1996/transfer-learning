# transfer learning
* 这个库中包含三个迁移学习方法，分别为TNB(Transfer Naive Bayes)[^1]、TCA+(Transfer Components Analysis +)[^2]和CCA(Canonical Correlation Analysis)[^3]
* **针对数据类型为表格数据类型**
* **改库仅为二分类问题的实例**
## TNB
主要包含5部分：数据读取、计算目标域的先验概率、离散化、计算目标域的条件概率、计算最终预测结果。
* 数据获取对应dataloader文件夹
* 计算目标域的先验概率对应PriorProbability类
* 离散化对应DiscreteByEntropy类
* 条件概率对应ConditionProbability类
* 最终预测结果对应predict方法
## TCA+
主要包含了三部分：数据读取、选择标准化方法、TCA方法
* 数据读取与TNB相同
* 根据[2]的规则选择标准化方法
* TCA类进行分布对齐和降维，返回降维后的数据，如果存在虚数，只取实部
## CCA
* **该方法在sklearn中有具体的实现类，在sklearn中的cross_decomposition中[^4]**
[^1]:Ma Y, Luo G, Zeng X, et al. Transfer learning for cross-company software defect prediction[J]. Information and Software Technology, 2012, 54(3): 248-256.
[^2]:Nam J, Pan S J, Kim S. Transfer defect learning[C]//2013 35th international conference on software engineering (ICSE). IEEE, 2013: 382-391.
[^3]:Jing X, Wu F, Dong X, et al. Heterogeneous cross-company defect prediction by unified metric representation and CCA-based transfer learning[C]//Proceedings of the 2015 10th Joint Meeting on Foundations of Software Engineering. 2015: 496-507.
[^4]:https://scikit-learn.org/stable/modules/generated/sklearn.cross_decomposition.CCA.html#sklearn.cross_decomposition.CCA
