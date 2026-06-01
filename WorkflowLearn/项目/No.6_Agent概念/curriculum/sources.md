# sources

> 最近确认时间：2026-06-01
> 状态：稳定主线已刷新，供应商细节保留在时效层

## 核心来源

- `初始文档.md`
- `掌握卡片/*.md`
- [ReAct paper](https://arxiv.org/abs/2210.03629)
- [MCP Architecture](https://modelcontextprotocol.io/docs/learn/architecture)
- [Anthropic: Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [OpenAI Tools](https://developers.openai.com/api/docs/guides/tools)
- [Gemini API Docs](https://ai.google.dev/gemini-api/docs)

## 2026-06-01 刷新方向

- ReAct 仍然是 agent loop 的经典起点，但今天更重要的不是会不会“思考再行动”，而是能不能把 tool call、state 和恢复设计清楚。
- MCP Architecture 继续作为工具协议化的稳定来源；具体宿主支持、连接方式和 registry 形态进入刷新队列。
- 长流程 harness 继续作为 agent 可交付性的主线：initializer、tool registry、progress artifact、checkpoint、恢复和测试要一起设计。
- Tool registry / hosted tools / computer use 属于产品形态快速变化层，只用于提示刷新方向，不写成长期断言。
- 多 Agent 协作只作为 eval 后的升级方案；稳定课程先讲 handoff、owner、冲突处理和责任边界。

## 当前结论

- 稳定主干应围绕 `agent vs workflow judgment -> tool contract -> state / resume -> harness -> observability -> handoff`。
- 具体框架名、平台可用性和 demo 快照属于时效层，不进入长期主干。

## 后续需补的外部核验方向

- 主流宿主 MCP 支持状态与连接边界
- tool registry / tool search / hosted tool 的产品形态
- long-running harness 的测试与恢复实践
- multi-agent coordination 的 eval 证据与适用边界
- Computer Use 的权限、安全和人工接管边界
