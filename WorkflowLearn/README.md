# WorkflowLearn

> 最近确认时间：2026-04-16
> 状态：首个可用版本

## 这是什么

`WorkflowLearn` 是一个 Markdown-first 的长期学习系统。

它的目标不是做一套只服务某个宿主的提示词，而是把学习这件事拆成一套可以跨 `Codex / Claude / Gemini` 运行的通用协议：

- 怎么恢复状态
- 怎么进入讲解
- 怎么验证是否真的学会
- 怎么把结果写回长期文档
- 怎么处理会过时的内容
- 怎么把学习产出沉淀成可复用的案例、方案和作品

当前这套仓库已经是自包含的正式来源。也就是说，直接在这个文件夹上打开终端并启动任一宿主，就应该能运行；不需要依赖外部 `AI-Shared`。

## 现在什么时候算“可用”

按 `2026-04-16` 当前状态，系统已经达到 **首个可用状态**。

这里的“可用”不是指“所有内容都写完了”，而是指下面这几件事已经同时成立：

1. 系统内核已经在仓库内收拢成单一真相层。
2. Codex / Claude / Gemini 都有本地入口。
3. 学习闭环、教学协议、状态 schema、刷新机制已经成文。
4. `项目/` 下的正式课程已经迁到新 schema。
5. `专题/` 层已经能承接某个阶段的路线图、产出清单和 capstone 案例包。

如果用更严格的话说，当前状态是：

- **可用**：是
- **稳定**：部分稳定
- **成熟**：还不是

## 这三个状态分别是什么意思

### 1. 可用

满足以下条件就算可用：

- 新会话能从仓库内入口启动
- 能恢复某个学习项目的当前状态
- 能按统一闭环继续学习、验证、写回
- 能区分稳定概念和时效内容
- 能留下长期文档，而不是只留在聊天记录里

现在已经满足。

### 2. 稳定

满足以下条件才算稳定：

- 主要课程都经过至少一轮外部核验
- 主要课程都已经补齐 `labs.md` 和 `outcomes.md`
- 典型专题至少有 `2-3` 个正式案例包
- 多宿主使用时不再出现“同一规则不同宿主跑出不同理解”的明显分叉

现在已经基本接近这个状态，但还没有进入长期稳定阶段。当前主要缺口是：

- 各课程的时效层还需要继续按真实选题刷新
- `Capstone A / B / C` 还需要从“首版可用”提升到“稳定可展示”
- 还没有经过一轮长期连续使用来证明回退、复习、断点续学都足够顺手

### 3. 成熟

满足以下条件才算成熟：

- 多个专题都能用同一套系统跑
- 系统文档几乎不再频繁改 schema
- 常见产物已经形成稳定模板库
- 新用户只看 `README.md` 就能上手
- 开源出去后，别人不用你亲自解释也能跑起来

现在距离成熟还有一段距离。

## 当前最准确的结论

**这套系统现在已经可以用于真实学习，但仍处在“第一个可用版本”，还不是最终稳定版。**

如果你今天就开始用它学，是合理的。
如果你今天就把它当“完全冻结、未来几乎不改”的系统，还太早。

## 仓库结构

```text
WorkflowLearn/
  AGENTS.md
  CLAUDE.md
  GEMINI.md
  README.md
  _系统/
  项目/
  专题/
```

### 根目录

- `AGENTS.md`：Codex 入口
- `CLAUDE.md`：Claude 入口
- `GEMINI.md`：Gemini 入口
- `README.md`：项目介绍与使用指南

### `_系统/`

只放通用系统层内容，不放当前阶段的专题学习计划。

关键文件：

- [_系统/全局规范.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/全局规范.md)
- [_系统/WorkflowLearnSystem/project.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/project.md)
- [_系统/WorkflowLearnSystem/Core-Learning.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/Core-Learning.md)
- [_系统/WorkflowLearnSystem/Teaching-Contract.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/Teaching-Contract.md)
- [_系统/WorkflowLearnSystem/runtime-contract.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/runtime-contract.md)
- [_系统/WorkflowLearnSystem/workflow-spec.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/workflow-spec.md)
- [_系统/WorkflowLearnSystem/file-schema.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/file-schema.md)
- [_系统/WorkflowLearnSystem/capstone-standard.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/capstone-standard.md)

### `项目/`

放正式学习项目。每个项目都应该有自己的：

- `project.md`
- `handover.md`
- `state.md`
- `curriculum/*.md`
- `refresh/*.md`

### `专题/`

放当前阶段的焦点路线图、产出清单和案例包。

例如当前专题：

- [专题/AI_PM转型/README.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/README.md)

## 如何启动

### Codex

最小入口：

1. [AGENTS.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/AGENTS.md)
2. [_系统/全局规范.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/全局规范.md)
3. `_系统/WorkflowLearnSystem/adapters/codex.md`

### Claude

最小入口：

1. [CLAUDE.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/CLAUDE.md)
2. [_系统/全局规范.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/全局规范.md)
3. `_系统/WorkflowLearnSystem/adapters/claude.md`

### Gemini

最小入口：

1. [GEMINI.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/GEMINI.md)
2. [_系统/全局规范.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/全局规范.md)
3. `_系统/WorkflowLearnSystem/adapters/gemini.md`

## 标准使用方式

### 场景 1：继续一个已有学习项目

读法：

1. 根入口
2. `_系统/全局规范.md`
3. 对应宿主 adapter
4. 项目级 `project.md`
5. 项目级 `handover.md`
6. 项目级 `state.md`
7. 必要的 `curriculum/*.md` 和 `refresh/*.md`

例如继续 `No.2_RAG与知识库`：

- [project.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/项目/No.2_RAG与知识库/project.md)
- [handover.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/项目/No.2_RAG与知识库/handover.md)
- [state.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/项目/No.2_RAG与知识库/state.md)

### 场景 2：查看当前阶段的学习路线

读法：

1. [专题/README.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/README.md)
2. 对应专题 `README.md`
3. 路线图、全景产出清单、capstone 组合

例如当前 AI PM 专题：

- [学习路线图.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/学习路线图.md)
- [全景预期产出清单.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/全景预期产出清单.md)
- [第一批Capstone组合.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/第一批Capstone组合.md)

### 场景 3：直接做专题案例

如果不是继续单门课，而是直接做一个综合案例，就进入专题案例包。

当前正式案例包包括：

- [Capstone A](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/README.md)
- [Capstone B](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/README.md)
- [Capstone C](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_C_AI_Native_Copilot_Feature/README.md)

## 标准学习闭环

系统当前固定闭环是：

`恢复 -> 差异扫描 -> 学习 -> 验证 -> 写回 -> 刷新 -> 更新下一步状态`

如果是教学型模块，则内部还必须遵守：

`讲解 -> 理解确认 -> 掌握验证 -> 费曼/实操 -> 结算 -> 复习计划`

这意味着：

- 没恢复状态，不能假装继续
- 没验证通过，不能写成正式结论
- 时效项不确定，不能塞进稳定层

## 每次使用时，你应该预期什么产出

这是最重要的部分。`WorkflowLearn` 不是“聊完就结束”，而是每一步都应该有明确产出。

### A. 系统层产出

当你在维护系统本身时，应该产出：

- 规则文档
- schema 文档
- adapter 文档
- 教学协议
- 使用指南

对应目录：

- `_系统/`

### B. 项目层产出

当你在推进某一门正式课程时，至少会涉及这些文件：

#### 1. `project.md`

预期产出：

- 这个项目到底学什么
- 目标是什么
- 不学什么
- 当前进度处在哪个阶段

#### 2. `handover.md`

预期产出：

- 当前判断
- 已冻结决策
- 未决问题
- 下一步

#### 3. `state.md`

预期产出：

- 当前模块
- 最近一次验证时间
- 下一个动作
- 当前卡点

#### 4. `curriculum/concepts.md`

预期产出：

- 稳定概念
- 长期有效的方法
- 跨模型、跨厂商仍成立的判断

#### 5. `curriculum/volatile.md`

预期产出：

- 容易过时的厂商快照
- 默认值
- 参数经验
- 需要重刷的判断

#### 6. `curriculum/sources.md`

预期产出：

- 当前依据是什么
- 最近一次官方或外部核验得出了什么结论
- 还缺什么核验

#### 7. `curriculum/labs.md`

预期产出：

- 可恢复的练习任务
- 代表性验证
- 错误归因
- 可直接复用的案例作业

#### 8. `curriculum/outcomes.md`

预期产出：

- 这门课能证明什么能力
- 会产出哪些文档、方案、案例
- 这些产物以后能放到哪里用

#### 9. `refresh/refresh-queue.md`

预期产出：

- 哪些内容以后要重刷
- 为什么要重刷
- 什么时候触发重刷

### C. 专题层产出

当你围绕一个阶段目标做专题化学习时，应该预期这些产出：

#### 1. 路线图

例如：

- [学习路线图.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/学习路线图.md)

预期产出：

- 学习顺序
- 项目映射
- 当前缺口
- 下一步主线

#### 2. 全景产出清单

例如：

- [全景预期产出清单.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/全景预期产出清单.md)

预期产出：

- 最终要拿到哪些作品
- 每类作品要证明什么能力
- 覆盖哪些方向

#### 3. Capstone 组合

例如：

- [第一批Capstone组合.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/第一批Capstone组合.md)

预期产出：

- 先做哪几套综合案例
- 每套案例由哪些课程拼成
- 最小交付包是什么

#### 4. Capstone 案例包

例如：

- [Capstone A](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_A_Grounded_Knowledge_Assistant/README.md)
- [Capstone B](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_B_Workflow_Agent_Operations_Assistant/README.md)
- [Capstone C](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/专题/AI_PM转型/Capstone_C_AI_Native_Copilot_Feature/README.md)

预期产出：

- 一套完整案例
- 不是散的笔记，而是完整的可展示材料

如果要新建 `Capstone B / C / D / E`，默认应遵循：

- [_系统/WorkflowLearnSystem/capstone-standard.md](/Users/rayli/Documents/VibeDoingEverything/VibeDoing/WorkflowLearn/_系统/WorkflowLearnSystem/capstone-standard.md)

## 当前已经有哪些正式产出

按 `2026-04-16` 当前状态，已经正式存在的产出包括：

### 系统层

- 多宿主入口
- 统一核心规则
- 教学协议
- 文件 schema
- 使用边界

### 课程层

- `No.1-No.8` 已全部有新 schema 落点
- `No.1-No.8` 已全部有 `concepts / teaching-guide / volatile / sources / labs / outcomes`

### 专题层

- 当前 AI PM 专题路线图
- 全景产出清单
- 第一批 capstone 组合
- `Capstone A` 首版案例包
- `Capstone B` 首版案例包
- `Capstone C` 首版案例包

## 当前还不该期待什么

为了避免误判，这里也明确写清：

你**现在不应该期待**这套系统已经具备以下状态：

- 所有时效内容都自动更新
- 所有专题都已经有完整案例包
- 所有课程都已经做完深度外部核验
- 所有宿主的行为已经在长期使用中被完全证明一致
- 新用户不经任何解释就一定能无歧义跑通全部流程

这些是下一阶段要继续打磨的内容，不是当前已经完成的事实。

## 如果你今天开始用，推荐顺序

### 如果你是系统维护者

1. 读本 `README.md`
2. 读根入口
3. 读 `_系统/全局规范.md`
4. 读 `WorkflowLearnSystem/*`

### 如果你是学习使用者

1. 读本 `README.md`
2. 看 `专题/` 下当前路线
3. 选一个 `项目/`
4. 从 `project.md + handover.md + state.md` 恢复
5. 按 `curriculum/` 和 `refresh/` 继续

### 如果你想直接做作品

1. 读当前专题路线图
2. 读 capstone 组合
3. 直接进入现成案例包

## 下一步最合理的工作

如果继续推进，现在最有价值的不是再改系统概念，而是：

1. 继续把 `Capstone A / B / C` 从“首版可用”提升到“稳定可展示”
2. 用真实连续学习过程验证回退、复习和断点续学体验
3. 决定下一批 `Capstone D / E` 是否需要开新方向

## 一句话总结

`WorkflowLearn` 现在已经是一套 **能真实使用的、多宿主、自包含、Markdown-first 学习系统**。

它当前最准确的定位是：

**已经可用，但还在从“首个可用版本”走向“稳定版”的过程中。**
