Papers I have read.
==========
To track and list the papers I have read,with simple comments.

###On Visual Tracking

1. *Highly Nonrigid Object Tracking via Patch-Based Dynamic Appearance Modeling.* K.M.Lee 用到 patch,star model
2. *An adaptive coupled-layer visual model for robust visual tracking.* LukaCˇehovin. local 和 global
3. *Visual tracking decomposition.* K.M.Lee 一个 tracker 包括一对 obs 和 motion model，不同 tracker 通过 IMCMC 交互，通过一个标准判断是否接受这个采样
4. *Adaptive pyramid mean shift for global real-time visual tracking.* 用 color 和 background，动态调整 scale。
5. *Tracking by Sampling Trackers.* K.M.Lee 一个 tracker 用四维向量表示，posterior 分解。
6. *Robust Object Tracking Using Constellation Model with Superpixel.* Weijun Wang 从上个时刻的分布进行采样I 个；Motion；观测更新权重；每个样本根据star model采样leaf，并根据 leaf 的观察更新权重。形成新的分布。
7. *Embedding motion in model-based stochastic tracking.* J.M. Odobez pf 讲的很好，三个假设。打破假设。
8. *Nearest neighbor field driven stochastic sampling for abrupt motion tracking.* proposal中使用到 nnf，总体用 mcmc，有一个平滑。
9. **基于聚类的视频镜头分割和关键帧提取**，很简单地利用解决了连雪帧聚类的问题。
10. **融合 HCRF 和 AAM 的足球精彩事件检索**,提出13种可用的情感特征，找到每种事件特有的情感特征组合，根据这个组合加权求和计算情感激励值，作为 HCRD 的一个观察输入。然后训练出 HCRF 用于分类。
11. **SLIC superpixels**，用类似 kmeans 的方法，简单好用。这个[c++源代码](https://github.com/PSMM/SLIC-Superpixels)写的非常好，注释也清晰，已经详细阅读过。代码可以作为其他论文实现时的参考，也可以作为平时使用 c++时的参考。
12. **Superpixel Segmentation for Robust Visual Tracking**。用 SLIC 做超像素分割，然后用决策树做二分类训练，在新的一帧中对超像素进行分类，找到足够的 patch 来描述这个 object。


