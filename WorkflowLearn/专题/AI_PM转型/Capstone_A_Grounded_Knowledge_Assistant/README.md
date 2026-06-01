# Capstone A

> 最近确认时间：2026-04-16
> 状态：首版案例包已扩成作品集版原型

## 主题

`Grounded Knowledge Assistant`

当前默认样例是：`城市治理知识助手`。
它也可以平移成企业知识助手、政策问答助手或内部知识搜索产品。

## 目标

用一套完整案例证明三件事：

- 你能判断为什么这个场景该上 `RAG / Grounding`
- 你能把引用、fallback、人工接管和上线门槛一起设计进去
- 你能把它讲成一个可上线的产品，而不是只会画检索架构图

## 交付文件

### Core Delivery Layer

- [rag-fit-memo.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/rag-fit-memo.md)
- [product-spec.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/product-spec.md)
- [knowledge-architecture-map.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/knowledge-architecture-map.md)
- [eval-plan.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/eval-plan.md)
- [grounding-citation-design.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/grounding-citation-design.md)
- [fallback-citation-design.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/fallback-citation-design.md)

### Portfolio Layer

- [case-study.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/case-study.md)
- [presentation-script.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/presentation-script.md)
- [interview-qna.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/interview-qna.md)

## 课程映射

- `No.1`：LLM 边界、hallucination 风险、context 预算
- `No.2`：RAG / retrieval / grounding / citations
- `No.3`：eval、launch gate、在线护栏
- `No.5`：fallback、HITL、trust

## 使用顺序

1. 先读 `rag-fit-memo.md`
2. 再读 `product-spec.md` 和 `knowledge-architecture-map.md`
3. 然后读 `eval-plan.md`
4. 再读 `grounding-citation-design.md` 和 `fallback-citation-design.md`
5. 最后用 `case-study.md`、`presentation-script.md`、`interview-qna.md` 做展示与面试准备

## 标准地位

本目录现在也是当前 `WorkflowLearn` 的首个 `capstone-standard` 原型实现。
后续 `Capstone B / C / D / E` 默认都应复用同一结构，而不是重新发明案例包形态。
