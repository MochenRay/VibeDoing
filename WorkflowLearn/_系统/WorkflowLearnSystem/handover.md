# WorkflowLearnSystem 交接页

> 更新日期：2026-04-16

## 当前判断

旧 `WorkflowLearn` 系统不适合继续在原架构上小修小补。

结论是：

- **系统层重写**
- **课程层迁移与升级**
- **状态层重置**
- **时效层建立刷新机制**
- **正式系统收回本地仓库**

这不是“整仓推倒重来”，但也不是“修几个错字继续用”。

## 已冻结的关键决策

1. 不再为旧 `项目信息.md`、`_snapshot.md`、`学习报告.md` 修历史一致性。
2. 新系统不再绑定单一宿主，而是采用“共享核心规则 + Codex / Claude / Gemini 适配层”。
3. 正式系统定义回到 `WorkflowLearn` 仓库内部，`AI-Shared` 不再是运行时依赖。
4. 课程内容以后必须区分：稳定概念、时效快照、项目状态。
5. 1.0 的教学性要作为独立教学协议继承，不再混进宿主规则或旧状态文件。

## 当前产出

- `project.md`：系统首页
- `Core-Learning.md`：宿主无关学习内核
- `runtime-contract.md`：运行最小契约
- `workflow-spec.md`：标准学习闭环
- `file-schema.md`：正式文档最小 schema
- `Teaching-Contract.md`：教学协议主合同
- `teaching/*.md`：讲解、验证、复习策略
- `adapters/codex.md`、`adapters/claude.md`、`adapters/gemini.md`：宿主适配层
- `state.md`：轻量恢复状态模板
- `refresh/refresh-queue.md`、`refresh/verification-policy.md`：刷新与验证模板
- `curriculum/*.md`：课程层模板

## 未决问题

1. `AI-Shared` 后续是保留镜像，还是完全停止同步。
2. 教学状态字段最终固定写在 `state.md` 还是拆到项目级 `review` 文档。

## 下一步

1. 把教学状态字段接入项目级 `state.md` 模板
2. 清理残留的 1.0 外围参考件
3. 再进入第一批课程迁移
