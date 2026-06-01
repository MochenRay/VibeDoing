# Codex 重构与课程升级方案

> 状态：历史本地工作稿
> 最近确认时间：2026-04-16
> 说明：本文件保留为本地演进记录，现行正式系统定义以 `_系统/WorkflowLearnSystem/` 为准。

更新时间：2026-04-16

## 1. 这套系统到底要做什么

这不是一个“学习笔记仓库”，而是一套面向 AI 产品经理转型的学习操作系统。

它应该稳定支持 5 件事：

1. 把一个大主题切成可学习、可验证、可恢复的学习项目。
2. 让学习不止停在“知道”，而是走到“能判断、能解释、能设计、能拆方案”。
3. 把知识分成稳定概念和强时效事实，避免“底层原理”和“当月价格表”混在一起。
4. 让课程内容持续保持可验证、可追溯、可刷新，而不是写成一次性的“最新实践”。
5. 最终产出对找工作有用的能力证据：判断框架、案例拆解、方案设计、评测思路、Agent/Harness 视角。

## 2. 重写判断

结论不是“整套推倒重来”，而是：

- **控制层重写**：要重写。
- **内容层部分保留**：可以保留大量稳定知识骨架。
- **状态层直接清空重建**：应该这样做。

原因很简单：

- 旧系统的运行假设明显带有 Claude/Gemini 时代遗留物，不适合直接继续挂在 Codex 上。
- 但大量底层概念本身没有坏，坏的是运行方式、状态管理和时效层。
- 你已经明确表示历史进度不重要，那就不值得花精力修旧状态一致性。

所以最合理的路线是：

**重写系统内核，保留高价值知识，重建课程结构和刷新机制。**

## 3. 为什么控制层必须重写

当前控制层存在 6 类系统性问题：

1. 依赖不存在的执行抽象：
   - 例如 `write_to_file`
   - 例如对 `Read` 工具调用记录的验证

2. 假定存在命令路由器：
   - 例如 `/学习`、`/实操`、`/课程`
   - 在当前 Codex 环境里，这些只是文本，不是宿主能力

3. 假定状态会自动同步：
   - `_snapshot.md` 被写成“自动更新”
   - 实际上这里没有自动状态层

4. 路径规范和仓库实际结构不一致：
   - 例如白板路径规范仍引用 `vibe-learning`
   - 当前仓库根是 `WorkflowLearn`

5. 单一状态被分散到多个文件：
   - `项目信息.md`
   - `学习路径.md`
   - `_snapshot.md`
   - `学习报告.md`
   - `知识白板.canvas`

6. 文件 schema 本身已经漂移：
   - frontmatter 位置不一致
   - `last_review` / `last_reviewed` 混用
   - 有的卡片元数据在头部，有的在尾部

这些不是“修几行文案”能解决的问题。

## 4. 新系统的目标架构

建议把系统拆成 4 层。

### 4.1 Runtime 层

职责：定义 Codex 下真正可执行的学习流程。

建议保留：

- 学习初始化
- 讲解
- 验证
- 回退
- 收尾

建议删除：

- 伪工具名
- 宿主不支持的 slash command 假设
- “自动更新”式描述

建议文件：

- `_系统/Codex-Learning.md`
- `_系统/runtime-contract.md`
- `_系统/workflow-spec.md`
- `_系统/file-schema.md`

### 4.2 Curriculum 层

职责：存放真正的课程内容。

每个主题不再只是一篇 `初始文档.md`，而是拆成 5 类文件：

- `concepts.md`：稳定概念层
- `volatile.md`：模型名、价格、窗口、benchmark、版本差异
- `sources.md`：官方来源和校验日期
- `labs.md`：练习、场景题、产品判断题
- `career.md`：这一模块如何映射到 AI PM 能力和岗位价值

### 4.3 State 层

职责：保存“现在学到哪了”。

这层必须轻量，而且允许丢弃重建。

建议只保留一个主状态文件：

- `state/current-learning.md`

按需再保留一个项目态文件：

- `项目/<name>/state.md`

不再让 `学习路径`、`报告`、`白板` 同时承担状态源角色。

### 4.4 Refresh 层

职责：保持课程 up-to-date。

建议增加：

- `_系统/source-registry.md`
- `_系统/refresh-queue.md`
- `_系统/verification-policy.md`

每个时效性模块必须有：

- `last_verified`
- `verification_scope`
- `source_type`
- `volatility`

## 5. 课程内容怎么处理

### 5.1 可保留的稳定知识

这些内容大多保留骨架即可：

- `No.1` 的 Token / Context / Temperature / 幻觉 / LLM 原理
- `No.2` 的 RAG / Embedding / ANN / Chunking / 检索错误 vs 生成错误
- `No.3` 的评测和指标框架
- `No.4` 的 Prompt 基本结构和迭代方法
- `No.5` 的 AI 产品设计基础框架
- `No.6` 的 Agent 基础概念
- `RAG_Vector_DB` 的底层方法论部分
- `Antigravity_Mastery` 中与 Agent Loop、Artifacts、MCP 骨架相关的部分

### 5.2 必须整体重写的内容

- `No.7_技术选型判断`
- `No.8_AI_Native进阶`

这两块太依赖当时的模型能力、价格和生态快照，继续“修补更新”性价比不高。

### 5.3 应该直接清空重建的内容

以下内容都属于状态层，而不是知识层：

- `项目信息.md`
- `_snapshot.md`
- `学习报告.md`
- 旧版 `学习路径.md`

如果你接受“重新学习也没关系”，这些文件不值得做历史修复。

## 6. 新课程主线应该怎么升级

你的目标不是“泛懂 AI”，而是建立一个对找 AI PM 工作真正有竞争力的知识结构。

建议把课程主线重构成 6 个方向：

1. **LLM Foundations**
   - Token
   - Context
   - Sampling
   - Hallucination
   - Model capability boundaries

2. **Retrieval, Memory, and Knowledge Systems**
   - RAG
   - Embedding
   - ANN
   - Chunking
   - Reranking
   - Evaluation of retrieval systems

3. **Prompting, Structured Output, and Tool Use**
   - Prompt structure
   - Tool calling
   - Structured outputs
   - Model routing
   - Failure handling

4. **Agents and Harness Engineering**
   - Agent loop
   - Task decomposition
   - Artifact design
   - Long-running harnesses
   - MCP
   - Browser/computer use
   - Multi-agent coordination

5. **Evals, Guardrails, and Production Readiness**
   - Offline evals
   - Scenario evals
   - Hallucination checks
   - Safety and compliance
   - Cost / latency / reliability trade-offs
   - Regression testing for AI features

6. **AI PM Strategy and Job Conversion**
   - AI feature discovery
   - Product scoping under model uncertainty
   - AI-native UX
   - Enterprise workflow AI
   - Agent platform PM
   - Applied AI PM
   - AI infra / eval / operations PM

## 7. 当前外部信号说明课程必须升级

以下官方资料都说明生态已经继续往前走了：

- OpenAI 已明确把 Responses API 作为构建 agent 的未来方向，并给出 Assistants API 迁移路径：
  - <https://platform.openai.com/docs/guides/migrate-to-responses>
- OpenAI API 定价页已经以 GPT-5 系列为当前主线：
  - <https://openai.com/api/pricing>
- Anthropic 当前模型总览已经是 Claude 4.6 系列，而不是旧文档中的 4.5：
  - <https://docs.anthropic.com/en/docs/about-claude/models/overview>
- Anthropic 已公开把“long-running agents 的 harness”当成一类独立工程问题来讲：
  - <https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents>
- MCP 官方文档已经把它定义成连接模型与外部工具/上下文的标准协议：
  - <https://modelcontextprotocol.io/schema/v1>
- Google Gemini 当前文档主线已是 Gemini 2.5 / 3.x 系列，而不是旧内容中的固定快照：
  - <https://ai.google.dev/gemini-api/docs/models?hl=en>
  - <https://ai.google.dev/gemini-api/docs/pricing?hl=en>

这意味着新课程不能再把“模型对比表”和“价格表”写死在主概念文档里。

## 8. 是否需要“完全重写”

我的判断：

- **系统层**：需要重写。
- **课程层**：不需要完全重写。
- **时效层**：需要系统化刷新。
- **状态层**：直接重置。

换句话说，这不是“整仓重做”，而是：

**重写操作系统，迁移有价值课程，废弃脏状态，建立持续刷新机制。**

## 9. 推荐执行顺序

### Phase 0：冻结旧系统

- 保留旧文件做参考
- 停止继续维护旧状态文件
- 不再尝试修历史快照一致性

### Phase 1：重写 Codex Runtime

- 新建 Codex 入口文件
- 重写运行规范
- 重写文件 schema
- 去掉宿主不兼容假设

### Phase 2：重构课程目录

- 课程内容按“稳定概念 / 时效快照 / 实操 / 来源 / 职业映射”拆层
- 给每个模块补 `sources.md`
- 给每个模块标 `last_verified`

### Phase 3：刷新重点模块

优先级建议：

1. `No.7_技术选型判断`
2. `No.8_AI_Native进阶`
3. `No.6_Agent概念`
4. `No.3_AI产品评估指标`
5. `No.4_Prompt_Engineering`
6. `No.1` 的主流模型对比部分

### Phase 4：重建学习产品化输出

这一步是为了找工作：

- 每个主题都输出一份 PM 视角的判断框架
- 每个大模块都产出一份案例拆解或方案设计
- 最终组合成你的 AI PM 能力档案

## 10. 我的建议

建议现在就按下面的判断执行：

- **不修旧系统**
- **直接重写 Codex 控制层**
- **保留稳定概念内容**
- **强时效模块重写**
- **全部状态文件视为可丢弃**

如果你同意，下一步我建议直接进入实施，不再继续讨论“旧状态要不要修”。

第一刀应该落在：

1. 新建 Codex 入口与 runtime contract
2. 统一课程文件 schema
3. 清空旧状态层
4. 重写 `No.7` 和 `No.8` 的课程骨架

## 11. 求职导向课程取舍（No.1-No.6）

### 11.1 判断方法

这部分不是按“学术完整性”排，而是按“对 2026 年 AI 产品经理岗位有没有直接价值”排。

本轮判断主要依据两类外部证据：

1. **官方技术主线**
   - OpenAI 文档当前把 `tools`、`function calling`、`structured outputs`、`evals`、`Agents SDK`、`MCP and Connectors` 放在核心能力区。
   - Anthropic 当前仍把 `prompting`、`tool use`、`long-running agent harness` 作为一线实践主题。
   - MCP 官方把协议定位为连接模型与外部系统的标准层。

2. **当前岗位信号**
   - AI PM 岗位越来越多地要求理解：
     - LLM/ML product lifecycle
     - retrieval / context graph / knowledge access
     - prompt logic / workflows / policies
     - evals / validation / guardrails
     - deployment / governance / MLOps / model lifecycle

注意：

- 这不是“充分社区调研”的最终版结论。
- 这是“官方资料 + 当前招聘市场信号”驱动的高可信初版。
- 如果后续要做更细的岗位策略，还需要再补一轮 practitioner/community 调研。

### 11.2 必须学

这些模块对你找 AI PM 工作最直接，应该保留并优先升级。

#### 必须学 1：No.2 RAG 与知识库

理由：

- 企业 AI 产品里，知识获取、检索、上下文拼接、错误诊断仍然是核心问题。
- 当前岗位已经开始明确写 `agentic retrieval`、`context graph`、让 LLM 工具“找到并使用相关数据”。
- 这块直接对应企业搜索、Copilot、Agent、工作流自动化、知识助手等岗位。

保留重点：

- RAG 流程
- Embedding / ANN / Chunking
- 检索错误 vs 生成错误
- RAG 的适用边界

需要升级：

- 默认 chunk 经验值
- 产品案例
- 检索架构中的 reranking / graph / tool retrieval 扩展

#### 必须学 2：No.6 Agent 概念

理由：

- 当前官方技术主线已经不是“单轮问答”，而是 `tools + state + orchestration + evals + guardrails`。
- 当前岗位里，AI Agents、AI Workflows、Autonomous Agents、AI Platform 都非常常见。
- 这是离 “Harness Engineering” 最近的课程基底。

保留重点：

- Agent vs 普通对话
- ReAct / Agent loop
- Tool design
- MCP
- 何时用 Agent，何时不用

需要升级：

- 具体平台案例
- Computer Use 和多 Agent 的当前生态
- 从“概念介绍”升级到“agent runtime / harness design / state / artifacts / verification”

#### 必须学 3：No.3 AI 产品评估指标

理由：

- 当前岗位最明显缺口之一不是“会说 AI”，而是能把 AI 功能评估、验证、上线治理说清。
- OpenAI 官方把 evals 单列成系统能力。
- 岗位描述里已经频繁出现 validation、performance metrics、evaluation suites、AI quality、guardrails。

保留重点：

- Precision / Recall / F1 的产品判断逻辑
- A/B test
- 响应延迟 / 成本 / 体验权衡
- 评估框架

需要升级：

- 从“分类指标课”升级到“LLM/Agent evals 课”
- 增加 ground truth、representative sample、human eval、tool-use eval、workflow eval、regression eval

#### 必须学 4：No.4 Prompt Engineering

理由：

- Prompt 工程没有过时，但它已经不再等于“写几句话让模型更聪明”。
- 当前岗位已明确出现 prompt logic、guardrails、workflows、tool usage evaluations。
- 官方文档也仍把 few-shot、system instructions、structured outputs、function calling 视为核心能力。

保留重点：

- Prompt 基本结构
- System prompt
- Few-shot
- 复杂任务拆解
- Prompt 迭代

需要升级：

- 弱化“Prompt 小技巧”
- 强化 `Prompt + Schema + Tools + Evals + Policies`
- 把 Structured Outputs 和 Function Calling 升到主线，而不是附录

#### 必须学 5：No.1 大模型基础认知

理由：

- 这是所有技术判断的底层语法。
- 虽然招聘信息很少直接写 “懂 Token”，但不会这些，你在模型能力边界、成本、context、幻觉、输出稳定性上会持续犯低级错误。

保留重点：

- Token
- Context
- Temperature / sampling
- Hallucination
- “模型本质上是预测型系统，不是数据库”

需要升级：

- 大幅压缩主流模型对比和价格快照
- 保留概念，不保留时点对照表

### 11.3 可选学

这些内容有价值，但优先级低于上面 5 个模块，或者应该并入其它模块而不是独立占大篇幅。

#### 可选学 1：No.5 AI 产品设计特殊性

理由：

- 里面的人机边界、Fallback、预期管理、置信度展示，对 AI PM 很重要。
- 但这些更像“AI PM UX 方法论”，不是你当前与市场对齐时最稀缺的硬能力。
- 它适合作为 No.3 / No.4 / No.6 的产品化补充，而不是单独优先主线。

建议处理：

- 保留
- 压缩
- 合并进 “AI PM Strategy and Job Conversion” 主线

#### 可选学 2：No.1 中的主流模型对比

理由：

- 理解“能力边界差异”有用。
- 但招聘市场真正看重的不是背参数，而是会不会做 trade-off。

建议处理：

- 改成“模型能力维度与选型变量”
- 不再做静态榜单

### 11.4 应该删或并入

这里的“删”不是知识没价值，而是**不值得继续以当前形式存在**。

#### 应删/并入 1：No.1 的价格表和模型快照

- 直接删出主文档
- 放入 `volatile.md`

#### 应删/并入 2：No.3 的静态价格计算部分

- 保留“成本建模方法”
- 删除具体厂商报价快照

#### 应删/并入 3：No.4 中过度 vendor-specific 的旧 API 示例

- 例如某一版 Claude Tool Use 示例
- 应改成“协议/模式级写法”

#### 应删/并入 4：No.5 里和 No.3/No.6 重复的人机协同、Fallback、错误反馈内容

- 保留框架
- 并入 AI PM 主线，不再重复造轮子

### 11.5 最终排序

如果目标是 **“尽快建立对 AI PM 求职最有竞争力的知识结构”**，建议顺序是：

1. `No.1` 精简版
   - 只学底层机制
2. `No.2`
   - 直接补企业 AI 产品最常见能力
3. `No.4`
   - 从 Prompt 走到 Tools / Structured Outputs / Workflow
4. `No.6`
   - 从 Agent 概念走到 Harness 思维
5. `No.3`
   - 把“会做 AI”升级成“会评估 AI”
6. `No.5`
   - 补齐 UX、人机协同、Fallback、产品叙事

### 11.6 对应外部证据

官方资料：

- OpenAI `Using tools`：
  - <https://developers.openai.com/api/docs/guides/tools>
- OpenAI `Function calling`：
  - <https://developers.openai.com/api/docs/guides/function-calling>
- OpenAI `Structured outputs`：
  - <https://developers.openai.com/api/docs/guides/structured-outputs>
- OpenAI `Working with evals`：
  - <https://developers.openai.com/api/docs/guides/evals>
- OpenAI `Evaluation best practices`：
  - <https://developers.openai.com/api/docs/guides/evaluation-best-practices>
- Anthropic prompt best practices：
  - <https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices>
- Anthropic long-running harnesses：
  - <https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents>
- Gemini prompt design：
  - <https://ai.google.dev/gemini-api/docs/prompting-strategies?hl=en>
- MCP 官方介绍：
  - <https://modelcontextprotocol.io/>

岗位信号：

- Aledade AI Platform PM：
  - <https://jobs.lever.co/aledade/76677033-2329-4b4d-94c6-0486ea6b010c>
- Aledade Senior TPM, AI Data Platform：
  - <https://jobs.lever.co/aledade/946d319e-f8c4-4d11-835d-59db22227213>
- Shield AI Product Manager, AI Platforms：
  - <https://jobs.lever.co/shieldai/7886f437-2d5e-4616-8dcb-3dc488f1f585>
- Cinder Agent Product Manager：
  - <https://jobs.ashbyhq.com/cinder/2c483a08-7d94-4901-babb-5cbd880ce949>
- Hello Patient AI Agent Product Manager：
  - <https://jobs.ashbyhq.com/hellopatient/bfc01b2e-c1a8-40b9-9840-2c0e19ecf49d>
- Vanta Staff Product Manager, AI-Powered Workflows：
  - <https://jobs.ashbyhq.com/vanta/4d1a2838-9103-446c-9255-00a068479aab>

## 12. 直接结论

如果只看 No.1-No.6：

- **必须学**：`No.1`（精简后）、`No.2`、`No.3`、`No.4`、`No.6`
- **可选学**：`No.5`
- **应该删或并入的部分**：所有静态模型快照、价格表、旧 vendor 示例、重复的人机协同话术

真正该做的不是“删掉 No.1-No.6”，而是：

**把它们从“课程笔记”重构成“AI PM 求职能力地图”。**
