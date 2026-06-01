# Presentation Script

> 最近确认时间：2026-04-16
> 用途：5-8 分钟讲解稿

## 开场

这个项目不是“让 agent 帮运营自动干活”这么简单，而是设计一套 `Workflow Agent Operations Assistant`。
我的核心目标是：在多系统工单处理中，让 agent 负责该负责的动态判断，但不越过审批、权限和恢复边界。

## 问题

运营工单处理里常见几个痛点：

- 工单描述混乱
- 需要查多个系统
- 规则复杂且有例外
- 高风险动作必须审批

如果只做纯 workflow，会太僵硬。
如果直接做全自由 agent，会难以控制风险。

## 我的判断

所以我选择：

- `workflow-first`
- `agentic substeps`
- `human handoff for high-risk`

这个判断的关键不是技术时髦度，而是要兼顾：

- 灵活性
- 可控性
- 可恢复性
- 可观测性

## 我的方案

我把案例拆成几块：

- tool contract
- state / resume
- long-running harness
- observability
- agent eval
- launch / rollout

所以这不是一份“AI 能力畅想”，而是一份运行系统方案。

## 怎么判断它能不能上线

我不是只看完成率，而是看：

- route accuracy
- tool correctness
- handoff accuracy
- human rejection rate
- rollback trigger

也就是说，我把上线门槛和回滚条件前置了。

## 这套案例证明的能力

它证明我可以从 PM 视角把：

- workflow 设计
- agent 设计
- 安全边界
- 可观测与运维

放进一个完整产品方案里。
