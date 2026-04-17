# CD19 先导救援试点论文清单

## 使用说明

- **P0**：今天优先处理，足够支撑第一轮工作。
- **P1**：明后天补充，用来把排序逻辑变得更成熟。
- `Access` 只表示当前可访问形态：
  - 免费全文
  - 免费接收稿
  - 摘要 / 官方记录
  - 结构记录

---

## P0-1

### He et al., 2023
**CD19 CAR antigen engagement mechanisms and affinity tuning**

- 为什么重要：
  - 这是第一优先级。
  - 它把 **FMC63 / SJ25C1 结构、亲和力调节、antigen density、功能变化** 连成了一条线。
- 最佳用途：
  - `paper-intake`
  - `structure-critique`
- 获取方式：
  - 免费全文（PMC 记录）：https://pmc.ncbi.nlm.nih.gov/articles/PMC10228544/
  - 期刊官方记录：https://www.science.org/doi/10.1126/sciimmunol.adf1426
  - 结构记录（FMC63-CD19 示例）：https://www.rcsb.org/structure/7URV
- 阅读重点：
  1. FMC63 与 SJ25C1 的结合差异
  2. affinity tuning 如何改变 target density sensitivity
  3. 哪些结论来自结构，哪些来自功能实验

---

## P0-2

### Ghorashian et al., 2019
**Enhanced CAR T cell expansion and prolonged persistence in pediatric patients with ALL treated with a low-affinity CD19 CAR**

- 为什么重要：
  - 它让你建立“低 affinity 不一定更差”的第一性直觉。
  - 适合支撑“失败并不一定是因为绑得不够紧”的论证。
- 最佳用途：
  - `structure-critique`
  - later `variant-ranking`
- 获取方式：
  - 期刊官方页面：https://www.nature.com/articles/s41591-019-0549-5
  - 免费接收稿：https://discovery.ucl.ac.uk/id/eprint/10082596/
  - UCL 仓库直链 PDF：https://discovery.ucl.ac.uk/id/eprint/10082596/1/Amrolia%20CARPALLManuscript2ndrev5-19.pdf
- 阅读重点：
  1. 低 affinity binder 与 FMC63 的差异
  2. expansion / persistence / toxicity 逻辑
  3. 为什么“更强结合”不等于更好产品

---

## P0-3

### Seigner et al., 2023
**Solving the mystery of the FMC63-CD19 affinity**

- 为什么重要：
  - 用来校准你对 KD 数据的信任度。
  - 它会提醒你实验设计问题会把 affinity 结论带偏。
- 最佳用途：
  - `paper-intake`
  - supporting note for `variant-ranking`
- 获取方式：
  - 官方文章：https://www.nature.com/articles/s41598-023-48528-0
  - PubMed: https://pubmed.ncbi.nlm.nih.gov/38155191/
- 阅读重点：
  1. 为什么文献中的 FMC63 affinity 差异那么大
  2. 哪些实验设计会导致假高/假低结论
  3. 以后如何避免“只盯一个 KD 数字”

---

## P0-4

### Teplyakov et al., 2018
**Crystal structure of B-cell co-receptor CD19 in complex with antibody B43 reveals an unexpected fold**

- 为什么重要：
  - 它帮助你先认识 CD19 的外部结构与表位空间。
  - 很适合做结构层底图。
- 最佳用途：
  - `paper-intake`
  - `structure_notes`
- 获取方式：
  - 结构记录：https://www.rcsb.org/structure/6AL4
  - PubMed: https://pubmed.ncbi.nlm.nih.gov/29490423/
- 阅读重点：
  1. CD19 的外部结构有什么不直观之处
  2. B43 的表位位置与识别方式
  3. 这对后面理解 FMC63 类 binder 有什么帮助

---

## P1-1

### Sarén et al., 2023
**Complementarity-determining region clustering may cause CAR-T cell dysfunction**

- 为什么重要：
  - 用来防止你把 CDR 改造想得太简单。
  - 它提示：CDR 改动可能引发 clustering / tonic signaling 风险。
- 最佳用途：
  - `variant-ranking`
- 获取方式：
  - 官方文章：https://www.nature.com/articles/s41467-023-40303-z
- 阅读重点：
  1. CDR 为什么可能带来自聚集与 tonic signaling
  2. 为什么改 binding 不只是在改 affinity

---

## P1-2

### Shukla et al., 2025
**CAR Binders Affect CAR T-cell Tonic Signaling, Durability, and Sensitivity to Target**

- 为什么重要：
  - 用来强化排序逻辑：binder 不只是影响结合，还影响表面表达、durability 和低抗原识别能力。
- 最佳用途：
  - `variant-ranking`
- 获取方式：
  - 官方文章：https://aacrjournals.org/cancerimmunolres/article/13/6/867/762671/CAR-Binders-Affect-CAR-T-cell-Tonic-Signaling
  - PubMed: https://pubmed.ncbi.nlm.nih.gov/40298385/
- 阅读重点：
  1. 不同 binder 如何改变 tonic signaling 与 durability
  2. 为什么同样是 CD19，也不能把 binder 当可互换零件

---

## P1-3

### Warmuth et al., 2026
**Balancing the efficacy and safety of chimeric antigen receptor T-cell therapy by affinity combination**

- 为什么重要：
  - 用来让 `variant-ranking` 不只看 efficacy，而是同时看安全性和平衡性。
- 最佳用途：
  - `variant-ranking`
- 获取方式：
  - 官方文章：https://www.nature.com/articles/s41467-026-71354-7
- 阅读重点：
  1. affinity combination 为什么可能比单一极端更合理
  2. 排序时如何体现 efficacy/safety tradeoff
