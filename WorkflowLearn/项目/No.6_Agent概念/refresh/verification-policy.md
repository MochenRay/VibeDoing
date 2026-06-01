# verification-policy

> 最近确认时间：2026-04-16

## 项目级规则

### 可直接迁入 `concepts.md` 的内容

- Agent、Workflow、ReAct、Tool Contract、State、Harness、Observability 的稳定机制
- 可跨框架复用的设计原则与失败归因

### 必须进入 `volatile.md` 的内容

- 具体框架名、产品名、能力快照
- Computer Use 当前表现
- 官方文档里的默认值和演示结论

### 旧状态继承规则

- 旧“已掌握/已完成”不自动继承到新状态层
- 旧示例可迁入 `labs.md`，但必须去掉无法复核的聊天内容

### 必须回退的情况

- 结论依赖某家框架的当期功能表
- 无法分清 workflow 问题、工具问题、状态问题和组织问题
- 设计没有恢复路径或观测路径
