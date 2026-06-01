# 第一批 Capstone 组合

> 最近确认时间：2026-06-01
> 状态：首版组合已冻结

## 目的

这份文档把 `No.1-No.8` 中已经整理好的模块，组合成第一批可直接产出的正式案例包。
目标不是“把课程学完”，而是尽快形成能用于作品集、面试和案例讲解的成套交付物。

## 组合原则

- 每个 capstone 必须跨至少 `3` 门课，不做单课孤立作业。
- 每个 capstone 必须同时包含：产品判断、系统结构、评估方案、失败处理。
- 第一批 capstone 优先覆盖 `AI 应用 PM` 和 `Agent / Workflow PM` 两个方向。

## Capstone A：Grounded Knowledge Assistant

### 定位

- 面向 `AI 应用 PM`
- 主题：知识助手 / 政策问答 / 企业知识搜索

### 主要来自

- `No.1`：LLM 边界说明
- `No.2`：RAG / Grounding 主线
- `No.3`：Prompt / Schema / Tool Use，负责回答合同、引用结构与可验证输出
- `No.4`：Eval / Launch Readiness
- `No.5`：Fallback / HITL / Trust

### 最小交付包

1. `rag-fit-memo.md`
2. `product-spec.md`
3. `knowledge-architecture-map.md`
4. `eval-plan.md`
5. `grounding-citation-design.md`
6. `fallback-citation-design.md`

已落盘到：
`专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/`

并已扩成当前标准原型：

- `Core Delivery Layer`
- `Portfolio Layer`

### 核心证明能力

- 你能判断为什么这里该上 RAG。
- 你能把 retrieval 做成带引用、可验证、可接管的产品，而不是只会画向量库架构。
- 你能把上线门槛和失败处理一起讲清楚。

## Capstone B：Workflow Agent Operations Assistant

### 定位

- 面向 `Agent / Workflow PM`
- 主题：内部流程自动化 / 多步骤任务协同 / 工具编排

### 主要来自

- `No.3`：Prompt / Schema / Tool Use
- `No.6`：Agent / Workflow / Harness Engineering
- `No.4`：Agent eval / Launch gate
- `No.5`：HITL / fallback
- `No.7`：技术选型与 rollout

### 最小交付包

1. `agent-vs-workflow.md`
2. `product-spec.md`
3. `workflow-architecture-map.md`
4. `tool-contract-pack.md`
5. `state-resume-scheme.md`
6. `long-running-harness.md`
7. `observability-blueprint.md`
8. `agent-eval-pack.md`
9. `risk-handoff-design.md`
10. `launch-rollout-plan.md`

已落盘到：
`专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/`

### 核心证明能力

- 你能判断什么时候该上显式 workflow，什么时候值得上 agent。
- 你能把 tool contract、state、handoff 和 observability 做成完整运行方案。
- 你能把 agent 从 demo 拉到 production 讨论。

## Capstone C：AI-native Copilot Feature

### 定位

- 兼顾 `AI 应用 PM` 与 `AI Native PM`
- 主题：Copilot / Inline Edit / Tool-driven UI / 多模态工作台

### 主要来自

- `No.3`：Prompt / Schema / Generative UI
- `No.8`：AI-native surface / feedback / multimodal
- `No.5`：Trust / fallback / HITL
- `No.7`：ROI / 产品化决策

### 最小交付包

1. `ai-native-feature-spec.md`
2. `surface-selection.md`
3. `ui-brief.md`
4. `multimodal-flow.md`
5. `feedback-loop-blueprint.md`
6. `eval-plan.md`
7. `fallback-trust-design.md`
8. `launch-readiness.md`
9. `pricing-or-roi-note.md`

已落盘到：
`专题/AI_PM转型/Capstone_C_AI_Native_Copilot_Feature/`

### 核心证明能力

- 你能把 AI 输出设计成可继续操作的 surface，而不只是聊天框。
- 你能同时讲体验、反馈闭环、上线门槛和商业约束。
- 你能解释为什么这个 feature 是 AI-native，而不是“加了个聊天功能”。

## 建议顺序

1. 先做 `Capstone A`
2. 再做 `Capstone B`
3. 最后做 `Capstone C`

这个顺序的原因是：

- `Capstone A` 最容易把 `No.1-No.5` 串起来，适合作为第一件完整作品。
- `Capstone B` 对 runtime、state、observability 要求更高，适合作为第二件硬核作品。
- `Capstone C` 更适合在前两件作品基础上，做体验与产品化升级。

## 当前冻结决定

- `No.2/C1` 直接并入 `Capstone A`
- `No.3` 进入 `Capstone A` 的 Prompt / Schema / Tool Use 能力映射，但不新增孤立交付物；其内容落在 `product-spec.md`、`eval-plan.md`、`grounding-citation-design.md` 和 `fallback-citation-design.md`
- `No.6` 作为 `Capstone B` 的主干
- `No.8` 作为 `Capstone C` 的主干
- 第一批作品集的首版主干已经形成 `A + B + C`
- 其中 `A / B` 仍是主案例，`C` 作为 AI-native 体验与产品化强化案例
