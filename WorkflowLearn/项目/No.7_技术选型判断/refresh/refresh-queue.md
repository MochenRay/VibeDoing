# refresh-queue

> 最近确认时间：2026-06-01

## 待刷新

- `模型价格与上下文窗口`
  - `reason`: 厂商会持续调价、换默认模型、调整上下文与输出上限
  - `refresh_when`: 做真实选型、预算评审或 PRD 成本估算时

- `benchmark 排名与分数`
  - `reason`: 榜单更新快，而且与真实业务目标不直接等价
  - `refresh_when`: 需要做模型 shortlist 时

- `vendor-specific 能力和默认推荐`
  - `reason`: 能力簇和推荐模型变化快
  - `refresh_when`: 需要做供应商对比或 build vs buy 时

- `成本测算示例`
  - `reason`: token、工具/搜索/检索、缓存、存储、人工审核、监控、rollout 和调用模式会影响总成本
  - `refresh_when`: 做 ROI 或 pricing hypothesis 时

- `fine-tune 能力、价格和替代路径`
  - `reason`: fine-tune 的可用模型、训练/推理成本、数据要求和与 RAG / prompt / tool use 的替代关系变化快
  - `refresh_when`: 把 fine-tune 写入正式方案、预算或 roadmap 前

- `build / buy / assemble vendor 对比`
  - `reason`: 现成平台、托管工具、检索能力和集成边界会持续变化
  - `refresh_when`: 做供应商 shortlist、采购评审或自研边界判断时

- `vendor lock-in 与迁移成本`
  - `reason`: API、数据格式、eval 工具、权限、日志、价格和合同条款都会改变切换成本
  - `refresh_when`: 准备签供应商、采用托管向量库、agent 平台或专有工具链时

- `多模态产品能力快照`
  - `reason`: 图像、语音、视频能力和质量边界变化快
  - `refresh_when`: 需要做 AI-native surface 选型时

## 已处理

- `solution routing / vendor lock-in 稳定主线`
  - `checked_on`: `2026-06-01`
  - `outcome`: 已补入稳定层；具体供应商能力、折扣、合同条款和迁移工具仍留在刷新队列

- `技术选型主线`
  - `checked_on`: `2026-04-16`
  - `outcome`: 已确认课程主线应围绕任务形态、风险、工具链、总成本、build/buy/assemble 和 rollout 组织
