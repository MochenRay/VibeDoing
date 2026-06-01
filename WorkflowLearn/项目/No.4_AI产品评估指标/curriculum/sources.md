# sources

> 最近确认时间：2026-06-01
> 状态：已记录 B3/B4 刷新方向，并补充安全评估来源

## 核心来源

- `初始文档.md`
- [OpenAI Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices)
- [OpenAI Working with evals](https://developers.openai.com/api/docs/guides/evals)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications)

## 2026-04-16 官方核验结论

- OpenAI 明确把 eval 读法组织成 `目标 -> 数据集 -> 指标 -> 对比 -> 持续迭代`，并要求结合 human judgment，而不是只看一个 0-1 分数。
- OpenAI 明确要求 eval 数据集覆盖典型样本、边缘样本、对抗样本，并建议把开发日志和生产日志沉淀成后续 eval case。
- OpenAI 把复杂度拆成 `single-turn / workflow / single-agent / multi-agent` 四类架构，说明评估必须跟着架构层级走，不能混成一张总分表。
- OpenAI 对 `LLM-as-judge` 的建议是：先用清晰 rubric 和人工标注校准，再决定是否放大自动评分规模。
- Anthropic 的 harness 文章补足了 agent eval 视角：长流程系统必须评估增量推进、artifact 留存、恢复能力和端到端验证，而不是只看最后是否“像完成了”。

## 当前结论

- 旧 `No.3` 里关于基础指标和 A/B test 的部分仍可保留。
- 旧 `No.3` 最大的问题是把课程中心放在“会算指标”，而不是“如何评估 AI / agent 系统”。
- 新稳定主干应围绕架构边界、数据集设计、持续评估和上线门槛，而不是围绕一张静态指标表。
- 2026-06-01 刷新方向：`B3` 应成为可复用 `launch gate / continuous eval / agent eval` 模板，覆盖 objective、dataset、metrics / rubric、comparison、human review、rollback 和 eval backlog。
- 安全评估应进入稳定主干，但具体 policy taxonomy、严重等级和拦截策略必须随平台与业务场景刷新。

## 首版迁移对应关系

- `基础指标`：来自旧文档第 2-3 节
- `Launch Readiness / A/B`：来自旧文档第 5-7 节，但做了结构重写
- `Agent / workflow evals`：新增主线，主要依据外部官方文档补入
- `Safety / policy evals`：2026-06-01 依据 NIST AI RMF 与 OWASP LLM 风险框架补入

## 后续需补的外部核验方向

- model-as-judge：模型裁判能力、rubric 校准与人工标注流程仍需按最新官方文档核验。
- continuous eval：线上日志回灌、回归样本管理、drift signal 与 eval backlog 的平台能力仍会变化。
- agent / tool-use eval：tool selection、argument correctness、handoff、状态恢复和多 agent trace 评估仍是 volatile 项。
- safety / policy evals：策略分类、严重失败 taxonomy、人工复核和阻断机制仍需 current-check。
- grounding / citation evals：引用一致性、证据覆盖和 hallucination 检测方法仍需按场景刷新。
