# sources

> 最近确认时间：2026-06-01
> 状态：官方主线已补充并重写为当前课程依据

## 核心来源

- `初始文档.md`
- `学习路径.md`
- `掌握卡片/P1-P3, A1-A2, B1-B2`
- `项目信息.md`
- [OpenAI Retrieval guide](https://developers.openai.com/api/docs/guides/retrieval)
- [Anthropic Citations](https://docs.anthropic.com/en/docs/build-with-claude/citations)
- [Gemini Grounding with Google Search](https://ai.google.dev/gemini-api/docs/grounding/)

## 2026-04-16 官方核验结论

- OpenAI Retrieval guide 明确说明 `chunk_size / overlap / max_num_results / score_threshold / ranker / hybrid_search` 都是可调参数，默认值不等于稳定原则。
- OpenAI Retrieval 还表明现代 retrieval 不止是“分块后查向量库”，还包括 query rewriting、filtering、ranking 和 hybrid search 等中间层能力。
- Anthropic 的 citations 功能说明了“带出处回答文档问题”已经是正式能力簇，这支持把 citation experience 视为 RAG 产品设计的一部分。
- Gemini 的 grounding 文档直接把 grounding 的价值写成 `reduce hallucinations + access real-time information + provide citations`，并给出 `groundingMetadata` 这类可用于构建 inline citations 的结构。
- 这意味着稳定主干不该只讲“怎么检索”，还要讲“怎么把检索结果变成可验证、可展示、可追责的用户体验”。

## 当前结论

- `chunk_size / overlap / Top-K` 这类数值首先是产品默认或实验参数，不是稳定知识。
- 稳定知识应该保留为：按文档类型、业务目标、检索失败模式与评估样本来决定切分和检索策略。
- `query rewriting / filtering / ranking / hybrid search` 说明现代 retrieval 不是只背一个固定默认值。
- `RAG` 不是纯后端检索问题，也包含 citation、grounding 和 fallback 的产品表达问题。
- `B3` 应升级为可复用的适用边界判断：比较 RAG、长上下文、搜索、工具调用和 workflow，而不是默认把所有知识问题都归入 RAG。

## 2026-06-01 刷新方向

- 本次不新增未核验外部 citation，只记录课程刷新方向。
- 当前需要持续刷新的主线是：hybrid search、ranking / reranking、query rewriting、citations、vector store cost。
- 具体厂商默认值、API 字段、价格和性能数字不进入稳定概念层，继续放在 `volatile.md` 或刷新队列中。
- B3 的稳定表达应聚焦 fit judgment 与 failure boundary：先判断是否需要检索，再区分 retrieval、generation、tool 和 workflow failure。

## 首版迁移对应关系

- `P1/P2/P3`：桥接层与数据质量认知
- `A1/A2`：RAG 流程与语义检索原理
- `B1/B2`：离线策略与在线诊断
- `B3`：当前来自 `初始文档.md`，后续需要补案例化验证

## 后续需补的外部核验方向

- retrieval eval
- reranking
- query rewriting
- grounding / citation patterns
- agent retrieval patterns
- vector store cost and storage lifecycle
