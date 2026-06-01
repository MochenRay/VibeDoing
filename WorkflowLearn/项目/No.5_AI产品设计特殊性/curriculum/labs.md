# labs

> 最近确认时间：2026-06-01
> 状态：作品模板已扩写

## Lab 1：Fallback Ladder

- 目标：为一个 AI 功能设计主路径、降级路径和人工接管路径
- 交付物：`fallback-ladder.md`
- 必须包含：触发条件、替代输出、用户感知、责任归属
- 通过条件：失败后用户仍能继续推进任务，不会直接卡死

## Lab 2：Uncertainty Copy Pack

- 目标：把不确定性翻译成用户能理解的表达
- 交付物：`uncertainty-copy.md`
- 必须包含：高 / 中 / 低三档表达、引用提示、不能回答时的默认文案
- 通过条件：用户不会误以为系统“一定正确”或“一定知道”

## Lab 3：HITL Boundary Map

- 目标：划分哪些交给 AI，哪些必须人工确认
- 交付物：`hitl-boundary-map.md`
- 必须包含：风险、准确率、可逆性、合规性四个维度，以及谁来接手
- 通过条件：边界足够清楚，能直接落成流程图或 SOP

## Lab 4：Feedback and Incident Loop

- 目标：把用户反馈接到后续 eval 和迭代里
- 交付物：`feedback-loop.md`
- 必须包含：收集哪些信号、如何存储、谁负责复盘、如何回流到 eval
- 通过条件：反馈不是埋点摆设，而能进入真实改版闭环

## Lab 5：Failure State Journey

- 目标：为一个 AI-native 交互设计错误状态和恢复状态
- 交付物：`failure-state-journey.md`
- 必须包含：重试、换问法、转人工、查看依据四条路径中的至少两条
- 通过条件：失败时界面仍然“可继续”，而不是只报错

## Lab 6：Trust Brief

- 目标：为一个高风险 AI 功能写信任设计说明
- 交付物：`trust-brief.md`
- 必须包含：预期、限制、提示、升级路径、残余风险
- 通过条件：能明确告诉用户“能信到哪一步、不能信到哪一步”

## Lab 7：Industry Handoff Rule

- 目标：把同一个 AI 功能放进两个不同行业，比较接管规则如何变化
- 交付物：`industry-handoff-rule.md`
- 必须包含：风险等级、可逆性、责任主体、人工 SLA、触发条件、升级路径
- 通过条件：不能只写“低置信度转人工”，必须说明为什么这个行业要在这个节点接管
