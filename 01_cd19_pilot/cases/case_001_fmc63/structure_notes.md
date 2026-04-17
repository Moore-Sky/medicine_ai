# 结构笔记

仅保留对 `CD19 / FMC63 lead rescue` 有帮助的结构与机制信息。

## 1. CD19 的结构底图

- `Teplyakov 2018` 显示，CD19 ectodomain 不是按序列直觉可预测的两个串联常规 Ig 域，而是更异常的 `elongated beta-sandwich` / domain-swapped 拓扑。
- 这意味着：只按序列位置谈“某个 loop 应该朝外/朝里”风险很高，CD19 的表位解释必须尽量依赖已解结构。
- 对 lead rescue 来说，这个底图的价值不是直接给出变体，而是防止后续把错误的结构想象当成工程前提。

## 2. FMC63、SJ25C1 与 CAT 的表位关系

- `He 2023` 直接给出 `FMC63-CD19` 与 `SJ25C1-CD19` 复合物结构。
- `FMC63` 主要抓 `loop 1 (154-166)` 与 `loop 2 (214-224)`，由 `VH` 主导，`VL` 提供补充接触。
- `SJ25C1` 与 `FMC63` 共享部分表位，但在 CD19 表面近似旋转约 `90°`，且更明显利用 `loop 3 (95-109)`。
- `Ghorashian 2019` 的 CD19 loop 突变结果进一步支持：`CAT` 与 `FMC63` 是“重叠表位 + 不同微观接触”的关系，而不是完全无关的结合模式。

## 3. 哪些残基/区域更像 rescue 抓手

- `He 2023` 指出，`FMC63` 的重要接触热点集中在少数 CDR 位点，文中直接测试了 `Y70`、`Y260`、`Y261` 等位点的弱化突变。
- 同一论文中，`SJ25C1` 的 `W52`、`I120` 一类位点也能在“不完全丢失结合”的前提下改变功能阈值。
- 这支持一个工程直觉：首轮 rescue 更适合做“少数热点位点的小步调参”，而不是一上来重写整段 CDR。

## 4. Affinity 不是单一答案，测量本身也会骗人

- `Seigner 2023` 说明 `FMC63` 文献 `KD` 分布可从 `0.3 nM` 到 `47 nM`，差异大到不能直接拿来横比。
- 主要 artefact 包括：
  - 未充分达到平衡
  - ligand depletion
  - interaction partner 构型/多价带来的 avidity
- 因此，本项目里看到任何 `FMC63 KD`，都要先问 assay 背景，再决定能否与别家数据并排比较。
- 更稳妥的当前基线是：`FMC63` 大致处于低 nM 量级，而不是某一个绝对数字。

## 5. 结构如何连接到功能

- `He 2023` 的关键信息不是“弱一点更好”或“强一点更好”，而是 binder affinity/geometry 会改写 `antigen density threshold`。
- 适度弱化的变体在高 / 中 CD19 density 下仍可维持杀伤，但在低 density 下更容易拉开差距。
- 更弱的 binder 往往伴随更低的 `trogocytosis`；但如果 affinity 降得过头，则会连细胞因子释放和总体杀伤一起掉下去。
- 这意味着 rescue 的真正目标更像是“调工作窗口”，不是单向追求更低或更高 affinity。

## 6. 对 FMC63 rescue 的首轮工程含义

- 首选方向应是 `FMC63` 重叠表位上的温和调参，而不是默认换到完全陌生表位。
- 更值得盯的是 `koff / dwell time / density sensitivity`，而不是只盯单个 `KD`。
- `Ghorashian 2019` 支持“更快松手但不脱靶”的 binder 可能换来更好的 expansion / persistence。
- 当前 P0 证据还不足以直接判断 `tonic signaling`、`developability`、`manufacturability` 谁最好，因此第一轮结论只能到“优先假设”，不能写成已验证事实。

## 7. 证据拆分

### 直接证据
- CD19 存在异常 ectodomain fold。
- `FMC63`、`SJ25C1`、`CAT` 与 CD19 处于重叠但不完全相同的识别空间。
- 温和 affinity 弱化可改变低抗原密度识别、trogocytosis 与部分功能 readout。
- `FMC63` 的绝对 affinity 数值高度依赖 assay 设计。

### 强推断
- `FMC63` 若存在产品层面的“过敏感/过占据”问题，最现实的 rescue 方向不是继续加紧，而是做有限降敏。
- `KD` 相近也不等于产品行为相近，因为几何、停留时间和表位微差都可能改写功能。

### 未决问题
- `FMC63` 的哪些局部位点最适合优先进入小面板，仍需下一步失败假设来收敛。
- 目前证据尚不能单独区分：哪些风险来自 affinity，哪些来自几何，哪些来自 CAR 构型背景。
