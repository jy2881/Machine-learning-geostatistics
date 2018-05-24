# Machine-learning-geostatistics
尝试两篇paper中的方法，比较在只有坐标和目标特征的情况下，地统计插值和机器学习方法的优劣：
1. Machine Learning Algorithms and Their Application to Ore Reserve Estimation of Sparse and Imprecise Data（Sridhar Dutta1, Sukumar Bandopadhyay2, Rajive Ganguli3, Debasmita Misra4）
2. Generating Prediction Map for Geostatistical Data Based on an Adaptive Neural Network Using only Nearest Neighbors（Sathit Prasomphan and Shigeru Mase）

第一篇文章中的方法是使用x,y以及他们的乘机和各自的平方作为特征进行运算，最终rmse是28335.897902843044
第二篇文章中的方法是使用x,y，以及他们与周围最近的10个点的平均距离，平均sin，cos作为特征进行运算，最终rmse是34872.721587371765
地统计插值会在arcgis软件中进行，最终rmse是9400

我得到的结果与论文中一致，如果只有xy坐标作为特征的话，机器学习方法在空间插值上的精度远不如地统计插值。
不过结合之前开发者大会时的demo，如果你的数据有很多有用的特征，那么机器学习方法肯定会精度更高。
