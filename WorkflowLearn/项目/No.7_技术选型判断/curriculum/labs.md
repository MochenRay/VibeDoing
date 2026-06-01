# labs

> 最近确认时间：2026-06-01
> 状态：已强化 solution routing、ROI、rollout、监控与 fine-tune 核验练习

## Lab 1：Solution Routing

- 目标：把一组需求路由到正确方案层。
- 交付物：`solution-routing.md`
- 必须包含：prompt、RAG、workflow、agent、fine-tune、buy、assemble、build 路径及排除理由
- 通过条件：不是所有问题都被推到“上 agent”。

## Lab 2：Selection Memo

- 目标：为一个真实业务写一页选型 memo。
- 交付物：`selection-memo.md`
- 必须包含：业务目标、任务约束、候选方案、build/buy/assemble 判断、为什么不选其他方案、核心风险
- 通过条件：评审者能看懂这是“做正确的事”，不是“用最新的技术”。

## Lab 3：ROI Model

- 目标：为一个 AI 功能做正式 ROI 拆解。
- 交付物：`roi-model.md`
- 必须包含：token、工具/搜索/检索、缓存、存储、人工复核、监控、rollout、人工节省、风险成本、回收周期、敏感因素
- 通过条件：不只会算 token，还会算工具链、人工审核和运营成本。

## Lab 4：Launch / Rollout Plan

- 目标：设计一个从 demo 到 production 的 rollout 路线。
- 交付物：`rollout-plan.md`
- 必须包含：试点范围、扩大上线门槛、人工复核、SOP 变化、权限、监控、停止条件和回滚策略
- 通过条件：方案能落到真实组织，不停留在 demo。

## Lab 5：Productization Checklist

- 目标：把一个技术方案写成产品化清单。
- 交付物：`productization-checklist.md`
- 必须包含：UI、权限、日志、接管、反馈、评估、监控、成本观测与 fine-tune 当前核验项
- 通过条件：不只是“能跑”，而是“能上线、能维护、能解释”。

## 常见错误

- 先看模型再看问题
- 把所有场景都往 agent 上推
- 把 fine-tune 当成默认升级路径
- 只算 token，不算组织成本
- 只看技术先进性，不看维护和上线
