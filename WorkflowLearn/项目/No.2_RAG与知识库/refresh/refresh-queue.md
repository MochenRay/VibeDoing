# refresh-queue

> 最近确认时间：2026-06-01

## 待刷新

- `hybrid search / ranking / reranking`
  - `reason`: 召回与排序链路正在快速产品化，不同宿主默认能力差异大
  - `refresh_when`: 设计真实检索链路、做召回评估或比较平台方案时

- `query rewriting`
  - `reason`: 改写、扩展、过滤和多查询策略会直接影响召回，但实现方式变化快
  - `refresh_when`: 用户提问与文档表达差异较大，或需要解释召回失败时

- `citations / grounding 展示能力`
  - `reason`: 引用字段、inline citation、source span 和 UI 支持边界随平台变化
  - `refresh_when`: 写真实引用体验、fallback 或产品验收标准时

- `vector store cost / storage lifecycle`
  - `reason`: 存储、索引、检索调用、重建索引和保留周期都会影响方案取舍
  - `refresh_when`: 做 build / buy / assemble 决策或估算上线成本时

- `Embedding 模型选型`
  - `reason`: 厂商、效果、成本变化快
  - `refresh_when`: 做真实方案选型或成本估算时

- `向量数据库/服务推荐`
  - `reason`: 产品快照和生态变化快
  - `refresh_when`: 做 build / buy / assemble 决策时

- `评估指标阈值`
  - `reason`: 旧方案里的示例阈值需要按真实场景重算
  - `refresh_when`: 写 eval plan 或 launch gate 时

- `grounding / citations 的宿主支持边界`
  - `reason`: 不同平台的字段、展示和支持能力变化快
  - `refresh_when`: 要写真实引用体验或 UI 方案时

- `具体厂商默认值`
  - `reason`: chunk、Top-K、ranker、hybrid 权重、价格和 API 字段都属于时效层
  - `refresh_when`: 只有在真实选型或实现前才核验；课程稳定层只保留判断原则

- `Graph RAG / 知识图谱工具链`
  - `reason`: 图谱构建、实体抽取、关系索引和与向量检索的结合方式仍在快速产品化
  - `refresh_when`: 场景需要实体关系解释、路径推理或跨文档关系追踪时

- `agentic retrieval 实现模式`
  - `reason`: 何时检索、如何停止、query budget 和 trace 能力受平台与框架影响
  - `refresh_when`: 需要多轮检索、多源检索或 agent 自主决定检索策略时

## 已处理

- `chunk_size / overlap / Top-K 默认值`
  - `checked_on`: `2026-04-16`
  - `outcome`: 官方文档确认这些数值属于 API 默认和实验参数，不是稳定课程知识
  - `source`: [OpenAI Retrieval guide](https://developers.openai.com/api/docs/guides/retrieval)

- `RAG / Grounding 主线`
  - `checked_on`: `2026-04-16`
  - `outcome`: 已确认课程主线应围绕 retrieval、diagnosis、grounding、citations 和 fit judgment 组织

- `B3 RAG fit memo 方向`
  - `checked_on`: `2026-06-01`
  - `outcome`: B3 刷新为适用边界模块，重点比较 RAG、长上下文、搜索、工具调用和 workflow，并区分 retrieval / generation / tool / workflow failure
