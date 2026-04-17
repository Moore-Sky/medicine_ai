---
name: structure-critique
description: 为现有 CD19 binder/CAR lead（默认 FMC63）生成首轮失败假设。用于用户要求“解释当前 lead 为什么不理想”并需要结构与机制支撑时。输出严格 3 条假设，不用于 de novo 设计。
---

# 目标

产出可用于下一步变体设计的首轮失败解释框架。

# 输入

- benchmark lead：默认 FMC63
- 相关论文卡：1 到 3 篇（如 He 2023、Ghorashian 2019）
- 可选结构笔记：`cases/case_001_fmc63/structure_notes.md`

# 输出

写入 `cases/case_001_fmc63/failure_hypotheses.md`，严格 3 条。  
每条必须包含：

1. 假设陈述
2. 机制理由
3. 支持证据
4. 置信度
5. 最大未知点
6. 工程含义

# 硬约束

- 只在 CD19 lead rescue 范围内推理。
- 区分直接证据与推断，不夸大因果关系。
- 至少 1 条假设体现 affinity 之外风险（如 tonic signaling、durability、developability）。
- 不给湿实验执行细节，只给高层工程含义。

# 推荐假设篮子

优先从以下类型中选择，通常覆盖至少两类：

- 表位/结合几何不匹配
- affinity window 偏离
- antigen-density sensitivity 不理想
- tonic signaling 或 clustering 风险
- durability / exhaustion 权衡失衡

# 执行步骤

1. 读取输入论文卡与结构笔记，列出直接已知事实。
2. 用“事实 -> 机制路径 -> 假设”方式构建 3 条假设。
3. 检查每条假设是否可转译为后续变体方向。

# 禁止事项

- 不要写第 4 条及以上假设。
- 不要把所有问题归因于“affinity 太高/太低”。
- 不要用营销化措辞替代证据表述。
