---
name: variant-ranking
description: 对 6 到 10 个 CD19 binder 改造候选进行优先级排序。用于用户已经有小面板候选并希望得到工程化排名时。不要用于大规模突变枚举或“只按 affinity”的排序。
---

# 目标

输出一版可执行、可解释、可沟通的优先级面板。

# 输入

- 候选列表：6 到 10 个
- 上游依据：`failure_hypotheses.md` 与相关论文卡
- 输出路径：`cases/case_001_fmc63/variant_panel.md`

# 输出

按 `templates/variant_panel.md` 写入排序结果。  
每个候选必须包含：

1. 候选名称
2. 编辑类型
3. 可能有帮助的原因
4. 预期收益
5. 主要风险
6. 排名
7. 排名理由（可写入备注列）

# 排序维度

每个候选都要经过以下维度审视：

- functional potential
- specificity 风险
- tonic signaling / clustering 风险
- durability 风险
- developability 风险
- manufacturability / complexity 风险

# 硬约束

- 不允许只看 affinity 或 KD。
- 对证据弱、机制链条断裂、可验证性差的候选降权。
- 第一版优先小步、可解释、可对照的改动。
- 明确保留不确定性，不伪装确定结论。

# 执行步骤

1. 将每个候选映射到对应失败假设。
2. 逐项评估收益与风险，形成相对排序。
3. 写入面板并检查是否仍保持 6 到 10 个聚焦想法。

# 禁止事项

- 不要扩写到 50+ 候选。
- 不要输出“看起来很强但无法解释”的黑箱排序。
- 不要省略主要风险字段。
