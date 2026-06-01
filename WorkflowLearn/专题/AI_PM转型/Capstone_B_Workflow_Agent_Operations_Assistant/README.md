# Capstone B

> 最近确认时间：2026-06-01
> 状态：已对齐 No.6 workflow / agent / harness 刷新主线

## 主题

`Workflow Agent Operations Assistant`

当前默认样例是：`内部运营工单协同助手`。
它也可以平移成客服工单协调、销售运营任务协同、内部支持流程自动化等场景。

## 目标

用一套完整案例证明三件事：

- 你能判断什么时候该上显式 workflow，什么时候值得上 agent
- 你能把工具 contract / MCP 边界、状态、恢复、handoff 和 observability 做成完整运行方案
- 你能用 eval 和 rollout gate 判断 agent 是否能从“能演示”推进到“可讨论上线”

## 交付文件

### Core Delivery Layer

- [agent-vs-workflow.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/agent-vs-workflow.md)
- [product-spec.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/product-spec.md)
- [workflow-architecture-map.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/workflow-architecture-map.md)
- [tool-contract-pack.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/tool-contract-pack.md)
- [state-resume-scheme.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/state-resume-scheme.md)
- [long-running-harness.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/long-running-harness.md)
- [observability-blueprint.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/observability-blueprint.md)
- [agent-eval-pack.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/agent-eval-pack.md)
- [risk-handoff-design.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/risk-handoff-design.md)
- [launch-rollout-plan.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/launch-rollout-plan.md)

### Portfolio Layer

- [case-study.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/case-study.md)
- [presentation-script.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/presentation-script.md)
- [interview-qna.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/interview-qna.md)

## 课程映射

- `No.3`：Prompt / Schema / Tool Use
- `No.6`：Workflow vs Agent judgment / Tool contract / MCP / State-resume / Harness / Observability / Handoff / Eval
- `No.4`：Agent eval / Launch gate
- `No.5`：fallback、HITL、trust
- `No.7`：选型 / ROI / rollout

## 使用顺序

1. 先读 `agent-vs-workflow.md`
2. 再读 `product-spec.md` 和 `workflow-architecture-map.md`
3. 然后读 `tool-contract-pack.md`、`state-resume-scheme.md`、`long-running-harness.md`
4. 再读 `observability-blueprint.md`、`agent-eval-pack.md`、`risk-handoff-design.md`
5. 最后读 `launch-rollout-plan.md`，再用 `case-study.md`、`presentation-script.md`、`interview-qna.md` 做展示与面试准备

## No.6 对齐点

- `agent-vs-workflow.md` 先给出哪些环节保持 workflow、哪些环节需要 agent 判断。
- `tool-contract-pack.md` 只写稳定工具契约；具体宿主 MCP 支持和工具目录形态进入刷新层。
- `state-resume-scheme.md`、`long-running-harness.md`、`observability-blueprint.md` 共同证明长流程可恢复、可观测、可接手。
- `agent-eval-pack.md` 决定是否需要多 agent，而不是默认把流程拆成多个角色。

## 标准地位

本目录是当前 `capstone-standard` 的第二个正式实例。
后续 `Capstone C / D / E` 应继续复用同一结构。
