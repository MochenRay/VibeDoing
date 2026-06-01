# No.4_AI产品评估指标 交接页

> 最近确认时间：2026-06-01

## 当前判断

这个项目已经不再只是“会算 Precision / Recall”的指标课，而是 `AI / Agent Evals` 的核心模块。

2026-06-01：个人学习进度已重置。本项目课程材料保留，但不继承此前任何教学验证或案例通过状态。

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
- 课程材料保留；个人学习通过记录已清空

## 下一步

1. 待 No.1-No.3 完成后，从 `P1 为什么 AI PM 需要 evals` 开始首轮讲解。
2. 后续再把 `B3/B4` 扩成一份可复用的上线评审模板。
