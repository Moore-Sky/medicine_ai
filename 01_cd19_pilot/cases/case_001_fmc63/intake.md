# FMC63 案例卡整合

以下内容仅覆盖 `references/paper_list.md` 中的 P0 论文，目的不是做综述，而是为 `CD19 / FMC63 lead rescue` 提供首轮可复用证据。

## P0-1 He et al., 2023

### 引用信息
He et al., 2023. *CD19 CAR antigen engagement mechanisms and affinity tuning*. Sci Immunol 8:eadf1426.

### 核心问题
这篇论文要解决的是：能否把 `FMC63` 与 `SJ25C1` 的 CD19 结合结构直接转成可操作的 binder 调参抓手，从而改变 CAR 对不同 `antigen density` 的识别阈值，而不是只追求更强结合。

### 研究系统
- target: 人源 `CD19` 可溶 ectodomain；并在高 / 中 / 低 CD19 density 的肿瘤细胞模型中做功能评估
- binder / CAR: `FMC63`、`SJ25C1` 及其结构指导突变体
- assay / model: cryo-EM、MD/MM-GBSA、SPR、CAR-T 杀伤、trogocytosis、细胞因子释放

### 关键结构发现
- `FMC63` 与 `SJ25C1` 的 variable region 序列不相近，但在 CD19 上识别部分重叠的膜远端表位。
- `FMC63` 主要通过 `VH` 域接触 CD19，`VL` 也参与；接触重点集中在作者定义的 `loop 1 (154-166)` 与 `loop 2 (214-224)`。
- `SJ25C1` 相对 `FMC63` 在 CD19 表面近似旋转约 `90°`，除 `loop 1/2` 外还更明显接触 `loop 3 (95-109)`。

### 关键功能发现
- 在该文的 SPR 条件下，`FMC63 WT` 约为 `4.5 nM`，`SJ25C1 WT` 约为 `26.9 nM`。
- 适度降低 affinity 后，CAR 在高 / 中抗原密度靶细胞上仍可保持较强杀伤，但在低抗原密度条件下活性明显分化，说明 affinity 会直接改写 `density threshold`。
- 更弱的 binder 往往伴随更低的 `CD19 trogocytosis`；但 affinity 降得过头时，会连带损伤细胞因子释放与总体杀伤。

### 工程改动
作者基于结构与 MD 热点做了小规模理性突变，而不是大规模枚举：
- `FMC63`: `Y70A`、`Y260A`、`Y261A`
- `SJ25C1`: `W52F`、`I120V`、`I120A` 及更激进的 glycine 突变

### 对 CD19 lead rescue 的可复用启示
- `FMC63` 不应被当成只能“保留或替换”的黑箱；它已有清晰的结构热点，可做有限、可解释的局部调参。
- 对 CD19 CAR 来说，binder 调参影响的不只是 `KD`，还影响低抗原密度识别、trogocytosis 与功能窗口。
- 更合理的目标是把 `FMC63` 从“固定强结合”改成“按目标 antigen density 校准阈值的 binder”。

### 证据与推断
#### 直接证据
- cryo-EM 给出了 `FMC63-CD19` 与 `SJ25C1-CD19` 的结合几何。
- SPR 量化了 WT 与多个突变体的相对 affinity。
- CAR 功能实验直接显示不同突变体在高 / 中 / 低 CD19 density 条件下的杀伤与 trogocytosis 差异。

#### 强推断
- 对 `FMC63` 做温和弱化，可能是降低过度敏感、改善功能窗口的现实起点。
- 结合几何与接触 loop 的差异，意味着不同 binder 不能仅用单一 `KD` 横向互换。

#### 开放问题
- 该文没有直接回答这些 affinity/geometry 差异在长期 `durability`、`tonic signaling`、`developability` 上的代价。
- 文中突变是 proof-of-mechanism，不等于已给出最优临床级 rescue 方案。

## P0-2 Ghorashian et al., 2019

### 引用信息
Ghorashian et al., 2019. *Enhanced CAR T cell expansion and prolonged persistence in pediatric patients with ALL treated with a low-affinity CD19 CAR*. Nat Med 25:1408-1414.

### 核心问题
这篇论文要回答的是：一个比 `FMC63` 更低 affinity 的 CD19 binder，是否可能在真实产品表现上更好，而不是更差。

### 研究系统
- target: `CD19`
- binder / CAR: 低 affinity `CAT` binder，对照 `FMC63`
- assay / model: SPR、CD19 loop 突变结合分析、体外增殖/杀伤、异种移植模型、儿科复发/难治 B-ALL 临床研究

### 关键结构发现
- 通过 CD19 loop 突变，作者显示 `CAT` 与 `FMC63` 识别相同或高度重叠的表位区域。
- 两者共同依赖 `loop 1 / loop 2` 中的关键残基；文中点到 `L96`、`C97`、`W159`、`R163` 为共同敏感位点。
- `CAT` 还额外受 `Y157`、`K161`、`D162` 影响，提示即便表位重叠，微观接触方式仍不相同。

### 关键功能发现
- 文中 SPR 显示 `CAT` 相比 `FMC63` 为显著更低 affinity 的 binder；`CAT` 报告 `KD` 约 `14 nM`，差异主要来自更快 `off-rate`，而不是更慢 `on-rate`。
- `CAT CAR T` 在体外显示更强增殖/细胞毒潜力，在异种移植模型中也显示更好的增殖能力与抗肿瘤活性。
- 临床部分显示 `12/14` 例复发/难治儿科 B-ALL 获得分子缓解；`11/14` 在末次随访仍检测到 CAR T 持续存在；摘要中报告未见 severe CRS。

### 工程改动
核心工程变化不是大范围改造，而是把 `FMC63` 换成一个更低 affinity、`off-rate` 更快、但表位仍相邻/重叠的 `CAT` binder。

### 对 CD19 lead rescue 的可复用启示
- “失败不是因为绑得不够紧”是这条线的第一性结论之一。
- 对 CD19 CAR，适度降低 affinity、缩短结合停留时间，可能反而提升扩增与持续性。
- 若未来要 rescue `FMC63`，优先考虑“局部降敏/调 off-rate”，而不是默认继续做更强结合。

### 证据与推断
#### 直接证据
- SPR 直接比较了 `CAT` 与 `FMC63` 的 binding kinetics。
- 体外、动物与小规模临床数据都支持低 affinity 方案并未牺牲总体抗肿瘤潜力。
- CD19 loop 突变结果支持 `CAT` 与 `FMC63` 表位重叠。

#### 强推断
- `off-rate` 调节可能比单纯追求更低 `KD` 更接近真正可优化的产品旋钮。
- 若 `FMC63` 存在过强占据或过度敏感问题，沿重叠表位做“更快松手”的变体，比彻底换表位更稳健。

#### 开放问题
- 这篇论文不能把所有产品差异都单独归因于 binder，仍可能混有构型、制造与临床人群差异。
- 文中的 `FMC63` 对照 affinity 数值不应脱离 assay 背景直接当成通用金标准。

## P0-3 Seigner et al., 2023

### 引用信息
Seigner et al., 2023. *Solving the mystery of the FMC63-CD19 affinity*. Sci Rep 13:23024.

### 核心问题
这篇论文聚焦一个很工程化的问题：文献里 `FMC63-CD19` 的 `KD` 为什么能差到一百倍以上，哪些数值可以信，哪些可能只是 assay artifact。

### 研究系统
- target: 可溶 `CD19` 与细胞表面 `CD19`
- binder / CAR: `FMC63 scFv`
- assay / model: 文献回顾、steady-state binding 设计比较、优化后的 SPR；重点控制 `equilibration`、`ligand depletion` 与 `avidity`

### 关键结构发现
- 本文不是新结构论文，但使用已知 `FMC63-CD19` 结构信息来界定优化后的可溶 CD19 系统，并强调 interaction partner 的正确折叠/单体状态对 affinity 判读很重要。

### 关键功能发现
- 作者整理出文献中 `FMC63 scFv` 对 `CD19` 的 `KD` 报道大致落在 `0.3-47 nM`，差异超过百倍。
- 他们证明 `insufficient equilibration`、`ligand depletion` 与多价/构型带来的 `avidity` 都会把测得的 affinity 带偏。
- 在“严格单体、正确折叠、并尽量排除 artefact”的 SPR 条件下，作者给出的 `FMC63 scFv` affinity 约为 `2-6 nM`。

### 工程改动
这篇论文改的不是 binder，而是测量体系本身：把容易混入 artefact 的实验设计换成更接近真实单体 1:1 结合的读数框架。

### 对 CD19 lead rescue 的可复用启示
- 后续所有 `variant-ranking` 都不该把某一个历史 `FMC63 KD` 当绝对真值。
- 跨论文比较 affinity 时，必须先问“interaction partner 是什么构型、是否单体、是否达到平衡、是否有 ligand depletion / avidity”。
- 对 rescue 项目来说，`KD` 更适合作为相对排序工具，而不是唯一目标函数。

### 证据与推断
#### 直接证据
- 论文直接演示了不同实验设计如何造成测得 affinity 的系统性偏差。
- 优化测量后给出了更窄的 `FMC63` affinity 区间。

#### 强推断
- 许多看似“产品更优/更差”的 affinity 叙事，可能先要扣除 assay 设计误差后才能成立。
- `FMC63` 的合理工程起点更像“低 nM 级基准”，而不是某个单一神圣数字。

#### 开放问题
- 即使 `KD` 被校准，`kon/koff`、结合几何和 CAR 构型对功能的贡献仍需要与 He 2023、Ghorashian 2019 联合解释。

## P0-4 Teplyakov et al., 2018

### 引用信息
Teplyakov et al., 2018. *Crystal structure of B-cell co-receptor CD19 in complex with antibody B43 reveals an unexpected fold*. Proteins 86:495-500.

### 核心问题
这篇论文首先解决的是 CD19 外部结构到底长什么样，以及一个真实 anti-CD19 抗体如何识别这个目标。

### 研究系统
- target: `CD19` extracellular domain
- binder / CAR: 抗 `CD19` 抗体 `B43 Fab`
- assay / model: X-ray crystallography（论文报告 CD19-B43 复合物及 unbound B43）

### 关键结构发现
- CD19 ectodomain 并不是按序列直觉预测的“两个串联 c-type Ig domains”，而是一个更不直观的、由两段 Ig fold C 端半区互换形成的 elongated `beta-sandwich`。
- 论文给出了 `B43` 的识别表位，并解释了其对非人源物种缺乏交叉反应的原因。
- 这说明 CD19 的可结合表面和 loop/折叠关系，不能只凭序列编号想当然外推。

### 关键功能发现
- 本文重点是结构底图，不是 CAR 功能优化论文；它真正提供的是“CD19 外部拓扑不直观”这一底层约束。

### 工程改动
没有做 binder rescue；其价值在于提供结构参照系，让后续 `FMC63/SJ25C1/CAT` 的表位讨论有可靠底图。

### 对 CD19 lead rescue 的可复用启示
- 做 CD19 binder rescue 时，先尊重 `CD19` 的异常折叠，再谈 loop 改造或表位推断。
- 任何只靠序列编号、没有结构锚点的“拍脑袋表位解释”都应降权。
- 这篇论文是后续理解 `FMC63` 类 binder 为什么能共享部分表位、但几何又不同的结构前提。

### 证据与推断
#### 直接证据
- X-ray 结构直接揭示了 CD19 ectodomain 的异常拓扑与 `B43` 的识别方式。

#### 强推断
- CD19 binder 的功能差异，部分可能来自对这个“不按常规 Ig 逻辑排列”的表面几何的不同利用方式。

#### 开放问题
- `B43` 的结构信息为底图，但并不能单独推出 `FMC63` 的最佳 rescue 方向；仍需与 He 2023 和 Ghorashian 2019 的功能结果联读。
