# Case Study

> 最近确认时间：2026-04-16
> 用途：作品集主案例正文

## 一句话概述

我设计了一套 `内部运营工单协同助手`，目标不是让 agent 自由乱跑，而是用 `workflow-first + agentic substeps` 提升跨系统工单处理效率，同时保持可恢复、可观察和可接管。

## 背景

运营工单常见问题是：

- 问题描述不标准
- 需要查多个系统
- 流程有 SOP，但存在例外
- 高风险操作必须审批

所以最难的不是“会不会回答”，而是：

- 能不能正确选工具
- 能不能在中途中断后恢复
- 能不能在高风险时老实 handoff

## 核心判断

这里不适合纯 workflow，也不适合全自由 agent。

我最终选择的是：

- 主路径显式 workflow
- 局部动态决策交给 agentic substeps
- 高风险节点强制回到人工和规则流

## 我做的方案

这套方案包含：

- tool contract pack
- state / resume scheme
- long-running harness
- observability blueprint
- agent eval pack
- launch / rollout plan

换句话说，我不是只回答“能不能做”，而是同时回答：

- 怎么做
- 怎么恢复
- 怎么观察
- 怎么评估
- 怎么上线

## 这套方案的亮点

### 1. 把 state 当成产品能力

不是把状态隐藏在 agent 内部，而是显式设计 checkpoint、handoff 和 replay。

### 2. 把 tool contract 做成安全边界

不同工具按只读、可回滚、高风险分类，避免所有动作都默认可自动执行。

### 3. 把 observability 前置

让故障从“感觉它怪怪的”变成可追踪的 route error、tool error、state error、handoff failure。

## 这套案例证明了什么能力

- 我能判断什么时候该上 agent
- 我能把 runtime、state、tools 和 handoff 串起来
- 我能把 agent 从 demo 设计成可上线讨论的系统
