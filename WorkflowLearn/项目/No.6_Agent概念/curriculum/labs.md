# labs

> 最近确认时间：2026-06-01
> 状态：围绕 workflow / agent / harness 作品包刷新

## Lab 1：Agent vs Workflow Memo

- 目标：把“到底要不要上 agent”写成可评审 memo。
- 交付物：`agent-vs-workflow.md`
- 必须包含：任务特征、确定路径、需要 agent 判断的环节、环境不确定性、工具种类、恢复成本、为什么不用更简单方案
- 通过条件：结论不是“更先进所以更好”，而是能解释哪些部分用 workflow，哪些部分才值得交给 agent。

## Lab 2：Tool Contract Pack

- 目标：为查询工具、写入工具和高风险工具各写一份正式 contract，并标出是否适合接入 MCP。
- 交付物：`tool-contract-pack.md`
- 必须包含：输入、输出、错误、权限、确认机制、幂等性、副作用、审计字段、MCP tool / resource 边界
- 通过条件：能区分只读工具、可回滚工具和高风险工具，并能说明 registry 中如何发现、启用和禁用工具。

## Lab 3：State / Resume Scheme

- 目标：为一个长流程任务设计状态结构、检查点和恢复策略。
- 交付物：`state-resume-scheme.md`
- 必须包含：状态字段、检查点、幂等键、恢复条件、重试上限、超时、人工接手和完成判定
- 通过条件：任务中断后能说明如何从中间状态继续，而不是重新来过。

## Lab 4：Long-running Harness

- 目标：为一个 30 分钟以上的任务设计 runtime loop。
- 交付物：`long-running-harness.md`
- 必须包含：initializer、session startup、tool registry load、progress artifact、checkpoint、failure rollback、session end cleanup
- 通过条件：设计里有清晰的增量推进逻辑、恢复协议和人工暂停点，而不是一次性大任务。

## Lab 5：Observability Blueprint

- 目标：写一份 agent runtime 的可观测蓝图。
- 交付物：`observability-blueprint.md`
- 必须包含：tool call、state change、decision log、error taxonomy、handoff artifact、报警规则、上线 gate
- 通过条件：出现故障时可以基于日志和 artifact 定位问题，并能判断是模型、工具、状态还是流程错误。

## Lab 6：Agent Eval Pack

- 目标：设计一组判断 agent 是否可上线、是否需要多 agent 的 eval。
- 交付物：`agent-eval-pack.md`
- 必须包含：任务集、成功标准、失败分类、人工评审样本、回归用例、多 agent 升级条件
- 通过条件：多 agent 不是默认方案，只有 eval 证明单 agent / workflow 无法达标时才升级。

## 常见错误

- 把 agent 当成只会聊天的模型
- 工具设计过大，职责不清
- 只有最终答案，没有中间状态
- 失败后无法恢复
- 把组织流程问题误判成模型问题
- 没有 eval 就先拆成多个 agent
