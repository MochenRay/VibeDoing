# refresh-queue

> 最近确认时间：2026-04-16

## 待刷新

- `B1 当前厂商快照（下次正式学习前）`
  - `reason`: 模型名、价格、上下文窗口会继续变化
  - `refresh_rule`: 开始学习本模块前先复核官方页面，不直接复用旧表格

- `具体 tokenizer 经验值`
  - `reason`: 中英文 token 经验值和多模态 token 预算都受模型族影响
  - `refresh_rule`: 做真实成本估算或模型路由时先按当期官方文档复核

## 已处理

- `B1 主流模型对比`
  - `checked_on`: `2026-04-16`
  - `outcome`: 官方页面已与旧项目里的模型表和推荐结论明显错位，因此继续保留在 `volatile`，不升格为稳定主干
  - `sources`:
    - [OpenAI API Pricing](https://openai.com/api/pricing/)
    - [Anthropic Models overview](https://platform.claude.com/docs/en/about-claude/models/overview)
    - [Gemini API Models](https://ai.google.dev/gemini-api/docs/models)

- `上下文窗口与价格表`
  - `checked_on`: `2026-04-16`
  - `outcome`: 旧表格只适合作为历史材料；当前学习中只保留“能力 × 约束 × 成本”的选型框架

- `Token / Context / Hallucination 主线`
  - `checked_on`: `2026-04-16`
  - `outcome`: 已确认课程主线应围绕 token 预算、working memory、context limits 和 hallucination mitigation 组织
