---
name: evidence-pack
description: 将前序分析（论文卡、失败假设、变体面板）整合为面向客户的 CD19 lead rescue 证据包。用于用户要求生成或重写 cases/case_001_fmc63/evidence_pack.md 时，强调可读性与证据分层。
---

# 目标

把内部分析结果转译为客户可理解、可追溯的结论与建议。

# 输入

- `cases/case_001_fmc63/intake.md`
- `cases/case_001_fmc63/structure_notes.md`
- `cases/case_001_fmc63/failure_hypotheses.md`
- `cases/case_001_fmc63/variant_panel.md`

# 输出

按 `templates/evidence_pack.md` 产出到：

- `cases/case_001_fmc63/evidence_pack.md`

内容必须覆盖：

1. 项目概览
2. 基准先导
3. 当前不理想点
4. 直接证据
5. 强推断
6. 关键未知项
7. 下一步聚焦面板
8. 优先级理由
9. 需要明确沟通的风险

# 硬约束

- 语言用中文，避免术语堆砌。
- 论文标题保留英文原文。
- 明确分层：直接证据 / 强推断 / 未知项。
- 不承诺湿实验结果，不把假设写成事实。

# 执行步骤

1. 汇总上游文件，抽取一致结论与冲突点。
2. 将技术细节翻译为客户关心的影响（效果、风险、可执行性）。
3. 用模板成稿并检查“是否每个结论都能追溯到证据或推断”。

# 禁止事项

- 不要写成论文综述或方法学教科书。
- 不要忽略风险与不确定性。
- 不要脱离 CD19/FMC63 范围扩题。
