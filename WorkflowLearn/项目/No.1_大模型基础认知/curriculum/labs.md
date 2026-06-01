# labs

> 最近确认时间：2026-04-16
> 状态：作品模板已扩写

## Lab 1：LLM Boundary Memo

- 目标：写一份能给非技术同事读懂的 `LLM 边界说明稿`。
- 交付物：`llm-boundary-memo.md`
- 必须包含：token、context、sampling、hallucination、为什么纯模型会错
- 通过条件：不靠术语堆砌，也能解释清楚“LLM 能做什么、不能做什么”

## Lab 2：Context Budget Review

- 目标：为一个真实文档任务做上下文预算评审。
- 交付物：`context-budget-review.md`
- 必须包含：输入预算、输出预算、是否需要摘要、是否需要 RAG、失败风险
- 通过条件：能回答“塞得下”和“该不该这么塞”是两回事

## Lab 3：Sampling Strategy Note

- 目标：为三个不同任务写一份采样策略判断。
- 交付物：`sampling-strategy-note.md`
- 必须包含：低温/中温/高温适用场景、风险、副作用、替代手段
- 通过条件：能区分“随机性问题”和“知识边界问题”

## Lab 4：Hallucination Risk Review

- 目标：为一个高风险 AI 功能写幻觉风险评审。
- 交付物：`hallucination-risk-review.md`
- 必须包含：会错在哪、为什么会错、如何限制、如何引用、何时转人工
- 通过条件：能把“幻觉”翻译成产品与流程设计，而不是只停留在概念层

## Lab 5：Explain It to a Non-expert

- 目标：向外行解释 LLM、RAG、工具调用三者区别。
- 交付物：`non-expert-script.md`
- 必须包含：LLM 本体、RAG、tool use 的区别，以及各自的失败方式
- 通过条件：不会把 LLM 误讲成“去数据库查答案”

## 历史验证结论

- `15000` 字政策文档并不 automatically 适合直接塞进长上下文模型；产品上仍要考虑 RAG 或抽取式上下文。
- 数据提取、合同审查、代码等强调正确性的任务优先低温；文案和脑暴可适度提高，但调温度不是知识问题的主解。
- “限定数据范围”是软约束，不是硬开关；高风险场景里仍要设计引用、原文溯源和人工审核。
- 好用的外行解释框架是“高概率续写 / 词语接龙”，不要用“搜索”“检索”比喻 LLM 本体。
- 回答“死板”的正确排查顺序是 prompt → few-shot → schema → 模型 → 温度；温度永远是**最末端**的旋钮，不是第一反应。
- 高风险场景（法律/医疗/金融）铁律：错报代价 >> 漏报代价。"我不知道" 应作为**可见、可操作**的产品状态暴露给用户，而不是被系统静默吞掉。
- Temperature 和 top_p 功能重叠，业界共识**只调一个**；要复现性加 `seed`；reasoning 模型（o1 / Extended Thinking 类）对 temperature 反应很弱甚至不暴露——这条属于 volatile 区域，需按厂商当期文档核实。
