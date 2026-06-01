# ui-brief

## 1. 页面结构

- 左侧：来源与上下文面板
- 中间：客户 brief / 方案稿主画布
- 右侧：证据抽屉、风险提示、AI 建议和待确认事项

## 2. 核心组件

- `Context Intake Panel`
  - 展示 CRM 字段、会议纪要、历史案例、上传文件
- `Draft Blocks`
  - 每个段落都可接受、改写、锁定或发起审核
- `Evidence Drawer`
  - 显示当前段落引用的来源、抽取时间和置信提示
- `Action Rail`
  - 显示“补信息”“重跑建议”“提交审核”“标记为人工完成”
- `Risk Banner`
  - 高风险内容置顶提醒，不允许静默通过

## 3. 状态设计

- `draft`
- `needs_more_context`
- `needs_human_review`
- `approved_for_use`

## 4. 界面原则

- AI 输出必须贴近用户正在操作的对象
- 任何高风险内容都必须带出处或显式说明“无可靠证据”
- 用户修改行为比点赞更重要，必须被记录
