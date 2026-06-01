# file-schema

> 最近确认时间：2026-06-01

## 1. 目的

`file-schema` 定义 `WorkflowLearnSystem` 里长期文档的最小结构。
目标不是统一排版，而是统一恢复、验证、写回和刷新时所依赖的语义字段。

## 2. 总原则

- 所有长期文档都必须可由任意宿主读取。
- 所有容易过期的内容都必须有明确日期。
- 所有状态都必须能恢复，不能只存在聊天上下文里。
- 所有文件都要区分“稳定内容”与“时效内容”。
- 所有正式文件都不得包含宿主专属命令。

## 3. 项目级文件

### 3.1 `project.md`

用途：项目首页与稳定定位。

必备字段：

- `name`
- `purpose`
- `goals`
- `scope`
- `non_goals`
- `success_criteria`
- `current_state`

### 3.2 `handover.md`

用途：当前判断、已冻结决策、下一步。

必备字段：

- `current_judgment`
- `frozen_decisions`
- `open_questions`
- `current_outputs`
- `next_steps`

### 3.3 `state.md`

用途：轻量、可恢复的项目状态源。

必备字段：

- `status`
- `current_module`
- `last_verified`
- `next_action`
- `stale_items`
- `blocked_items`

教学型项目建议再增加：

- `teaching_phase`
- `round`
- `concept_type`
- `error_count`
- `fallback_reason`
- `review_due`
- `review_count`
- `last_reviewed`

时间戳语义：

- `state.md` 的最近确认时间表示学习状态、教学阶段或下一步判断发生过确认。
- `refresh-queue.md` 的最近确认时间表示时效项发生过核验或刷新登记。
- 两者可以不同步；不能因为刷新队列更新，就自动把教学状态改成已验证。
- 如果刷新结果改变了当前教学下一步，才同步更新 `state.md`。

## 4. Curriculum 文件

### 4.1 `concepts.md`

用途：稳定概念。

### 4.2 `teaching-guide.md`

用途：live teaching 的详讲稿，负责把稳定概念展开成直觉、例子、反例、边界、误区与理解确认问题。

### 4.3 `volatile.md`

用途：时效内容与待刷新判断。

### 4.4 `sources.md`

用途：来源与核验依据。

### 4.5 `labs.md`

用途：实操与练习记录。

### 4.6 `outcomes.md`

用途：把模块映射到应用场景、能力迁移与可交付产出。

## 5. 记录层文件

### 5.1 `refresh-queue.md`

用途：列出需要重新核实的时效项。

### 5.2 `verification-policy.md`

用途：定义何时算验证通过。

## 6. 格式约束

- 标题层级保持稳定，方便恢复。
- 文件名保持简短，便于跨宿主引用。
- 不把运行日志、聊天记录、调试输出写成正式内容。
- 不把 adapter 细节写进共享 schema。

## 7. 推荐目录形态

```text
_系统/WorkflowLearnSystem/
  Core-Learning.md
  runtime-contract.md
  workflow-spec.md
  file-schema.md
  Teaching-Contract.md
  project.md
  handover.md
  state.md
  teaching/
    lecture-policy.md
    validation-policy.md
    review-policy.md
  curriculum/
    concepts.md
    teaching-guide.md
    volatile.md
    sources.md
    labs.md
    outcomes.md
  refresh/
    refresh-queue.md
    verification-policy.md
    scan-policy.md
  adapters/
    codex.md
    claude.md
    gemini.md
```
