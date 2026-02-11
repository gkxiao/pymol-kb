# isomesh 语义约束
- 定义：在体素值 = threshold 处生成三角网格
- 法线方向：指向值增加方向（∇v）
- 内部 = 法线反向侧（值 < threshold）
- 外部 = 法线指向侧（值 > threshold）
- 陷阱：取反/掩膜不改变表面几何位置，仅改变值分布
- 正确用法：直接 isomesh map, threshold
