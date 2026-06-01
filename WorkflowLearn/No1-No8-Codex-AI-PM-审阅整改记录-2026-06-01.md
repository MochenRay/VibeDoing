# No.1-No.8 Codex AI PM 审阅整改记录

> 记录日期：2026-06-01
> 对应审阅报告：`No1-No8-Codex-AI-PM-审阅报告-2026-06-01.md`
> 整改原则：按“用户尚未学习、从头开始”重设课程；审阅项先进入首轮入口，时效细节仍留 refresh。

## 已改内容

| 审阅项 | 处理结果 | 修改位置 |
|---|---|---|
| C1 No.7 handover 过时 | 已更新 No.7 交接页，移除“补 concepts/labs/outcomes”的旧下一步，改为 vendor lock-in、统一 routing、首轮教学验证 | `项目/No.7_技术选型判断/handover.md` |
| C2 时间戳漂移 | 已在系统 schema 写明 `state.md` 与 `refresh-queue.md` 的时间戳语义；已更新 No.1、No.2、No.3、No.4、No.5、No.6、No.7、No.8 的状态判断 | `_系统/WorkflowLearnSystem/file-schema.md`；各项目 `state.md` |
| C3 Reasoning Models 缺失 | 已在 No.1 新增 A4；补 concepts、teaching-guide、labs、sources、refresh、state；并在 No.4 增加 reasoning model 下的 prompt 设计边界 | `项目/No.1_大模型基础认知/*`；`项目/No.3_Prompt_Engineering/*` |
| C4 No.3 / No.4 顺序 | 已执行目录级置换：`No.3_Prompt_Engineering` 在前，`No.4_AI产品评估指标` 在后；同步路线图、Capstone 映射和项目引用 | `项目/No.3_Prompt_Engineering/`；`项目/No.4_AI产品评估指标/`；专题映射文档 |
| I1 伦理/偏见/负责任 AI | 已改为稳定教学模块 F9：Responsible AI / Bias / Compliance；同时记录 NIST、EU AI Act、中国生成式 AI 监管作为框架来源 | `项目/No.5_AI产品设计特殊性/curriculum/concepts.md`；`sources.md`；`refresh/refresh-queue.md` |
| I2 安全评估深度不足 | 已新增 B4：Safety / Policy / Red-team Evals，把安全评估并入 launch gate | `项目/No.4_AI产品评估指标/curriculum/concepts.md`；`sources.md` |
| I3 Agent 安全/提示注入不足 | 已新增 P9：Agent Security，覆盖用户输入、检索文档、工具返回、多轮上下文、权限、净化、审计与人工确认 | `项目/No.6_Agent概念/curriculum/concepts.md`；`sources.md`；`refresh/refresh-queue.md` |
| I4 Agent 成本估算缺失 | 已新增 P10：Agent Cost Model，覆盖 reasoning、工具调用、重试、状态、日志、HITL 与失败回滚成本 | `项目/No.6_Agent概念/curriculum/concepts.md` |
| I5 统一决策框架不足 | 已强化 No.7 P2：按失败模式分流 prompt / RAG / workflow / agent / fine-tune，并把“拉错杠杆”纳入 Lab 1 | `项目/No.7_技术选型判断/curriculum/concepts.md`；`labs.md` |
| I6 数据策略 / 数据就绪评估 | 已新增 No.2 P4 与 Lab 7，覆盖数据源、owner、权限、质量、更新、禁止进入检索的数据和反馈回写 | `项目/No.2_RAG与知识库/curriculum/concepts.md`；`labs.md` |
| I7 AI 产品用户研究方法 | 已新增 No.3 P13 / Lab 8 与 No.5 F10 / Lab 8，覆盖 Wizard of Oz、信任校准、心智模型和失败接管观察 | `项目/No.3_Prompt_Engineering/curriculum/*`；`项目/No.5_AI产品设计特殊性/curriculum/*` |
| I8 监管合规不足 | 已纳入 No.5 F9；具体法规适用结论放入刷新队列，不写成静态法律意见 | `项目/No.5_AI产品设计特殊性/curriculum/concepts.md`；`refresh/refresh-queue.md` |
| I9 供应商锁定分析缺失 | 已在 No.7 P3/P4 增加 vendor lock-in 与切换成本；Lab 2 纳入 lock-in；refresh queue 纳入迁移成本刷新 | `项目/No.7_技术选型判断/curriculum/concepts.md`；`labs.md`；`refresh/refresh-queue.md` |
| I10 No.5 / No.8 反馈循环重叠 | 已明确 No.5 F6 是战术反馈与接管，No.8 P3 是战略反馈、eval dataset 与路线图 | `项目/No.5_AI产品设计特殊性/curriculum/concepts.md`；`项目/No.8_AI_Native进阶/curriculum/concepts.md` |
| N1 Graph RAG / 知识图谱 | 已进入 No.2 B4，定位为实体/关系/路径推理场景的可选检索模式 | `项目/No.2_RAG与知识库/curriculum/concepts.md` |
| N2 Agentic retrieval | 已进入 No.2 B5 与 No.6 P11，强调 query budget、停止条件、trace 与安全边界 | `项目/No.2_RAG与知识库/curriculum/concepts.md`；`项目/No.6_Agent概念/curriculum/concepts.md` |
| N3 Prompt caching | 已进入 No.3 P12 与 refresh queue，作为延迟/成本/prompt 架构问题处理 | `项目/No.3_Prompt_Engineering/curriculum/concepts.md`；`refresh/refresh-queue.md` |
| N4 MCP 引用 | 已补入 No.3 P6，说明 MCP 与 tool contract 的关系 | `项目/No.3_Prompt_Engineering/curriculum/concepts.md` |
| N5 AI 原生定价/变现 | 已补入 No.7 P5 / Lab 6，覆盖 seat、usage、outcome、free-tier 和边际成本 | `项目/No.7_技术选型判断/curriculum/*` |
| N6 用户引导 | 已补入 No.8 P8 / Lab 6，覆盖能力展示、边界提示、核实和撤销路径 | `项目/No.8_AI_Native进阶/curriculum/*` |
| N7 国际化/文化适配 | 已补入 No.8 P9 / Lab 7 | `项目/No.8_AI_Native进阶/curriculum/*` |
| N8 无障碍访问 | 已补入 No.8 P10 / Lab 7 | `项目/No.8_AI_Native进阶/curriculum/*` |
| N9 AI 事故危机管理 | 已补入 No.5 F11 / Lab 9 | `项目/No.5_AI产品设计特殊性/curriculum/*` |
| N10 上线后监控 | 已补入 No.4 B5，桥接 No.3、No.5、No.6、No.8 | `项目/No.4_AI产品评估指标/curriculum/concepts.md` |
| N11 跨职能团队协作 | 已补入 No.7 P8 / Lab 7 | `项目/No.7_技术选型判断/curriculum/*` |
| N12 流式/置信度 UX | 已补入 No.3 P8 / Lab 9 | `项目/No.3_Prompt_Engineering/curriculum/*` |

## 未改内容

| 审阅项 | 本次未改原因 | 后续触发条件 |
|---|---|---|
| Capstone A/B/C 交付物全文重写 | 本次只修课程映射和能力来源，不重写具体 portfolio 文件；否则会在未重新做案例验证前制造新“看似完成”的材料 | 当用户开始正式打磨某个 capstone 时，按真实案例逐文件重写 |
| 具体法规条款、供应商价格、模型默认值 | 这些是时效内容，不进入 stable；已放入 refresh queue | 做真实地区、行业、供应商或预算方案时再按官方来源刷新 |

## 外部依据处理

- `Reasoning Models` 依据 OpenAI Reasoning models、Anthropic Extended Thinking、Gemini Thinking 官方文档进入稳定概念层。
- `Responsible AI / Compliance` 只吸收 NIST AI RMF、EU AI Act、中国生成式 AI 服务监管的框架级判断；具体义务留在刷新队列。
- `Agent Security` 只吸收 OWASP LLM 风险框架中的稳定攻击面语言；具体风险排序和平台护栏留在刷新队列。
- Graph RAG、agentic retrieval、prompt caching、i18n、accessibility、pricing 等只进入稳定判断框架；具体平台能力、价格和实现清单进入 refresh。

## 当前状态

- `No.1` 不再视为全量完成；A1/A2/A3/B2 已通过，A4 Reasoning Models 待首轮教学验证。
- `No.2` 仍停在 B3 第 1 轮讲解；B3 刷新完成不等于教学通过。
- 目录级顺序已调整为 `No.1 -> No.2 -> No.3 Prompt -> No.4 Evals -> No.5 -> No.6 -> No.7 -> No.8`。
- `No.3-No.8` 已完成首轮课程刷新，但仍标记为 pending teaching，不能当成已掌握。
