# labs

> 最近确认时间：2026-06-01
> 状态：作品模板已扩写

## Lab 1：Prompt Brief

- 目标：把一个模糊需求写成可执行 prompt
- 交付物：`prompt-brief.md`
- 必须包含：角色、任务、输入、输出、约束、示例、失败边界
- 通过条件：另一个人不看口头背景也能直接复用

## Lab 2：Schema Spec

- 目标：把一段自然语言回答改写成 JSON / 表格 / UI descriptor
- 交付物：`schema-spec.md`
- 必须包含：字段、类型、枚举、必填项、兜底项、错误输入样例
- 通过条件：下游系统可以无歧义解析，不靠人工猜测

## Lab 3：Tool Contract

- 目标：为一个工作流定义工具边界
- 交付物：`tool-contract.md`
- 必须包含：工具名、参数、返回值、失败条件、副作用、确认机制
- 通过条件：能清楚说明何时该调用、何时不该调用、失败后怎么收口

## Lab 4：Prompt Guardrail Policy

- 目标：识别并隔离 prompt 注入风险
- 交付物：`prompt-guardrails.md`
- 必须包含：系统边界、输入过滤、不可覆盖规则、外部知识边界、回退策略
- 通过条件：用户输入不能轻易覆盖核心规则，且高风险请求有降级路径

## Lab 5：Generative UI Descriptor

- 目标：把 AI 输出改成可渲染的交互结构
- 交付物：`ui-descriptor.json` 或 `ui-brief.md`
- 必须包含：至少一个表单、卡片或步骤流，以及用户下一步动作
- 通过条件：输出不止能“展示”，还能驱动下一步操作

## Lab 6：Prompt Iteration Record

- 目标：对比两个 prompt 版本的输出差异
- 交付物：`iteration-record.md`
- 必须包含：v1/v2 对比、失败模式、稳定性、可复用性、剩余风险
- 通过条件：能说清改动带来的收益、副作用和后续该不该继续调 prompt

## Lab 7：Prompt / Tool Eval Pack

- 目标：为一个 prompt + tool 场景设计最小评估包
- 交付物：`prompt-tool-eval-pack.md`
- 必须包含：代表性样本、失败样本、schema 校验项、工具选择判断、参数正确性、人工复核位
- 通过条件：不是只展示一条成功 demo，而是能发现回归、误调工具和结构化输出错误
