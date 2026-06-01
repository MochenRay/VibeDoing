# sources

> 最近确认时间：2026-06-01
> 状态：官方主线已补充并重写为当前课程依据

## 核心来源

- `初始文档.md`
- `掌握卡片/*.md`
- `学习报告.md`
- [Anthropic Token counting](https://docs.anthropic.com/en/docs/build-with-claude/token-counting)
- [Anthropic Context windows](https://docs.anthropic.com/en/docs/build-with-claude/context-windows)
- [Gemini Understand and count tokens](https://ai.google.dev/gemini-api/docs/tokens)
- [Gemini Long context](https://ai.google.dev/gemini-api/docs/long-context)
- [Anthropic Reduce hallucinations](https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/reduce-hallucinations)
- [Lost in the Middle](https://arxiv.org/abs/2307.03172)
- [OpenAI Reasoning models](https://platform.openai.com/docs/guides/reasoning)
- [Anthropic Extended Thinking](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking)
- [Gemini Thinking](https://ai.google.dev/gemini-api/docs/thinking)

## 2026-04-16 官方核验结论

- Anthropic 与 Gemini 都把 token 计数写成正式能力，说明 token 不只是成本概念，还直接影响长度控制、模型路由和工具输入预算。
- Anthropic 把 context window 明确定义成“working memory”，并直接提醒更多上下文不自动等于更好；随着 token 增长会出现 accuracy / recall 下降。
- Gemini 的 long-context 文档也把 context 比作短期记忆，并说明即便有超长上下文，RAG、摘要和过滤在特定场景里仍然有价值。
- `Lost in the Middle` 仍然是理解长上下文局限的关键论文，支持“塞得下不等于用得好”这条稳定判断。
- Anthropic 对幻觉治理的建议非常稳定：允许模型承认不知道、先抽原文引用、要求带出处验证、找不到依据就撤回结论。

## 2026-06-01 Reasoning Models 核验结论

- OpenAI 已把 reasoning effort 明确写成模型调用参数，并说明更高 effort 会增加延迟和 token 使用。
- Anthropic Extended Thinking 与 Gemini Thinking 都把 thinking budget / thinking level 作为开发者需要管理的能力，而不是单纯提示词技巧。
- OpenAI 与 Gemini 都明确指出 reasoning / thinking tokens 可能对用户不可见，但会进入输出 token、上下文或计费统计。
- 因此 `Reasoning Models` 应进入 No.1 稳定主干；具体参数名、支持模型和默认值继续放在时效层。

## 当前结论

- `A1/A2/A3/A4/B2` 这类机制性内容可以继续作为稳定学习主干。
- `B1 主流模型对比` 只能保留为时效层或求职前速查材料，不能再作为长期稳定课程正文。
- 如果未来需要恢复“模型选型”章节，应按当时官方页面即时生成，而不是回收旧表格。
- `No.1` 的真正价值不是介绍模型名单，而是建立一套后续所有课程都会复用的边界语言。

## 后续可补的外部核验方向

- next-token prediction 的更底层论文锚点
- 采样与随机性的更直接官方解释
- 多模态 token 预算与上下文预算
- reasoning effort / thinking budget 的厂商参数、默认值和计费细节
- 时效性模型对比

## 首版迁移对应关系

- `A1`：`初始文档.md` 第 2-3 节 + `掌握卡片/A1. Token与上下文窗口.md`
- `A2`：`初始文档.md` 第 4 节 + `掌握卡片/A2. Temperature与采样.md`
- `A3`：`初始文档.md` 第 5 节 + `掌握卡片/A3. 模型幻觉与成因.md`
- `A4`：2026-06-01 依据 OpenAI / Anthropic / Gemini 官方 reasoning / thinking 文档新增
- `B2`：`初始文档.md` 第 7 节 + `掌握卡片/B2. 大模型工作原理概述.md`
