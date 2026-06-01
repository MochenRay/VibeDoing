# State / Resume Scheme

> 最近确认时间：2026-04-16

## 必要状态字段

- `ticket_id`
- `workflow_stage`
- `tool_calls_completed`
- `pending_tools`
- `risk_level`
- `evidence_refs`
- `draft_resolution`
- `handoff_status`
- `last_checkpoint`

## 检查点

1. 工单分类完成
2. 关键工具调用完成
3. 建议处理方案生成
4. 风险判断完成
5. 已提交人工接管或已关闭

## 恢复规则

- 从最近一个完成检查点恢复
- 如果关键工具结果过期，先重查再继续
- 如果已进入人工审批，不重复跑 agent 主流程

## 中断场景

- API 超时
- 权限不足
- 工单在处理中途被人工接管
- 高风险动作等待确认
