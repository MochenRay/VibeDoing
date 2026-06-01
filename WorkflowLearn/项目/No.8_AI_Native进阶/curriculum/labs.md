# labs

> 最近确认时间：2026-06-01
> 状态：已强化 surface、multimodal、feedback-to-eval 与 launch gate 练习

## Lab 1：Eval-aware PRD

- 目标：写一份把目标、评估和上线门槛绑在一起的 AI-native 需求稿。
- 交付物：`eval-aware-prd.md`
- 必须包含：目标、成功标准、surface 假设、eval 方案、上线门槛、人工接管
- 通过条件：需求稿不再只讲体验，而是从一开始就内置评估与上线条件。

## Lab 2：Feedback Loop Blueprint

- 目标：为一个 AI feature 设计显式与隐式反馈通道。
- 交付物：`feedback-loop-blueprint.md`
- 必须包含：显式反馈、隐式行为信号、数据回流、eval dataset 归档方式、标注负责人、复盘节奏
- 通过条件：反馈数据可以进入 eval、优化和 launch readiness，而不是只存在埋点系统里。

## Lab 3：Surface Selection Memo

- 目标：在 chat、copilot、inline edit、canvas/workbench、voice/live/multimodal 中做 surface 选择。
- 交付物：`surface-selection.md`
- 必须包含：任务类型、信息密度、用户下一步动作、模态输入、主 surface、辅助 surface、为什么不选其他 surface
- 通过条件：surface 选择基于任务摩擦，而不是跟风。

## Lab 4：Multimodal Flow

- 目标：设计一个多模态或 voice/live 任务流程。
- 交付物：`multimodal-flow.md`
- 必须包含：输入、实时性要求、处理、输出、失败接管、证据展示、隐私权限
- 通过条件：流程里能说明哪些步骤必须可验证，哪些步骤可以模糊生成。

## Lab 5：Launch Readiness Review

- 目标：写一份 AI-native feature 的上线评审。
- 交付物：`launch-readiness.md`
- 必须包含：护栏指标、eval dataset 状态、反馈遥测、人工接管、回滚条件、surface 风险、监控项
- 通过条件：能据此做一次真实上线讨论，而不是停留在概念演示。

## 常见错误

- 把 AI native 只理解成聊天框
- 只看模型能力，不看 surface 适配
- 只有满意度，没有反馈回路
- 没有接管和回滚设计
