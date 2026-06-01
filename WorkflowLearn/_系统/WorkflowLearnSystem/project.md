# WorkflowLearnSystem

## 用途

把当前 `WorkflowLearn / Vibe Learning` 仓库重构成可同时支持 Codex、Claude、Gemini，并可独立运行、独立开源的长期学习操作系统。

## 目标

- 重写控制层，移除绑定单一宿主的遗留假设。
- 重建课程结构，把稳定概念、时效快照、状态层拆开。
- 清空并重建旧状态层，不再修历史进度一致性。
- 让 `WorkflowLearn` 在脱离 `AI-Shared` 的情况下也能完整运行。

## 范围

- 宿主适配层与 runtime contract
- 教学协议与回退规则
- 文件 schema 与状态模型
- 课程目录重构
- 时效内容刷新机制
- 仓库自包含与未来开源边界

## 非范围

- 修复旧项目的历史快照一致性
- 保留旧学习进度作为正式状态
- 维护静态模型榜单、价格表或一次性快照为正式知识

## 成功标准

- 仓库内存在一套 `host-agnostic core + adapters` 的正式系统方案
- 仓库内存在一套独立于宿主的 `Teaching-Contract`
- 课程结构明确分成稳定概念层、时效层、状态层
- `WorkflowLearn` 单独打开即可运行，不依赖 `AI-Shared`
- `No.7` 与 `No.8` 被识别为优先重写模块

## 当前状态

- 2026-04-16：系统问题与迁移方向已冻结。
- 旧系统的核心问题已明确：宿主不兼容、状态源漂移、时效层混杂、文件 schema 漂移。
- 新系统目标已收紧为多宿主支持：共享同一核心规则，通过 Codex / Claude / Gemini 适配层接入。
- `Core-Learning.md`、`runtime-contract.md`、`workflow-spec.md`、`file-schema.md` 和三份 `adapters/*.md` 已在本地落盘。
- 1.0 中有价值的教学协议已被识别为系统层能力，而不是“以后再补的内容层”。
- `state.md`、`refresh/`、`curriculum/` 模板层已在本地落盘，可用于后续课程迁移。
