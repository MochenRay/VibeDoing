# Launch and Rollout Plan

> 最近确认时间：2026-04-16

## Phase 1：Shadow Mode

- 只生成建议
- 不影响真实工单结果
- 人工对比 agent 建议与真实处理

## Phase 2：Low-risk Assisted Mode

- 仅覆盖低风险工单
- 人工点击确认后执行
- 开始统计处理时长、返工率、人工否决率

## Phase 3：Expanded Rollout

- 扩展到更多工单类型
- 强化 observability 和 incident review
- 明确值班和回滚责任人

## 回滚条件

- 路由错误率显著升高
- 人工否决率过高
- 高风险 handoff 漏触发
- 关键工具调用错误持续出现
