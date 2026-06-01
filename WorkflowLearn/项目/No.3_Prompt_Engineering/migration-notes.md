# No.3_Prompt_Engineering / Migration Notes

> 最近确认时间：2026-04-17
> 状态：首版迁移说明

## 从旧文档迁移到新 schema

旧文件已归档到 `_legacy/`（2026-04-17），不再作为新系统真相源，仅保留作历史抽取素材。

旧文档的核心内容被重新分成四层：

- `concepts.md`：Prompt、System Prompt、few-shot、structured outputs、tool contracts、Generative UI
- `volatile.md`：厂商 API、SDK 语法、Thinking Mode 命名、具体 prompt recipe
- `labs.md`：写 prompt brief、写 schema、设计工具边界、做注入防护、做 UI 输出验证
- `outcomes.md`：如何把这套能力变成可展示的应用产出和面试表达

## 旧件位置

- `_legacy/初始文档.md`
- `掌握卡片/` 原为空目录，已删除

## 需要丢到时效层的内容

- 具体厂商的 API 形态
- 具体 SDK 示例代码
- 当前版本的 structured output / tool calling 命名
- 某个模型“最适合”的经验结论

## 需要保留到稳定层的内容

- Prompt 是接口合同
- System Prompt / User Prompt 的层级边界
- few-shot 的示例选择原则
- 结构化输出和 schema-first 设计
- 工具调用的边界与失败处理
- Generative UI / AI-native 交互的输出设计
