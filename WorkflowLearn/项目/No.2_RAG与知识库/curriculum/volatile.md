# volatile

> 最近确认时间：2026-04-16
> 状态：首版时效内容已归档，默认值相关条目已做官方抽检

## 当前条目

- 具体 embedding 模型选型结论
- 具体向量数据库产品或服务商推荐
- 固定 `chunk_size / overlap / Top-K` 默认值
- 初始文档中的示例指标阈值
- 任何与某家框架、厂商能力、性能数字绑定的结论
- grounding / citations 的具体 API 结构与产品支持边界

## 2026-04-16 官方抽检结果

- OpenAI Retrieval guide 当前默认切分是 `800 / 400`，但文档同时明确支持自定义 `chunking_strategy`。
- 同一份官方文档里，默认结果数、`score_threshold`、`ranker`、`hybrid_search` 权重也都是可调参数。
- 这说明旧项目里写死的 `chunk_size 500-1000`、`Top-K = 5` 只能算历史经验，不是稳定原则。
- Anthropic citations 与 Gemini grounding 都在演进具体字段、宿主支持和 UI 呈现方式，因此这部分仍应留在时效层。

## 当前判断

- `chunk_size 500-1000`、`Top-K = 5` 这类说法只能作为旧经验，不是稳定原则
- 稳定原则是“按文档类型和业务目标调粒度”，不是记住某个默认值
- 生产阈值需要结合场景、知识库体量和评估样本重新核验
- `embedding`、数据库选型和评估阈值仍然需要单独做外部核验，当前不升格
- grounding / citation 的具体能力边界也要按宿主和当期平台重新核验
