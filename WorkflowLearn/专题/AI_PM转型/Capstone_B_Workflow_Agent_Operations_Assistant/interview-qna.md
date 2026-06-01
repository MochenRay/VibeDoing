# Interview Q&A

> 最近确认时间：2026-04-16
> 用途：围绕 Capstone B 的标准答题资产

## 1. 为什么这里不是纯 workflow

因为工单描述和实际路径存在大量不确定性。
如果全部硬编码成流程，会导致维护成本高、覆盖不足、例外处理很差。

## 2. 为什么也不是全自由 agent

因为很多动作有权限和副作用边界。
如果让 agent 全自由决定，很容易越过审批、误用工具，或者在故障后无法恢复。

## 3. 你的核心架构判断是什么

`workflow-first + agentic substeps`

也就是：

- 主路径由显式 workflow 固定
- 动态理解和信息整合交给 agent
- 高风险节点回到人工和规则流

## 4. 你觉得这类 agent 产品最重要的设计点是什么

不是 prompt，而是：

- tool contract
- state / resume
- handoff
- observability

如果这四个点没设计好，系统最多只能做 demo。

## 5. 你怎么判断这个系统值不值得上

看三件事：

- 当前流程是否真的有高频重复劳动
- 例外情况是否足够多，值得加入 agentic 判断
- 组织是否有能力承接 handoff、值班和回滚

## 6. 你怎么评估这种系统

我会分层评估：

- workflow route accuracy
- tool argument correctness
- resolution usefulness
- safety / handoff correctness

不会只看最终完成率。

## 7. 这套案例最能证明你什么能力

- 我能判断 agent 和 workflow 的边界
- 我能把运行层能力设计清楚
- 我能把上线和运营问题一起纳入产品设计
