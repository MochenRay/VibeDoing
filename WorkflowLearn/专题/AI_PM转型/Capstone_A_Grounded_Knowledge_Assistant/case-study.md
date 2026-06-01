# Case Study

> 最近确认时间：2026-04-16
> 用途：作品集主案例正文

## 一句话概述

我设计了一个 `城市治理知识助手`，目标是在高风险政策问答场景里，用 `RAG + grounding + citations + fallback` 取代“只会回答、不会举证”的普通聊天问答。

## 背景

城市治理与政务服务场景里，工作人员需要快速查：

- 政策法规
- 办事指南
- SOP
- 历史处置案例

传统搜索的主要问题不是“搜不到字”，而是：

- 用户提问和政策表述经常不一致
- 文档分散在多个系统
- 政策版本会变
- 用户必须知道依据来自哪里，才能继续执行

## 核心判断

这个问题适合 `RAG`，但不适合“只有检索、没有验证”的简陋知识问答。

原因是：

- 问题本质是在找已有知识
- 知识会更新
- 结论必须可追溯
- 高风险场景里，错误自信比直接说不知道更危险

## 我做的方案

我把产品拆成三层：

- `data layer`：清洗、分块、元数据、版本管理、索引
- `answer layer`：query rewrite、retrieval、ranking、grounded generation
- `trust layer`：citations、版本提示、不确定性提示、fallback、人工接管

核心不是“把文档塞给模型”，而是让系统能回答三个问题：

1. 检到的依据对不对
2. 回答有没有忠实反映依据
3. 如果依据不够，系统会不会老实收窄或转人工

## 这套方案的亮点

### 1. 把 citation 做成产品主路径

不是回答后随便挂几个参考链接，而是让关键结论能逐条对应到出处。

### 2. 把 fallback 做成系统层能力

当版本冲突、证据不足或问题高风险时，系统不应该硬答，而应该切到：

- constrained answer
- 相近依据提示
- human handoff

### 3. 把 eval 前置

我不是只写了产品 spec，还同时写了：

- retrieval layer eval
- answer layer eval
- trust layer eval
- offline go / no-go
- online guardrails

## 这套案例证明了什么能力

- 我能判断什么时候该上 RAG，什么时候不该上
- 我能把 RAG 做成带引用、可验证、可接管的产品
- 我能把系统设计、风险控制和上线门槛一起讲清楚

## 如果继续迭代

下一步我会继续补：

- 版本冲突数据集
- citation 可读性测试
- 高风险问题的人审 workflow
- 更细的 query rewrite case
