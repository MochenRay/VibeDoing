# capstone-standard

> 最近确认时间：2026-04-16

## 1. 目的

`capstone-standard` 定义 `WorkflowLearn` 里专题综合案例包的标准形态。

它解决的是：

- 什么情况下应该从单课产出升级成 capstone
- 一个 capstone 至少该包含哪些文件
- 如何把案例同时做成“学习证明”与“作品集资产”
- 后续 `Capstone B / C / D / E` 应该如何复用同一标准

## 2. 适用范围

这个标准适用于：

- 专题目录下的综合案例包
- 跨至少 `3` 门课程的组合式案例
- 需要同时证明产品判断、系统设计、评估与失败处理能力的作品

它不适用于：

- 单门课内部的普通练习
- 只记录思考过程、没有交付意图的草稿
- 系统内核文档

## 3. 何时升格为 Capstone

满足以下条件时，应该从单课 `labs/outcomes` 升格成 capstone：

1. 已经跨课程。
2. 已经不只是概念说明，而是完整方案。
3. 已经包含上线判断或失败处理。
4. 已经值得进入作品集或面试讲解。

## 4. 标准结构

每个 capstone 分成三层：

### 4.1 Core Delivery Layer

证明“你真的会做”。

最小文件集：

1. `README.md`
2. `fit-memo.md` 或等价决策 memo
3. `product-spec.md`
4. `architecture-map.md` 或等价系统图
5. `eval-plan.md`
6. `risk / fallback / trust design.md`

### 4.2 Portfolio Layer

证明“你能讲出来，而且别人看得懂”。

最小文件集：

1. `case-study.md`
2. `presentation-script.md`
3. `interview-qna.md`

### 4.3 Optional Extension Layer

按主题自由加，但不能替代前两层。

可选文件示例：

- `roi-note.md`
- `roadmap.md`
- `demo-script.md`
- `ui-brief.md`
- `ops-runbook.md`

## 5. README 的职责

每个 capstone 的 `README.md` 必须承担：

- 主题说明
- 使用顺序
- 交付文件索引
- 课程映射
- 这个案例想证明什么

它不是重复正文，而是导航页。

## 6. 命名规则

推荐目录形态：

```text
专题/<topic>/Capstone_<letter>_<slug>/
```

例如：

- `Capstone_A_Grounded_Knowledge_Assistant`
- `Capstone_B_Workflow_Agent_Operations_Assistant`

字母只是当前阶段的展示顺序，不代表最多只能有 `A/B/C`。
如果后续专题需要继续扩展，完全可以有 `D / E / F`，前提是它们各自对应不同的能力主线或作品定位。

## 7. 质量标准

一个合格 capstone 必须满足：

- 读者不看聊天记录也能理解
- 不是一堆散文件，而是能串成一个完整案例
- 能同时回答“为什么做”“怎么做”“怎么验证”“失败怎么办”
- 至少有一份文件可以直接拿去做作品集主案例

## 8. 当前标准原型

当前第一份标准原型是：

- `专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/`

后续 `Capstone B / C / D / E` 应在不破坏本标准的前提下扩展，而不是重新发明目录和产物结构。
