# No.1_大模型基础认知 迁移说明

> 最近确认时间：2026-04-17

## 目的

说明旧项目文件在新 schema 下如何理解。
本文件只做结构映射，不迁移正文。

## 旧文件角色

| 旧文件 | 当前角色 | 说明 |
|---|---|---|
| `_legacy/初始文档.md` | 历史材料 | 可用于后续抽取稳定概念与时效项 |
| `_legacy/项目信息.md` | 历史状态摘要 | 不再作为新系统真相层 |
| `_legacy/学习路径.md` | 历史路径展示 | 不再承担状态职责 |
| `_legacy/_snapshot.md` | 历史快照 | 不再自动维护 |
| `_legacy/学习报告.md` | 历史总结 | 不再作为必须产物 |
| `_legacy/掌握卡片/*.md` | 历史节点记录 | 后续按需拆入 `concepts/labs/volatile` |
| `_legacy/知识白板.canvas` | 历史可视化 | 暂不纳入新状态真相层 |

## 新文件角色

| 新文件 | 角色 |
|---|---|
| `project.md` | 项目首页与长期定位 |
| `handover.md` | 当前判断与下一步 |
| `state.md` | 轻量可恢复状态 |
| `curriculum/concepts.md` | 稳定概念 |
| `curriculum/volatile.md` | 时效内容 |
| `curriculum/sources.md` | 来源线索 |
| `curriculum/labs.md` | 实操和失败归因 |
| `curriculum/outcomes.md` | 应用映射与成果输出 |
| `refresh/refresh-queue.md` | 待刷新项 |
| `refresh/verification-policy.md` | 项目级验证策略 |

## 当前迁移原则

- 旧文件已归档到 `_legacy/`（2026-04-17），不再作为新系统真相源，仅保留作历史抽取素材。
- 新文件先建立空骨架，再决定迁移顺序。
- 稳定概念与时效内容必须拆开。
- 旧“已掌握/已完结”状态不自动继承。
