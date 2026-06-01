# labs

> 最近确认时间：2026-06-01
> 状态：已强化 AI feature eval、agent workflow eval 与 launch gate 模板

## Lab 1：AI Feature Eval Plan

- 目标：把一个 AI 功能从“感觉不错”改写成可复用 eval plan。
- 交付物：`ai-feature-eval-plan.md`
- 必须包含：
  - `objective`
  - `target users / risky users`
  - `dataset sources`
  - `metrics / rubric`
  - `baseline / candidate comparison`
  - `human review`
  - `continuous eval backlog`
  - `go / no-go`
- 通过条件：读者能据此直接开跑第一轮离线评估。

## Lab 2：RAG / Workflow Scorecard

- 目标：为一个 retrieval 或 workflow 系统拆出分层 scorecard。
- 交付物：`scorecard-rag-workflow.md`
- 必须包含：
  - 检索层指标
  - 生成层指标
  - 工具调用准确性
  - 失败归因路径
  - 线上监控指标
- 通过条件：能回答“问题出在 retrieval、generation、tooling 还是 orchestration”。

## Lab 3：Agent Workflow Eval Plan

- 目标：为一个带工具调用、状态流转和 handoff 的 agent 设计正式 workflow eval plan。
- 交付物：`agent-workflow-eval-plan.md`
- 必须包含：
  - tool selection
  - argument correctness
  - handoff / escalation
  - state / artifact recovery
  - task completion
  - regression cases
  - drift signals
  - human review
  - severe failure taxonomy
- 通过条件：评估不再只看最终答案，而能覆盖工具误用、循环 handoff 和恢复失败。

## Lab 4：Launch Gate Template

- 目标：把离线评估、线上护栏和人工接管翻译成可复用上线门槛。
- 交付物：`launch-gate-template.md`
- 必须包含：
  - launch objective
  - 离线达标线
  - baseline comparison
  - 在线护栏指标
  - safety / policy checks
  - 人工接管条件
  - 回滚条件
  - 下一轮 eval backlog
- 通过条件：评审者能据此做一次真实 go / no-go 决策。

## Lab 5：基础指标手算补充

- 目标：保留传统指标功底，但只作为局部能力。
- 交付物：`metric-notes.md`
- 必须包含：
  - `Precision / Recall / F1`
  - 每个指标对应的业务风险说明
  - 为什么这些指标不足以单独代表 AI 产品质量
- 通过条件：能把指标解释成业务风险语言，而不是只会背公式。

## 常见错误

- 只拿一个分数当全部结论
- 把 workflow 错误都归成“模型不行”
- 只看离线质量，不看上线护栏
- 对 agent 只看完成率，不看工具误用与失败模式
- 上线后不回灌失败样本，导致回归和漂移无法被持续发现
