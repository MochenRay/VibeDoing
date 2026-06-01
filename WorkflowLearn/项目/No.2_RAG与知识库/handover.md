# No.2_RAG与知识库 交接页

> 最近确认时间：2026-04-16

## 当前判断

这个项目已经可以作为 `M3 Retrieval / Grounding` 的正式课程入口。
当前完成的是第一轮稳定内容迁移，不代表所有旧内容都已经过外部核验。

## 已冻结决策

1. `P1/P2/P3/A1/A2/B1/B2` 先作为稳定主干迁入
2. `B3` 适用边界保留在课程主线里，但后续要补更系统的案例判断
3. `C1` 定位为 capstone，而不是一般概念节点
4. embedding 产品、向量数据库产品、固定 chunk 默认值不直接写进稳定层
5. `C1` 默认拆成 `product spec + eval plan + fallback / citation design` 三个可交付物

## 未决问题

1. `B3` 是先做单独判断清单，还是直接嵌进 `C1` 的 pre-read

## 当前产出

- `project.md`
- `handover.md`
- `state.md`
- `migration-notes.md`
- `curriculum/*.md`
- `refresh/*.md`
- `P1/P2/P3/A1/A2/B1/B2` 的首版内容迁移
- `labs.md` 与 `outcomes.md` 的首版作品模板
- `C1` 默认样例已冻结为 `城市治理知识助手`
- `Capstone A` 首版案例包已落盘到 `专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/`

## 下一步

1. 把 `B3` 做成可直接复用的 `RAG fit memo`
2. 继续细化 `C1` 的 eval plan 与 fallback 细节
3. 对 `volatile` 里的 embedding、产品快照、指标阈值做下一轮外部核验
