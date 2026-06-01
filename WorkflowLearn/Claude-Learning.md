# Claude-Learning

> 最近确认时间：2026-04-16
> 状态：兼容桥接文件，不再是正式规则来源

## 说明

这个文件保留是为了兼容旧引用和旧入口习惯。
它不再承载 `WorkflowLearn` 的正式系统规则，也不再定义状态机、slash command 或文件写回协议。

## 新入口

- Claude：优先读 [CLAUDE.md](./CLAUDE.md)
- Gemini：优先读 [GEMINI.md](./GEMINI.md)
- Codex：优先读 [AGENTS.md](./AGENTS.md)

## 正式系统来源

`WorkflowLearn` 现在的正式系统定义在：

- `_系统/WorkflowLearnSystem/project.md`
- `_系统/WorkflowLearnSystem/Core-Learning.md`
- `_系统/WorkflowLearnSystem/Teaching-Contract.md`
- `_系统/WorkflowLearnSystem/runtime-contract.md`
- `_系统/WorkflowLearnSystem/workflow-spec.md`
- `_系统/WorkflowLearnSystem/file-schema.md`
- `_系统/WorkflowLearnSystem/teaching/`
- `_系统/WorkflowLearnSystem/adapters/`

## 已废弃假设

以下内容不再是现行系统的一部分：

- slash command 路由
- `write_to_file`
- 自动 `_snapshot.md`
- `项目信息.md` / `学习路径.md` / `学习报告.md` 作为状态真相层
- 旧文件（`项目信息.md` / `学习路径.md` / `_snapshot.md` / `学习报告.md` / `知识白板.canvas` / `掌握卡片/`）已归档到各项目 `_legacy/`
- 单宿主状态机

## 本地作用

这个文件现在只做一件事：
把旧入口习惯导向新的多宿主系统。
