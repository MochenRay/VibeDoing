# Workflow Architecture Map

> 最近确认时间：2026-04-16
> 目标：说明 workflow、agentic step、handoff 和 observability 的结构

```mermaid
flowchart LR
  T["工单输入"] --> C["分类与字段抽取"]
  C --> R["主 workflow 路由"]
  R --> Q["查询类工具"]
  R --> D["规则 / SOP 检索"]
  R --> A["agentic substep: 汇总与判断"]
  Q --> A
  D --> A
  A --> P["建议处理方案"]
  P --> L["低风险: 人工确认后执行"]
  P --> H["高风险: 自动 handoff"]
  A --> O["运行日志 / traces / state"]
  H --> O
  L --> O
  O --> E["eval / incident review / backlog"]
```

## 层次

### Workflow Layer

- 工单分类
- 路由
- 权限与审批边界

### Agentic Layer

- 摘要
- 多来源信息整合
- 例外判断

### Safety Layer

- 高风险动作拦截
- 人工接管
- 证据打包

### Runtime Layer

- state
- traces
- error taxonomy
- replay / recovery
