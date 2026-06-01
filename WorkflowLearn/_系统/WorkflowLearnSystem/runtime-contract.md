# runtime-contract

> 最近确认时间：2026-04-16

## 1. 合同目标

`runtime-contract` 描述任何宿主在运行 `WorkflowLearnSystem` 时必须满足的最小契约。
它不规定实现语言，不规定工具品牌，只规定能力、顺序和产物。

## 2. 合同对象

- `Core`：共享学习规则。
- `Teaching Contract`：共享教学规则。
- `Runtime`：承载一次学习会话的执行环境。
- `Adapter`：把宿主能力翻译成 Core 可理解的动作。
- `Project State`：项目级恢复状态。
- `Artifacts`：写回的长期结果。

## 3. 必要能力

任何合规 runtime 都必须提供：

1. 读取长期文档。
2. 识别当前项目与模块。
3. 恢复上次学习状态。
4. 记录本轮状态变化。
5. 写回长期文档。
6. 标记时效内容与刷新需求。
7. 支持失败后暂停，而不是伪造完成。

## 4. 会话输入

每次运行必须至少知道：

- `host`
- `workspace`
- `project`
- `current_mode`
- `entrypoint`
- `known_state_refs`
- `target_module`
- `teaching_phase`
- `round`
- `error_count`
- `writeback_targets`

如果其中某项缺失，runtime 必须先恢复或显式标记缺失，不得默认猜测。

## 5. 标准状态流转

runtime 只允许以下主路径：

`idle -> recovered -> active -> verified -> written -> refreshed -> closed`

补充分支：

- `active -> blocked`
- `verified -> needs_refresh`
- `written -> reopened`
- `blocked -> recovered`

状态切换必须有文字证据，不允许只在脑内完成。

## 6. 运行阶段定义

### 6.1 恢复

恢复阶段的任务是把项目状态、模块位置、未完成问题和最近确认时间找回来。
恢复失败时，必须停在 `blocked`，等待补齐信息。

### 6.2 学习

学习阶段的任务是产出理解、比较、归纳、例子和开放问题。
学习阶段不负责最终定稿，不负责把时效内容伪装成稳定知识。

### 6.3 验证

验证阶段确认三件事：

- 概念有没有理解错
- 事实有没有过时
- 产物有没有可写回价值

验证没通过时，不能直接进入正式写回。

### 6.6 教学协议扩展

如果当前会话属于教学型学习，runtime 还必须保证：

- 能恢复讲解 / 理解确认 / 掌握验证 / 费曼或实操所处阶段
- 能恢复当前轮次和错误计数
- 能在回退时写清 `fallback_reason`
- 能在通过后产出 `review_due` 和 `next_teaching_step`

### 6.4 写回

写回阶段只接受已验证内容，并且必须能被未来恢复。
写回内容应最小化重复，只留下长期有用的信息。

### 6.5 刷新

刷新阶段检查时效项是否需要重查。
如果某个结论依赖最近变化快的外部事实，它必须进入刷新队列或 volatile 区域。

## 7. 输出要求

每轮 runtime 至少要产出：

- 当前状态摘要
- 本轮学习结论
- 验证结果
- 写回清单
- 刷新清单
- 教学阶段结果
- 下一步动作

## 8. 失败规则

- 缺少恢复信息时，不允许假装继续。
- 验证失败时，不允许写成正式结论。
- 发现时效过期时，不允许继续沿用旧快照。
- 宿主能力不足时，只能降级流程，不能改 core 规则。

## 9. 兼容原则

Claude、Gemini、Codex 可以有不同 adapter，但它们必须遵守同一份 runtime contract。
如果某个宿主做不到某一步，优先改 adapter，不优先改 core。
