# 今日任务

## 今天的唯一目标

把这个仓库从“空框架”推进到“首轮可读成果”。

## 今日完成标准

完成以下 5 项即收工：

1. 读完 `references/paper_list.md` 中 P0 的 2 篇论文
2. 产出 `cases/case_001_fmc63/intake.md`
3. 产出 `cases/case_001_fmc63/structure_notes.md`
4. 产出 `cases/case_001_fmc63/failure_hypotheses.md`（仅 3 条）
5. 更新 `progress.md`

## 今日执行顺序

### 步骤 1
先让 Codex 总结它读到了哪些指令文件。

建议提示词：

```text
先总结你当前读到的 repo 指令来源，并用 5 句话说明这个项目今天要做什么、明确不做什么。
```

### 步骤 2
处理 P0 论文中的第一篇：He 2023。

建议提示词：

```text
使用 $paper-intake 处理 references/paper_list.md 里的 He 2023。
输出到 cases/case_001_fmc63/intake.md。
重点抓：
1) FMC63 与 SJ25C1 的结合/结构信息
2) affinity tuning 如何改变功能
3) antigen density 与 binder 设计的关系
```

### 步骤 3
补 `structure_notes.md`。

建议提示词：

```text
基于 intake.md，写 cases/case_001_fmc63/structure_notes.md。
只保留对 lead rescue 有用的结构与机制信息。
不要写泛泛综述。
```

### 步骤 4
写第一版失败假设。

建议提示词：

```text
使用 $structure-critique，基于 FMC63 + He 2023 + Ghorashian 2019，
写出 3 条失败假设到 cases/case_001_fmc63/failure_hypotheses.md。
每条都必须包含：
- 假设本身
- 为什么会这样
- 证据来自哪里
- 置信度
- 最大未知点
```

### 步骤 5
更新进度。

建议提示词：

```text
更新 progress.md，写明今天已经完成什么、还缺什么、下一步做什么。
```

## 今日禁止事项

- 不扩展到其他靶点
- 不做 20 篇文献大综述
- 不开始 de novo 设计
- 不输出 50 个以上变体
- 不把推断写成结论

## 如果还有时间

只做这一件事：

开始起草 `variant_panel.md` 的骨架，但先不填满。
