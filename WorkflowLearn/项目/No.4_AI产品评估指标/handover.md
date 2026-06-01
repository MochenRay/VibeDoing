# No.4_AI产品评估指标 交接页

> 最近确认时间：2026-06-01

## 当前判断

这个项目已经不再只是“会算 Precision / Recall”的指标课，而是 `AI / Agent Evals` 的核心模块。
当前完成的是第一轮结构重写，目标是让 AI PM 能写出可落地的评估方案、上线门槛和 agent 质量判断。

## 已冻结决策

1. 混淆矩阵与 `Precision / Recall / F1` 继续保留，但只作为入门层。
2. 课程中心改成 `objective -> dataset -> metrics -> compare -> continuous eval`。
3. workflow 和 agent 的评估必须单列出来，不再只讲单模型输出质量。
4. 旧文档中的价格表、固定阈值、静态响应时间表不进入稳定概念层。
5. launch readiness 必须同时覆盖离线指标、在线护栏和人工接管。

## 未决问题

1. B4 安全评估如何与 B3 launch gate 合并成一份正式上线评审模板。
2. `C1` capstone 是先做 `AI 应用评估方案`，还是先做 `Agent workflow 评估方案`。

## 当前产出

- `project.md`
- `handover.md`
- `state.md`
- `migration-notes.md`
- `curriculum/*.md`
- `refresh/*.md`
- `A1/A2/B1/B2/B3/B4` 的首版内容迁移

## 下一步

1. 把 `B3/B4` 扩成一份可复用的上线评审模板。
2. 为 `C1` 设计两个 capstone 题目：`AI feature eval plan` 和 `agent workflow eval plan`。
3. 对 `volatile` 里的模型裁判、示例阈值和 benchmark 快照做下一轮外部核验。
