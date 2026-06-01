# No.3_AI产品评估指标

> 最近确认时间：2026-04-16
> 状态：首版稳定内容已迁移

## 用途

本文件是 `No.3_AI产品评估指标` 在新 `WorkflowLearnSystem` schema 下的项目首页。
当前项目已从“通用指标课”重写为 `AI / Agent Evals` 的正式课程入口。

## 目标

- 为 `M4 Evals / Launch Readiness` 提供正式课程落点。
- 保留旧课里仍有价值的基础指标，但把主线切换为 AI / Agent 系统评估。
- 把时效快照、产品默认值和示例阈值单独隔离到 `volatile` 与刷新队列。

## 范围

- `project.md`
- `handover.md`
- `state.md`
- `curriculum/*.md`
- `refresh/*.md`
- `migration-notes.md`

## 非范围

- 不修旧项目的历史进度
- 不把旧价格表、模型快照或硬编码阈值写进稳定主干
- 不把 `No.5` 的 fallback / trust 细节全部吞并进来

## 成功标准

- `AI / Agent Evals` 主干已经迁入 `curriculum/`
- 混淆矩阵等基础指标降为入门层，而不是课程中心
- agent / workflow / launch readiness 已有明确课程落点

## 当前状态

- 2026-04-16：已完成第一轮重写，当前主线覆盖 `基础指标 -> eval 设计 -> workflow / agent eval -> launch readiness`
- 旧 `初始文档.md` 保留为参考材料，不再作为正式课程结构
