# state

> 最近确认时间：2026-06-01

## 当前状态

- `status`: a4_reasoning_models_pending_teaching
- `current_module`: A4 Reasoning Models 已补入课程，待首轮教学验证；A1/A2/A3/B2 已通过
- `last_verified`: 2026-06-01
- `next_action`: 先完成 A4 Reasoning Models 讲解与验证，再决定是否继续 No.2 B3
- `teaching_phase`: lecture
- `round`: 0
- `concept_type`: n/a
- `error_count`: 0
- `fallback_reason`: none
- `review_due`: 2026-05-14
- `review_count`: 0
- `last_reviewed`: not_started

## 已通过模块复习队列

- `A1 Token 与上下文窗口`：首轮通过 2026-05-13，首次复习 due 2026-05-14；后续 2026-05-16 / 2026-05-20 / 2026-05-27
  - 待强化：论述时不要漏成本维度
- `A2 Temperature 与采样`：首轮通过 2026-05-13，首次复习 due 2026-05-14；后续 2026-05-16 / 2026-05-20 / 2026-05-27
  - 待强化：正面场景更具体；"低温=准确"修正为"低温=稳定"
- `A3 模型幻觉与成因`：首轮通过 2026-05-13，首次复习 due 2026-05-14；后续 2026-05-16 / 2026-05-20 / 2026-05-27
  - 待强化：错误根因区分检索层 vs 注意力层；高风险场景不漏人工审核
- `B2 大模型工作原理概述`：首轮通过 2026-05-13，首次复习 due 2026-05-14；后续 2026-05-16 / 2026-05-20 / 2026-05-27
  - 待强化：格式→微调 / 语气安全→RLHF 的归因线反复混淆；费曼中要补"训练好了也不会自查"

## stale_items

- `B1` 的模型快照、价格、上下文窗口属于高频漂移内容，不进入稳定层。
- reasoning 模型对 temperature、reasoning effort、thinking budget、计费和上下文占用的具体行为在快速变化中，需按厂商文档周期核实。

## blocked_items

- 暂无。
