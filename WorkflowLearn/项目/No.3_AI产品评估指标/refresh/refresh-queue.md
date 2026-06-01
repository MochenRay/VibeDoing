# refresh-queue

> 最近确认时间：2026-06-01

## 待刷新

- `model-as-judge 选型`
  - `reason`: 高度依赖 judge 模型能力、rubric 质量、人工标注校准和平台工具链
  - `refresh_when`: judge 模型、评分 API 或标注流程发生变化

- `continuous eval 运行机制`
  - `reason`: 线上日志回灌、回归集维护、drift signal、eval backlog 与 trace 平台能力变化快
  - `refresh_when`: 准备把课程模板用于真实上线门槛或监控设计时

- `agent / tool-use eval`
  - `reason`: tool selection、argument correctness、handoff、状态恢复、多 agent trace 的评估口径仍在快速演进
  - `refresh_when`: 设计 agent workflow eval plan 或 agent launch gate 时

- `safety / policy evals`
  - `reason`: 策略分类、严重失败 taxonomy、人工复核和阻断机制依赖最新产品与平台政策
  - `refresh_when`: 功能涉及高风险内容、自动执行、用户数据或外部工具调用时

- `示例阈值与 benchmark 快照`
  - `reason`: 不同任务和不同风险等级会直接改写阈值含义
  - `refresh_when`: 切换场景、切换架构或准备上线新产品时

- `厂商 eval 平台能力`
  - `reason`: 平台接口、默认 grader 和 trace 视图变化快
  - `refresh_when`: 需要真实选型或写平台对比时

- `延迟 / 成本经验值`
  - `reason`: 产品、模型、工具调用和部署环境变化快
  - `refresh_when`: 做 launch gate 或 ROI 评审时

## 已处理

- `B3 launch gate 刷新方向`
  - `checked_on`: `2026-06-01`
  - `outcome`: 已确认本课 B3 应从指标讲解升级为可复用 `launch gate / continuous eval / agent eval` 模板；外部产品能力和政策细节仍保留在待刷新项

- `AI / Agent Evals 主线`
  - `checked_on`: `2026-04-16`
  - `outcome`: 已用官方来源确认新主线应围绕 eval workflow、架构边界、持续评估与 launch readiness 组织

- `静态指标表中心化`
  - `checked_on`: `2026-04-16`
  - `outcome`: 已确认静态指标表不再作为课程中心，只保留为局部方法
