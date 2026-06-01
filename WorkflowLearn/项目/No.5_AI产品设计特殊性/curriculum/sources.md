# sources

> 最近确认时间：2026-06-01
> 状态：官方主线已补充并重写为当前课程依据

## 核心来源

- [OpenAI Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices)
- [Anthropic: Reduce hallucinations](https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/reduce-hallucinations)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [Gemini Prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [NIST AI RMF 1.0](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf)

## 2026-04-16 官方核验结论

- Anthropic 对减少幻觉的建议非常直接：允许模型说不知道、要求直接引用、要求带出处验证、找不到依据就撤回结论。
- Gemini 明确建议在近期事实或复杂计算场景中启用 grounding / code execution，这说明很多“信任问题”本质上是工具配置问题。
- OpenAI 继续把 edge cases、human judgment 和 continuous eval 放在正式评估主线里，这意味着 trust / fallback 不能脱离 eval 单独存在。
- NIST AI RMF 把 trustworthy AI 拆成 valid and reliable、safe、secure and resilient、accountable and transparent、explainable 等维度，这为风险分级和人工接管提供了稳定框架。
- Anthropic 的 harness 文章再次说明：失败体验不是 UI 小补丁，很多时候要回到 artifact、恢复、测试和 handoff 设计。

## 当前结论

- 稳定主干应围绕 `fallback / uncertainty / HITL / trust calibration / feedback loop`。
- 具体阈值和文案仍应留在 `volatile`。
- 某行业特有的接管策略只能用于案例，不应直接上升为通用主干。

## 2026-06-01 复核方向

- trust / fallback 仍应与 eval、grounding、artifact、handoff 和 incident review 绑定，而不是作为独立 UI 文案课处理。
- 当前需要补强的是行业化接管边界：同一模型表现，在不同行业下对应的人工确认、责任归属和上线门槛会不同。
- 后续案例应优先沉淀可转成 eval case 的反馈，而不是只记录用户满意度。
