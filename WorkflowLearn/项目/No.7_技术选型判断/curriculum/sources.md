# sources

> 最近确认时间：2026-06-01
> 状态：已补充成本结构、tool/search/caching 与 fine-tune 当前核验方向

## 核心来源

- `初始文档.md`
- `掌握卡片/*.md`
- [OpenAI Tools](https://developers.openai.com/api/docs/guides/tools)
- [OpenAI Retrieval](https://developers.openai.com/api/docs/guides/retrieval)
- [OpenAI Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices)
- [OpenAI API Pricing](https://openai.com/api/pricing)
- [Anthropic Models overview](https://docs.anthropic.com/en/docs/about-claude/models/overview)
- [Gemini API Models](https://ai.google.dev/gemini-api/docs/models)
- [Gemini Developer API pricing](https://ai.google.dev/gemini-api/docs/pricing)

## 2026-04-16 官方核验结论

- OpenAI Pricing 已把 token 价格和 built-in tools 分开列出，说明成本核算不能只算输入输出 token。
- Gemini Pricing 也把 grounding with Google Search、context caching 这类能力单列出来，说明 retrieval / tool use 会直接影响 unit economics。
- OpenAI Retrieval 仍把 retrieval / file search 当作一条正式工具路线，而不是外挂技巧。
- Anthropic 与 Gemini 的模型页都把 structured outputs、tool use、long context、agent / tool models 作为正式能力簇展示，说明选型时必须把“模型能力”和“工具 / 运行时能力”一起看。
- OpenAI Evaluation best practices 再次强调：最终该不该上线，取决于任务目标、风险和评估结果，而不是只看 benchmark 排名。

## 当前结论

- 选型不是只看模型，而是看任务类型、知识形态、风险和组织成本。
- `Prompt / RAG / Workflow / Agent / Fine-tune` 都是工具，不是宗教。
- 成本核算必须同时纳入 token、tool、搜索/检索、缓存、存储、人工复核、监控、rollout 和运营成本。
- build / buy / assemble 判断要落到“哪一层形成差异化、哪一层买现成、哪一层组合”的结构化取舍。
- fine-tune 只能作为需当前核验的候选路径；稳定课程层只保留判断框架，不固化厂商价格、模型名单或默认推荐。
- 任何 vendor-specific 的价格或能力判断，都应该归入时效层。

## 后续需补的外部核验方向

- build vs buy
- assemble / integration cost patterns
- ROI modeling
- launch / rollout patterns
- organization / SOP integration
- fine-tune capability, pricing and replacement paths
