# labs

> 最近确认时间：2026-06-01
> 状态：作品模板已扩写

## Lab 1：Knowledge Architecture Map

- 目标：为一个知识助手画出离线与在线链路。
- 交付物：`knowledge-architecture-map.md`
- 必须包含：文档来源、分块、索引、检索、生成、引用展示、反馈入口
- 通过条件：读者能一眼看出系统哪里是 data layer，哪里是 answer layer

## Lab 2：Chunking Strategy Memo

- 目标：为三类文档写一份分块策略 memo。
- 交付物：`chunking-strategy-memo.md`
- 必须包含：政策法规、SOP、FAQ/案例库三类文档的切分单位与元数据
- 通过条件：不会用一套固定参数走天下

## Lab 3：Retrieval Diagnosis SOP

- 目标：写一份 `检索错误 vs 生成错误` 的诊断 SOP。
- 交付物：`retrieval-diagnosis-sop.md`
- 必须包含：定位顺序、常见误判、引用检查、后台观测点
- 通过条件：能把错误归因到检索、生成、数据质量或表达层

## Lab 4：Grounding and Citation Design

- 目标：把“回答正确”升级成“回答可验证”。
- 交付物：`grounding-citation-design.md`
- 必须包含：引用样式、版本提示、查看依据入口、无法给出处时的 fallback
- 通过条件：用户可以追踪关键结论来自哪里

## Lab 5：RAG Fit Memo

- 目标：判断一个场景到底该不该上 RAG，并形成可复用的适用边界 memo。
- 交付物：`rag-fit-memo.md`
- 必须包含：知识依据、更新频率、查询类型、引用需求、替代方案、失败归因边界
- 必须比较：RAG、长上下文、搜索、tool use、workflow、纯模型
- 通过条件：能说明何时适合 RAG，何时更适合 long context / search / tool use / workflow，并能区分 retrieval / generation / tool / workflow failure
- Capstone 映射：直接作为 `Capstone A / rag-fit-memo.md` 的第一版输入

## Lab 6：C1 Capstone Pack

- 目标：完成 `城市治理或企业知识助手` 的正式 capstone 包。
- 交付物：
  - `product-spec.md`
  - `eval-plan.md`
  - `fallback-citation-design.md`
- 必须包含：知识源设计、引用体验、失败归因、上线门槛、人工接管
- 通过条件：这三份产物可以一起进入作品集，而不是只是一篇概念说明

## Lab 7：Data Readiness Checklist

- 目标：判断一个知识助手是否具备上线前的数据基础。
- 交付物：`data-readiness-checklist.md`
- 必须包含：数据源、owner、权限、更新频率、质量缺口、禁止进入检索的数据、反馈回写机制
- 通过条件：能回答“我们到底有没有数据做这个 AI 功能”，而不是默认技术能补齐一切。

## Lab 8：Graph / Agentic Retrieval Decision

- 目标：判断一个场景是否需要 Graph RAG 或 agentic retrieval。
- 交付物：`retrieval-mode-decision.md`
- 必须包含：实体密度、关系密度、查询复杂度、检索轮次、停止条件、成本与延迟风险
- 通过条件：不会把所有复杂检索都升级为图谱或 agent，而能说清使用条件。

## 历史验证结论

- 城市政策问答里，“外地人能申请公租房吗” vs “非本市户籍人员申请条件”这类偏差暴露的是语义覆盖与表达转换问题，不是简单关键词缺失。
- 政策法规更适合按条款、章节或语义边界切，而不是机械按固定字数横切；同时要保留版本、发布日期和章节归属等元数据。
- 检索错误与生成错误的诊断顺序应先看文档是否对口，再看回答是否准确反映文档。
- 内容过时、表述不一致、分块断裂都可能让系统看起来可用，但结果并不可信。
