# sources

> 最近确认时间：2026-06-01
> 状态：已补充 AI-native surface、feedback telemetry 与 eval-aware operation 刷新方向

## 核心来源

- `初始文档.md`
- `掌握卡片/*.md`
- [OpenAI Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices)
- [OpenAI Working with evals](https://developers.openai.com/api/docs/guides/evals)
- [OpenAI Structured Outputs](https://platform.openai.com/docs/guides/structured-outputs?lang=javascript)
- [Vercel AI SDK: Generative User Interfaces](https://ai-sdk.dev/docs/ai-sdk-ui/generative-user-interfaces)
- [Anthropic Prompt engineering overview](https://docs.anthropic.com/en/docs/prompt-engineering)
- [Gemini Prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies)
- [Gemini API Models](https://ai.google.dev/gemini-api/docs/models)

## 2026-04-16 官方核验结论

- Vercel 的官方文档已经把 generative UI 定义成“模型超越文本、通过工具结果生成界面”，这支持把 AI-native surface 单独作为课程主线。
- OpenAI Structured Outputs 直接给出了 `Dynamically generated UI` 的 schema 示例，说明 UI descriptor 已经可以作为正式输出形态，而不是只靠 Markdown 文本。
- Gemini 的官方文档把 structured outputs、function calling、long context、Computer Use、File Search 放在一个能力簇里，说明 AI-native surface 选择和工具/模态能力绑定很深。
- Anthropic 继续强调先定义 success criteria 和测试方式，再迭代 prompt，这说明 AI-native feature 仍然需要 `eval-aware product design`。
- OpenAI 的 eval 文档继续把 continuous eval、human judgment 和 launch gate 当成正式流程，说明 AI-native 功能也不能跳过上线守门。

## 当前结论

- AI Native PM 的核心不是追单一模型能力，而是把 `surface / feedback / eval / fallback` 连成闭环。
- surface 选择要区分 chat、copilot、inline edit、canvas / workbench、voice / live / multimodal，而不是把所有 AI 功能都收进聊天框。
- 多模态与原生交互的产品价值，必须通过任务摩擦、信息类型、下一步动作、反馈采集和验证方式来判断。
- feedback telemetry 应能进入 eval dataset，并成为 launch readiness、回滚和迭代优先级的证据。
- 任何 vendor-specific 的能力快照都应进入时效层。

## 后续需补的外部核验方向

- multimodal surfaces
- voice / live interaction surfaces
- feedback loop / telemetry patterns
- trust / handoff patterns
- launch readiness for AI native features
- eval-aware product operations
- generative UI and workbench patterns
