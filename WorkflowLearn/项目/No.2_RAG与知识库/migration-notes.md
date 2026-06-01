# No.2_RAG与知识库 迁移说明

> 最近确认时间：2026-04-17

## 旧文件角色

| 旧文件 | 当前角色 | 说明 |
|---|---|---|
| `_legacy/初始文档.md` | 历史课程底稿 | 用于抽取概念与案例框架 |
| `_legacy/学习路径.md` | 历史模块图 | 用于恢复节点结构 |
| `_legacy/掌握卡片/*.md` | 历史验证记录 | 用于提取错误、验证高光、类比 |
| `_legacy/项目信息.md` | 历史状态摘要 | 不再作为新状态真相层 |
| `_legacy/_snapshot.md` | 历史快照 | 不再自动维护 |
| `_legacy/知识白板.canvas` | 历史可视化 | 暂不纳入正式状态层 |

## 新文件角色

| 新文件 | 角色 |
|---|---|
| `project.md` | 项目首页与长期定位 |
| `handover.md` | 当前判断与下一步 |
| `state.md` | 轻量可恢复状态 |
| `curriculum/concepts.md` | 稳定概念 |
| `curriculum/volatile.md` | 时效内容与默认值 |
| `curriculum/sources.md` | 迁移依据与待核验来源 |
| `curriculum/labs.md` | 实操、错误与诊断记录 |
| `curriculum/outcomes.md` | 对应用场景与成果的映射 |
| `refresh/refresh-queue.md` | 待刷新条目 |
| `refresh/verification-policy.md` | 项目级验证规则 |

## 当前迁移范围

- 已迁：`P1/P2/P3/A1/A2/B1/B2`
- 待补：`B3/C1`
- 时效项不进稳定层
- 旧文件已归档到 `_legacy/`（2026-04-17），不再作为新系统真相源，仅保留作历史抽取素材。
