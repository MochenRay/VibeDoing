# WorkflowLearn / Claude Entrypoint

> 最近确认时间：2026-04-16

## 目的

本文件是 Claude 在本地 `WorkflowLearn` 仓库中的入口投影副本。
当前仓库本身就是正式系统来源，不依赖外部 `AI-Shared` 才能运行。

## 最小读取顺序

1. `CLAUDE.md`
2. `_系统/全局规范.md`
3. `_系统/WorkflowLearnSystem/adapters/claude.md`

## WorkflowLearnSystem 必读

1. `_系统/WorkflowLearnSystem/project.md`
2. `_系统/WorkflowLearnSystem/Core-Learning.md`
3. `_系统/WorkflowLearnSystem/Teaching-Contract.md`
4. `_系统/WorkflowLearnSystem/runtime-contract.md`
5. `_系统/WorkflowLearnSystem/workflow-spec.md`
6. `_系统/WorkflowLearnSystem/file-schema.md`
7. `_系统/WorkflowLearnSystem/adapters/claude.md`
8. 教学型模块按需再读 `_系统/WorkflowLearnSystem/teaching/*.md`

## 项目延续

如果是在继续具体学习项目，再按需读取：

- 项目级 `project.md`
- 项目级 `handover.md`
- 项目级 `state.md`
- 必要的 `curriculum/*.md` 与 `refresh/*.md`

## 本地边界

- `WorkflowLearn` 仓库本身就是长期 Markdown 规则与项目文档的正式来源。
- 仓库内同时包含正式系统文档、实施现场和待迁移材料。
- Claude 的本地 jsonl、计划文件、hooks 和运行态不是共享状态。

## 禁止

- 不要把 `Claude-Learning.md` 当正式规则来源。
- 不要继续使用 slash command、`write_to_file`、自动 `_snapshot.md` 作为系统前提。
- 不要把 `项目信息.md`、`学习路径.md`、`学习报告.md`、`_snapshot.md` 当成新的单一真相源。
- 不要把 `AI-Shared` 当成运行时必需依赖。
