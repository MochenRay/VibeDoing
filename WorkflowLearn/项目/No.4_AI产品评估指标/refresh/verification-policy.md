# verification-policy

> 最近确认时间：2026-04-16

## 可以进入 `concepts.md` 的内容

- 混淆矩阵与基础分类指标
- `objective -> dataset -> metrics -> continuous eval`
- workflow / retrieval 的分层评估思路
- agent 的工具选择、参数正确性、handoff 与 task completion
- 上线前的离线指标、在线护栏和人工接管框架

## 必须进入 `volatile.md` 的内容

- 具体阈值和 benchmark 快照
- model-as-judge 的厂商推荐
- 价格表和延迟表
- 厂商 eval 平台能力与默认值

## 验证顺序

1. 先判断内容是不是稳定方法，而不是时间点快照
2. 再判断它是单模型 eval、workflow eval 还是 agent eval
3. 最后才给出 go / no-go 或上线建议
