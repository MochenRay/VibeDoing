# concepts

> 最近确认时间：2026-06-01
> 状态：B3 已刷新为 launch gate / continuous eval / agent eval 模板

## 模块 P1：为什么 AI PM 需要 evals

- 对 AI 产品来说，`eval` 不是“上线后再看看”，而是需求、验收和放量的共同合同。
- 没有 eval，团队通常只是在比较 demo 观感，而不是比较系统质量。
- AI PM 真正需要的是把“感觉好不好”翻译成：目标是什么、样本是什么、指标 / rubric 是什么、对比对象是什么、上线后如何持续发现回归和漂移。

## 模块 A1：混淆矩阵与基础分类指标

- `TP / TN / FP / FN` 仍然是理解误报、漏报和 tradeoff 的基本语言。
- `Precision` 适合表达“报出来的结果有多可信”，`Recall` 适合表达“真正重要的案例漏了多少”。
- `F1` 适合在精确率和召回率都重要时做平衡，但它仍然不能替代业务代价判断。
- 这类指标对分类、审核、预警、路由、风险识别等 AI 产品场景仍然成立。

## 模块 A2：评估设计四步

- 一条稳定工作流是：`objective -> dataset -> metrics / rubric -> compare -> continuous eval`。
- `objective` 先定义成功标准，再谈数据和指标，否则评估会变成无目标打分。
- `dataset` 不应只来自理想样本，还应包含生产数据、边缘案例、对抗样本和人工整理样本。
- `metrics / rubric` 不应只依赖单一数字；自动指标、模型裁判、人工评价和业务指标通常需要组合使用。
- `compare` 至少要说明 baseline、候选方案、回归样本和人工复核口径，否则无法判断新方案是否真的更好。
- `continuous eval` 要把线上日志、失败样本、用户反馈和策略变更回灌到数据集，持续检查回归、漂移和安全边界。

## 模块 B1：Workflow / Retrieval Evals

- 当系统从单次模型调用变成多步 workflow 时，评估应优先拆到每个关键步骤，而不是只看最终回答。
- 对 RAG / retrieval 系统，关键不是只看“答得像不像”，还要看检索是否找对、引用是否对应、上下文是否充分。
- 一个实用判断是：先评估检索环节，再评估最终生成环节，避免把不同类型的错误混在一起。
- 当系统引入 query rewriting、filtering、ranking 或 hybrid search 时，评估点也应跟着扩展。

## 模块 B2：Agent Evals

- agent 的新问题不只是“回答是否正确”，还包括“是否选对工具、是否传对参数、是否在正确时机交接或追问”。
- 单 agent 与多 agent 系统都存在新的 nondeterminism，因此必须按架构边界设计 eval。
- 对长流程 agent，除任务完成率之外，还要看增量进展、状态交接和失败后是否留下可恢复 artifact。
- 高风险 agent 不能只靠自动分数，必须设计人工复核、回滚和停止条件。
- agent eval 的稳定维度包括：tool selection、argument correctness、handoff、regression、drift、human review。

## 模块 B3：Launch Gate / Continuous Eval Template

- B3 的产物不是一堂指标课，而是一份可复用的上线门槛与持续评估模板。
- AI 功能上线前至少要回答：离线效果够不够、rubric 是否可解释、baseline 是否被击败、护栏指标稳不稳、失败时怎么接管、上线后怎么持续评估。
- launch gate 应固定包含：objective、dataset、metrics / rubric、baseline comparison、go / no-go threshold、human review、rollback、continuous eval backlog。
- agent / workflow gate 还要检查：工具选择是否正确、参数是否可执行、handoff 是否清晰、状态是否可恢复、回归样本是否通过、漂移信号由谁复核。
- 护栏指标通常包括延迟、成本、失败率、用户满意度、升级人工比例、严重错误率和策略违规率。
- `A/B test` 在 AI 产品里仍然重要，但它只适合回答“新方案是否优于旧方案”，不替代离线质量验证、人工复核和安全 / policy eval。
- 更成熟的上线方式是：离线 eval 先过线，小流量验证护栏，再把线上失败样本回灌到持续 eval，最后决定是否放量。

## 当前不进入稳定层的内容

- 具体模型裁判选择
- 固定分数阈值与 benchmark 快照
- 厂商 eval 产品能力表
- 价格表与响应时间静态表
