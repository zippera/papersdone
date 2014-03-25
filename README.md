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


