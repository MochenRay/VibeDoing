# migration-notes

> 最近确认时间：2026-04-17

## 迁移原则

- 旧文件已归档到 `_legacy/`（2026-04-17），不再作为新系统真相源，仅保留作历史抽取素材。
- 保留旧课里仍跨时间成立的指标与实验方法。
- 把“AI PM 真正会被问到的评估能力”前置为主线。
- 把价格、固定阈值、默认值和快照类内容移出稳定层。

## 旧件位置

- `_legacy/初始文档.md`
- `掌握卡片/` 原为空目录，已删除

## 旧内容到新 schema 的映射

| 旧内容 | 新位置 | 处理方式 |
|---|---|---|
| 混淆矩阵、`Precision / Recall / F1` | `curriculum/concepts.md` + `curriculum/labs.md` | 保留 |
| 场景化指标选择 | `curriculum/concepts.md` + `curriculum/outcomes.md` | 保留并升级 |
| Token 成本计算 | `curriculum/volatile.md` | 移出主干 |
| 响应时间阈值 | `curriculum/volatile.md` | 移出主干 |
| A/B 测试 | `curriculum/concepts.md` + `curriculum/labs.md` | 保留 |
| 火灾预警综合方案 | `C1 capstone` 方向 | 重写为通用 AI / Agent 评估方案 |

## 新主线

1. 基础指标与 tradeoff
2. eval objective / dataset / metrics
3. workflow 与 retrieval eval
4. agent eval
5. launch readiness 与上线门槛
