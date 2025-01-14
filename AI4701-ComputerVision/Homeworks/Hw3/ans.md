## 对输入中小的平移的近似不变性

池化操作能够达成对输入中小的平移的近似不变性，这是因为：池化层通过对其输入的局部区域进行**下采样**，从而抽象出更高层次的特征。例如，在最大池化或平均池化中，**即使像素点出现微小的平移，其局部相应值能基本保持不变（窗口内的最大值或平均值）**，这种高层特征仍然会被提取出来。因此，池化层对输入中的小平移具有近似的不变性。

## 好处

这种不变性带来了几个好处：

1. 增强泛化能力：因为模型对小的平移不敏感，它能更好地处理在不同位置、大小和角度下出现的相同特征，从而提高了模型对新、未见过的数据的泛化能力。
2. 减少过拟合风险：减少模型对训练数据中的精确位置信息的依赖，降低了模型过拟合的风险。
3. 降低计算成本：通过减小特征图的空间维度，池化减少了后续层的参数数量和计算量，从而降低了模型的计算成本。
