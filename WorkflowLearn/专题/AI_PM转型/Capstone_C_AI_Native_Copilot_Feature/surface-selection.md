# surface-selection

## 1. 候选 surface

- `Chat`
- `Sidebar Copilot`
- `Inline Edit`
- `Workspace Canvas`
- `Modal Review`

## 2. 选择标准

- 用户任务是否持续在主工作区发生
- 输出是否需要被继续编辑和复用
- 信息密度是否高到需要证据和结果并排展示
- 用户下一步是“继续做事”还是“继续提问”

## 3. 结论

主 surface 选择：`Workspace Canvas + Inline Edit + Sidebar Evidence Drawer`

原因：

- 客户 brief 和方案稿本身就是主工作对象，不能被聊天流挤出主界面
- 用户需要在段落级接受、修改、拒绝建议，所以必须支持 inline edit
- 证据来源和风险提示需要并排显示，避免“看答案再回头找依据”的来回切换

## 4. 为什么不选纯 Chat

- Chat 更适合探索，不适合沉淀结构化产物
- Chat 输出很难自然绑定“段落接受/拒绝/追溯来源/发起审核”
- Chat 容易把下一步动作隐藏在对话里，而不是显式变成界面行动

## 5. Chat 的位置

- 用作探索与追问入口
- 用作失败后的自然语言解释层
- 不作为默认主工作台
