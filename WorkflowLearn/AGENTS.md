# Codex 本地入口

本文件是 Codex 在本地 `WorkflowLearn` 仓库中的薄适配层。
当前仓库本身就是正式系统来源，不依赖外部 `AI-Shared` 才能运行。

## 最小冷启动只读

1. `AGENTS.md`
2. `_系统/全局规范.md`
3. `_系统/WorkflowLearnSystem/adapters/codex.md`

## 仅在以下情况追加读取

- 需要进入 `WorkflowLearnSystem` 正式规则：
  `_系统/WorkflowLearnSystem/project.md`
  `_系统/WorkflowLearnSystem/Core-Learning.md`
  `_系统/WorkflowLearnSystem/Teaching-Contract.md`
  `_系统/WorkflowLearnSystem/runtime-contract.md`
  `_系统/WorkflowLearnSystem/workflow-spec.md`
  `_系统/WorkflowLearnSystem/file-schema.md`
  必要时再读 `_系统/WorkflowLearnSystem/teaching/*.md`
- 需要项目延续：
  相关 `项目/<name>/project.md`、`handover.md`、`state.md`

## 说明

- `~/.codex` 继续保存 Codex 自身原始会话、缓存和运行态
- 不把 `~/.codex/history.jsonl`、`sessions/`、`archived_sessions/`、sqlite 文件当作正式学习文档
- `WorkflowLearn` 仓库本身就是长期 Markdown 文档的正式来源
- `AI-Shared` 若继续使用，也只应视为可选镜像，不是运行时前提

## 同步规则

- 外部镜像同步应视为可选后处理，不是运行时依赖
- 运行态和临时产物不要混进正式学习文档
