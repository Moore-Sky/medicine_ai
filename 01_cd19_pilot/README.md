# 面向 Codex 的 CD19 先导救援试点

## 这个项目是干什么的

这是一个 **面向 Codex 的最小可执行试点仓库**。

目标不是“直接设计新药”，也不是“今天就做出临床候选物”。

目标是先把下面这条工作流跑通：

**公开论文 → 结构理解 → 失败解释 → 小面板改造建议 → 可交付证据包**

第一枪固定为：

- **靶点：CD19**
- **场景：CAR binder / antibody lead rescue 演练**
- **默认 benchmark binder：FMC63**

## 为什么选 CD19

因为 CD19 这条线上：

- 已有成熟临床产品与公开临床讨论
- 有公开结构信息（B43–CD19、FMC63/SJ25C1–CD19）
- 有“亲和力不是越高越好”的明确案例
- 有关于 tonic signaling、durability、antigen density 的成熟讨论

这意味着：

1. 适合练 **paper-intake**：把论文压成标准案例卡。
2. 适合练 **structure-critique**：解释现有 lead 为什么“差一点”。
3. 适合练 **variant-ranking**：不是只看 affinity，而是按功能/风险/可制造性排序。

## 这个项目要达到什么效果

本项目的验收目标不是实验成功，而是**方法论跑通**。

### 最低交付物

1. 读完并整理 4 篇核心论文
2. 对 1 个 benchmark binder 写出 3 条失败假设
3. 提出 6–10 个聚焦改造方向
4. 对每个改造方向给出：
   - 机制理由
   - 预期收益
   - 主要风险
   - 优先级
5. 形成一份 `evidence_pack.md`

### 你真正想积累的能力

不是“背会免疫学名词”，而是积累下面三层知识：

#### 1. 靶点与结构层

- CD19 外部结构是什么样
- 关键表位大致在哪些 loop/区域
- 不同 binder 是否共享或部分重叠表位
- 结合几何和 antigen density 阈值可能怎样影响功能

#### 2. 工程与机制层

- 为什么高 affinity 不一定更优
- 为什么 binder 会影响 tonic signaling / durability
- 为什么 CDR 改动可能带来 clustering 或 developability 风险
- 为什么排序不能只按 KD

#### 3. 产品化与服务层

- 如何把论文解读压成案例卡
- 如何把“失败解释”写成客户能看懂的话
- 如何把变体建议收敛成小面板，而不是漫无边际地生成序列
- 如何形成一个像样的证据包（evidence pack）

## 今天怎么执行

按 `TODAY.md` 走，不要自己扩题。

今天只做四件事：

1. 让 Codex 读懂这个 repo 的边界
2. 先收核心论文
3. 先做第一张案例卡
4. 写出第一版 3 条失败假设

## 使用方式

### 方式 A：在 CLI / IDE 中直接让 Codex 开工

从 repo 根目录打开 Codex，然后发：

```text
先阅读 AGENTS.md、TODAY.md 和 references/paper_list.md。
今天不要扩题，只做 CD19/FMC63 的第一轮 paper-intake。
先处理 references/paper_list.md 中优先级 P0 的论文，产出：
1) cases/case_001_fmc63/intake.md
2) cases/case_001_fmc63/structure_notes.md
3) progress.md 更新
```

### 方式 B：显式调用 skills

```text
使用 $paper-intake 处理 He 2023 这篇论文，输出到 cases/case_001_fmc63/intake.md
```

```text
使用 $structure-critique 基于 FMC63 + He 2023 + Ghorashian 2019，写 3 条失败假设到 cases/case_001_fmc63/failure_hypotheses.md
```

```text
使用 $variant-ranking 对 6 个候选改造思路做排序，输出到 cases/case_001_fmc63/variant_panel.md
```

```text
使用 $evidence-pack 将 intake/structure/failure/panel 整理为客户版证据包，输出到 cases/case_001_fmc63/evidence_pack.md
```

## 当前明确不做的事

- 不做 pMHC
- 不做全新 de novo 抗体设计
- 不做湿实验方案细化
- 不做动物实验路线
- 不做临床申报策略承诺
- 不做“无限生成序列”的大海捞针

## 一句话定义这个 pilot

**用 Codex 把 CD19 公开知识压成一个可复用的 lead-rescue 工作流。**
