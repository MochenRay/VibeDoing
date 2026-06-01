# Observability Blueprint

> 最近确认时间：2026-04-16

## 必看面板

- 当前工单状态
- tool call 次数与失败率
- handoff 触发率
- 平均处理时长
- 恢复次数

## 必留日志

- route decision
- tool input / output
- risk score
- state checkpoint
- handoff artifact

## 错误分类

- route error
- tool error
- state error
- policy / permission error
- hallucinated recommendation
- handoff failure

## 目的

- 出现问题时能快速知道错在 workflow、tool、state 还是人审边界
- 不再靠人工猜“它为什么表现怪”
