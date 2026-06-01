# No.6_Agent概念 迁移说明

> 最近确认时间：2026-04-17

## 旧文件角色

| 旧文件 | 当前角色 | 说明 |
|---|---|---|
| `_legacy/初始文档.md` | 历史课程底稿 | 用于抽取 Agent / Tool / MCP / Computer Use 的基础骨架 |
| `掌握卡片/` | 无归档内容 | 原目录为空，已删除 |

## 新文件角色

| 新文件 | 角色 |
|---|---|
| `project.md` | 项目首页与定位 |
| `handover.md` | 当前判断与冻结决策 |
| `state.md` | 轻量可恢复状态 |
| `curriculum/concepts.md` | 稳定概念 |
| `curriculum/volatile.md` | 时效项与默认值 |
| `curriculum/sources.md` | 依据与外部核验 |
| `curriculum/labs.md` | 实操、验证、错误归因 |
| `curriculum/outcomes.md` | 应用场景与成果映射 |
| `refresh/refresh-queue.md` | 待刷新条目 |
| `refresh/verification-policy.md` | 验证规则 |

## 当前迁移范围

- 已迁：`Agent / Workflow / Harness` 的首版稳定主干
- 待补：`Computer Use`、多 Agent 协作、复杂 workflow capstone
- 时效项不进稳定层
- 旧文件已归档到 `_legacy/`（2026-04-17），不再作为新系统真相源，仅保留作历史抽取素材。
