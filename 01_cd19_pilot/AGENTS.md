# AGENTS.md

## 仓库目标

这个仓库是一个 **以 Codex 为先** 的 CD19 lead rescue 试点。

目标不是从零发明全新疗法。  
目标是训练一条可靠工作流：

1. 读一篇论文
2. 提取可复用的结构/机制洞察
3. 解释现有 lead 为什么可能不理想
4. 提出聚焦的变体面板
5. 用现实工程标准给面板排序
6. 形成面向客户的证据包

## 范围

在本仓库中，始终默认：

- target = CD19
- 主 benchmark binder = FMC63
- 项目类型 = CAR binder / antibody lead rescue 分析
- 首选输出语言 = 中文
- 当有助于仓库一致性时，文件名与标题可使用英文

除非有明确指令，不要扩展范围。

## 硬边界

不要做以下事情：

- 切换到 pMHC
- 把动物或湿实验执行细节写成已验证事实
- 把推测性想法当作既定事实
- 只按 affinity 优化
- 生成巨大且未筛选的突变集
- 在没有明确理由时重写整个仓库结构

## 工作方式

在本仓库执行任务时：

1. 先读 `README.md`、`TODAY.md`、`acceptance.md`、`progress.md`。
2. 优先使用 `templates/` 里的现有模板。
3. 输出保持简洁、结构化、带证据标注。
4. 明确区分：
   - 直接证据
   - 强推断
   - 未决问题
5. 每完成一个有意义步骤后更新 `progress.md`。

## 好结果的标准

本仓库中的高质量输出应满足：

- 论断能关联到论文或结构记录
- 用简明中文解释机制
- 不把 affinity 混同为整体产品质量
- 覆盖风险维度，例如：
  - specificity 风险
  - tonic signaling 风险
  - durability 风险
  - developability 风险
  - manufacturability 风险
- 收敛为小规模且有优先级的面板

## 文件级指导

### `references/paper_list.md`
保持为精选来源清单。  
不要变成超大参考文献堆。

### `cases/case_001_fmc63/intake.md`
这是标准论文/案例卡整合文件。  
优先按模板输出。

### `cases/case_001_fmc63/failure_hypotheses.md`
第一轮严格写 3 条假设。  
每条假设必须包含：
- 假设陈述
- 机制理由
- 支持证据
- 置信度
- 关键不确定性

### `cases/case_001_fmc63/variant_panel.md`
第一版保持 6–10 个聚焦想法。  
每个想法必须包含：
- 编辑类型
- 可能有帮助的原因
- 主要风险
- 排名

### `cases/case_001_fmc63/evidence_pack.md`
这是面向客户的文档。  
避免术语堆叠。  
说明每个结论为何重要。

## 今日完成定义

仅当以下条件全部满足，今日任务才算完成：

1. 至少 1 篇 P0 论文已转成 paper card
2. `structure_notes.md` 已存在
3. 已写出首版 3 条失败假设
4. `progress.md` 已更新

## 命令与仓库行为

当前没有构建系统。  
本仓库是 documentation-first。  
优先直接编辑 Markdown 文件。

如果后续创建辅助脚本，请在 `README.md` 记录，并保持结果可复现、确定。

## 自检规则

在宣布完成前，检查输出是否存在：

- 无证据支持的陈述
- 过度自信措辞
- 缺少风险讨论
- 过度扩题
- 未区分证据与推断
