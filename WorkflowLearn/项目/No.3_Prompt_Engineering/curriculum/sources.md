# sources

> 最近确认时间：2026-06-01
> 状态：官方主线已补充并重写为当前课程依据

## 核心来源

- [OpenAI Structured Outputs](https://platform.openai.com/docs/guides/structured-outputs?lang=javascript)
- [OpenAI Tools](https://developers.openai.com/api/docs/guides/tools)
- [Anthropic Prompt engineering overview](https://docs.anthropic.com/en/docs/prompt-engineering)
- [Gemini Prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [MCP Architecture](https://modelcontextprotocol.io/docs/learn/architecture)
- [Vercel AI SDK: Generative User Interfaces](https://ai-sdk.dev/docs/ai-sdk-ui/generative-user-interfaces)
- [OpenAI Reasoning models](https://platform.openai.com/docs/guides/reasoning)
- [Anthropic Extended Thinking](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking)
- [Gemini Thinking](https://ai.google.dev/gemini-api/docs/thinking)

## 2026-04-16 官方核验结论

- Anthropic 把 prompt engineering 前提写得很明确：先定义 success criteria、测试方式和第一版 prompt，再谈调 prompt。
- Gemini 继续把 prompt engineering 定义成迭代过程，并明确建议复杂 JSON Schema 直接使用 structured output 特性，而不是只靠自然语言约束。
- OpenAI Structured Outputs 已把 `function calling` 和 `response_format` 的边界讲清楚：前者用于连接系统能力，后者用于约束模型对用户输出的结构。
- OpenAI Structured Outputs 还直接提供了 `Dynamically generated UI` 的 schema 示例，说明结构化输出已经可以直接服务 UI 生成。
- OpenAI Tools 文档已经把 built-in tools、function calling、tool search、remote MCP servers 放进同一条工具主线里。
- Vercel 的 Generative UI 文档明确把“工具结果 -> React 组件渲染”定义成一类 AI-native 交互，而不是把输出停留在长文本。

## 当前结论

- 稳定主干应围绕 `Prompt Brief -> Schema -> Tool Contract -> Guardrails -> UI Rendering`。
- 具体 API 细节、字段命名和宿主能力差异仍应放入 `volatile`。
- 任何单厂商 recipe 只能作为示例，不能反向变成课程主干。

## 2026-06-01 复核方向

- 工具、结构化输出、remote MCP 与 Generative UI 已经明显收束到同一条产品能力链：模型输出不只是文本，还会变成参数、工具调用和界面状态。
- 本课稳定层应继续讲 `behavior spec / schema / tool contract / UI descriptor / eval` 的关系；具体 SDK 写法、模型支持矩阵和宿主命名仍留在时效层。
- 后续案例要优先补 `prompt-tool-eval-pack`，避免把 prompt 课重新学成 prompt recipe。
- Reasoning / thinking 已进入主流模型调用界面；本课只吸收“目标、约束、输出合同、验证方式”这条稳定 prompt 设计原则，具体参数留在 `volatile`。
