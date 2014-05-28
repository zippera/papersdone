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
13. **Robust Object Tracking Using Constellation Model with Superpixel**。用超像素提供的信息求 parts 的 likelihood，外观模型用的 star model，跟踪框架还是基于粒子滤波的。
14. **Sparse coding based visual tracking: Review and experimental comparison** 一篇综述，讲的非常好，尤其是 sparse coding 在 visual traking 中的应用，虽然不详细，但是会获得直观的了解。
15. **Incremental learning for robust visual tracking**，target 用训练出来的低维空间的 eigenbasis 表示，particle 也用这个表示，然后计算距离。关键是增量地学习出 eigenbasis，所谓增量，就是把最近跟踪出来的 target也加入训练数据，文章中的算法力求提高训练效率。整体的跟踪框架还是传统的 particle filter. 
16. **Fast video shot boundary detection framework employing pre-processing techniques**，提供了一个用于视频镜头分割的框架，极大的减少了需要计算的 non-boundary segments，对于 hard-cut 和 GT 也提供了很好的方案。不涉具体的特征和距离选择。
17. **Abrupt Motion Tracking via Adaptive Stochastic Approximation Monte Carlo Sampling**，实验室师兄周修庄的 CVPR 论文。用 DOS 来动态更新目标分布，escape local trap.用density grid 动态更新 proposal，使得采样的接受率更高。
18. **Wang-Landau Monte Carlo-Based Tracking Methods for Abrupt Motions**，K.M.Lee 团队2013年的 PAMI。提出了三种方法：WLMC,AWLMC,NFWL. 也用 Dos 来应对 abrupt motion.用 ML 来代替原来的目标分布，这个是可以用样本估计的。AWLMC 中用增加退火的步骤，来make promising regions more compact.NFWL 主要是应对考虑 scale 突变的情况，这时候样本空间大了很多，为了有效采样，使用无拒绝的提议分布，另外更新 DOS 的幅度也有效加大。
19. **Abrupt motion tracking using a visual saliency embedded particle filter**，赵清杰老师团队发表在 PR 的一篇论文。在跟丢的时候用 saliency map 来 detect 高概率的几个区域。这个有点仿生学的意味，当 center 和 surround 的 constrat 很大时，这个 center 的 saliency 或 attention 比较大。具体的计算过程基本是用的 USC iLab 的。


