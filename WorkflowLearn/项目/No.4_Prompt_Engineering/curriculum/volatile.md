# volatile

> 最近确认时间：2026-04-16
> 状态：时效项已按官方主线重判

## 继续留在时效层的内容

- 具体厂商的 structured output API 名称
- 具体厂商的 tool calling / function calling 语法
- 具体 SDK 的参数字段与默认值
- Thinking Mode / reasoning mode 的宿主命名
- MCP、schema、tool 参数在不同宿主里的落地差异
- 当前版本的 prompt cookbook / recipe 示例

## 2026-04-16 官方抽检结果

- OpenAI 明确区分 `function calling` 和 `response_format`，但具体参数名和 SDK 写法仍会变化。
- OpenAI Tools 明确存在 built-in tools、tool search 和 remote MCP servers；哪些模型支持哪些工具、哪些宿主支持哪些桥接，是时效层问题。
- Gemini 把 structured outputs、function calling、long context、Computer Use、File Search 并列成能力入口，这说明能力簇本身稳定，但页面结构和具体限制会继续变化。
- Vercel 的 Generative UI 也在快速演进实现方式，稳定的是“把 tool result 接进 UI”，不是某个具体 hook 或组件协议。

## 当前判断

- 这些内容适合写进 adapter、示例代码或刷新队列，不适合写进稳定概念层。
- 稳定主干只保留“什么时候用 prompt、什么时候上 schema、什么时候定义 tool contract、什么时候渲染 UI”。
