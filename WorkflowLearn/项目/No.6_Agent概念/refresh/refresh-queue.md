# refresh-queue

> 最近确认时间：2026-06-01

## 待刷新

- `Computer Use 的产品可用性与能力边界`
  - `reason`: 平台支持、权限模型、确认机制和安全边界变化快
  - `refresh_when`: 需要做真实桌面自动化、浏览器 agent 或高风险操作方案时

- `MCP 与主流宿主的支持状态`
  - `reason`: 协议主线稳定，但宿主支持范围、remote MCP、认证和连接方式变化快
  - `refresh_when`: 需要真实接入 MCP server、remote MCP、connectors 或企业工具时

- `Tool registry / hosted tools / tool search`
  - `reason`: 工具发现、启用、权限和审计方式与具体 runtime 强绑定
  - `refresh_when`: 需要设计工具市场、内部工具目录或动态工具发现时

- `agent 框架生态`
  - `reason`: 框架名、默认抽象和推荐实践变化快
  - `refresh_when`: 需要做 build vs use 框架决策时

- `多 Agent 协作实现趋势`
  - `reason`: 管理者-专家、多角色 handoff、共享状态和任务拆分模式仍在演进
  - `refresh_when`: eval 显示单 agent / workflow 不足，需要写多角色 orchestration 方案时

- `长流程 harness 最新实践`
  - `reason`: 跟可用工具、状态管理、checkpoint、恢复和测试能力强绑定
  - `refresh_when`: 设计长任务 runtime、恢复机制或上线 gate 时

## 已处理

- `Agent / Workflow 主线`
  - `checked_on`: `2026-06-01`
  - `outcome`: 已确认课程主线应围绕 workflow vs agent judgment、tool contract / MCP、state / resume、long-running harness、observability、HITL / handoff 和 eval 组织
