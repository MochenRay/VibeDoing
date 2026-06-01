# refresh-queue

> 最近确认时间：2026-06-01
> 状态：待刷新项已按宿主和示例边界重写

## 待刷新项

- `structured output API 变化`
  - `reason`: API 名称、参数和兼容模型会变化
  - `refresh_when`: 写示例代码或 adapter 时

- `tool calling / function calling 语法变化`
  - `reason`: 宿主和 SDK 写法变化快
  - `refresh_when`: 做工具集成 demo 或 host adapter 更新时

- `Thinking / reasoning mode 命名变化`
  - `reason`: 命名、支持模型、effort / budget 档位和默认值是宿主实现，不是稳定课程概念
  - `refresh_when`: 对比不同宿主行为时

- `MCP 落地能力变化`
  - `reason`: 各宿主支持范围和连接方式会变化
  - `refresh_when`: 需要真实接入 remote MCP 或 connector 时

- `prompt cookbook / recipe 推荐变化`
  - `reason`: cookbook 属于实践快照，不是课程主干
  - `refresh_when`: 更新示例题或模版库时

- `prompt / tool eval 样本与判分方式`
  - `reason`: tool use、schema 输出和 UI descriptor 的失败模式会随产品架构变化
  - `refresh_when`: 做真实 demo、Capstone B/C 或上线前回归评估时

- `prompt caching 能力与计费`
  - `reason`: 缓存窗口、命中规则、可缓存内容、隐私边界和价格随平台变化
  - `refresh_when`: 真实方案依赖长系统提示、长工具说明或重复上下文时

- `流式 / 置信度 UX 模式`
  - `reason`: 宿主 UI、模型延迟、引用能力和风险提示规范都会影响具体体验
  - `refresh_when`: 设计面向用户的生成过程、部分结果或高风险输出状态时

## 处理规则

- 只刷新会影响宿主适配或示例代码的内容
- 不把价格表、模型榜单、短期实践写回稳定层
- 如果某项只影响某个宿主，就写回 adapter，不回写 core
