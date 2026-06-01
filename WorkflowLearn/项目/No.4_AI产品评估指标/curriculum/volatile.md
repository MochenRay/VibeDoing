# volatile

> 最近确认时间：2026-04-16
> 状态：时效内容已按官方主线重判

## 继续留在时效层的条目

- 旧文档中的模型价格和 Token 成本表
- 旧文档中的固定响应时间分档
- 示例型分数阈值、目标值和 benchmark 快照
- 具体 model-as-judge 选型
- 厂商 eval 产品能力与默认设置

## 2026-04-16 官方抽检结果

- OpenAI 会给任务示例里的参考阈值和 grader 做法，但这些都依赖任务目标、标注方法和风险承受度，不能抽成通用常数。
- OpenAI 把 `LLM-as-judge` 明确写成“先校准再放大”的策略，这意味着 judge 模型选择和 rubric 配置天然属于时效层。
- OpenAI 把 agent / workflow 的 edge cases 写到了评估正文里，包括多工具参数错误、多 agent handoff 和长对话噪音，这类 failure mix 会随产品架构变化。
- Anthropic 明确指出 harness 里的 feature list、progress file、端到端验证方法都来自当前工程约束，后续会继续演化。

## 当前判断

- 稳定的是 `objective / dataset / rubric / scorecard / launch gate` 这套方法，不是某个固定分数线。
- 价格、延迟、默认值、示例阈值和 benchmark 只能当学习当期快照维护，不进入长期主干。
- model-as-judge、benchmark 和厂商 eval 平台会继续变化，必须继续留在时效层。
