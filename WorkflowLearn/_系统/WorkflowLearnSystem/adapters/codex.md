# WorkflowLearnSystem / Codex Adapter

> 最近确认时间：2026-04-16

## 1. 目的

本文件只描述 Codex 对 `WorkflowLearnSystem` core/runtime 的映射方式，不重复 core 规则。

## 2. 读取入口

- 先读仓库根目录 `AGENTS.md`
- 再读 `_系统/全局规范.md`
- 需要延续项目上下文时，再读对应项目的 `project.md`、`handover.md`、`state.md`
- 不把 `~/.codex/history.jsonl`、`sessions/`、`archived_sessions/`、sqlite 或插件缓存当作正式来源

## 3. 写回前置检查

- 先确认写入目标在当前仓库内
- 先确认本次修改只属于 adapter，不在这里改 core/runtime
- 先确认单文件写后不超过 200 行；超长则先拆分
- 如果要同步外部镜像，把它视为额外动作，不视为运行时前提

## 4. 并行策略

- 中大型改动默认走 `git worktree + agents 集群`
- 目标还不是 Git 目录时，先并行探索，再统一收口
- 单文件、小范围事实核查、强耦合调整时不强行并行

## 5. 运行态边界

- `~/.codex/history.jsonl`、`sessions/`、`archived_sessions/`、sqlite、插件缓存和当前设置继续留在本地
- Codex 原生执行文件留在本地，不写入正式学习文档
- 正式学习文档以当前仓库为准
