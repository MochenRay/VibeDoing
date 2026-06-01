# concepts

> 最近确认时间：2026-06-01
> 状态：已强化 surface selection、voice/live/multimodal、feedback telemetry 与 launch readiness

## 模块 P1：什么是 AI Native PM

- AI Native PM 不是“会用模型的 PM”，而是把产品体验、模型能力、反馈闭环和持续评估放在同一系统里思考的人。
- AI native 产品的关键不是文案像不像 AI，而是是否真的改变了产品的交互、生产方式和迭代方式。

## 模块 P2：Eval-aware PM

- `eval-aware` 意味着产品设计从需求阶段就要考虑怎么验证、怎么上线、怎么回滚。
- 好的 PM 不只是看结果，还要设计指标、样本、门槛和反馈采集方式。
- AI 产品的“感觉不错”必须被翻译成可执行的评估方案。

## 模块 P3：Feedback Loop

- 用户反馈不只是满意度按钮，还包括修改行为、重新生成、复制、停留、接管和升级人工。
- 反馈闭环的价值在于把产品使用过程变成持续改进的证据链。
- 有效反馈必须能回流到 eval dataset：哪些样本进入评测、谁标注、如何复盘、何时影响上线门槛。
- 没有反馈闭环的 AI 产品，很容易越用越漂。
- 本模块的反馈闭环偏战略层：它关心反馈如何进入路线图、eval dataset 和运营机制；No.5 F6 处理单次失败中的战术反馈与接管。

## 模块 P4：Native Surfaces

- AI native surface 不只是一种聊天界面，而是一组适合任务和上下文的原生交互。
- 常见 surface 包括 chat、copilot、inline edit、canvas / workbench、command surface、voice / live / multimodal input。
- surface 选择要看任务阶段：探索适合 chat，持续协作适合 copilot，局部改写适合 inline edit，高信息密度产物适合 canvas / workbench，移动或低手占用场景才优先 voice / live。
- 产品判断不是“哪种最酷”，而是“哪种 surface 最适合这个任务、这个时机和这个人机分工”。

## 模块 P5：Multimodal Judgment

- 多模态的重点不是“能看图说话”，而是能否把图、音、文本和上下文统一到一个任务链里。
- 语音、实时对话和多模态输入要先判断是否减少采集、理解、确认或执行摩擦。
- 多模态 surface 还要明确证据展示、失败接管、隐私权限和不可验证输出的处理方式。

## 模块 P6：Trust / Safety / Handoff

- AI native 产品必须设计失败提示、接管入口、权限边界和升级路径。
- Trust 不是附加项，而是产品是否可用的前提。
- 高风险场景必须把人工复核和停止条件作为产品的一部分。

## 模块 P7：Observability 与 Launch Readiness

- 既然产品会变化，就必须看得见变化。
- 需要能追踪用户反馈、模型变化、surface 变化、eval 变化和上线后的风险。
- launch readiness 要把 eval 门槛、反馈遥测、人工接管、回滚条件和 surface 风险放在同一张表里。
- AI native 功能不能只靠一次性 launch，要能持续运营和持续评估。

## 模块 P8：User Onboarding / Expectation Management

- AI-native 界面要帮助用户形成正确预期：能做什么、不能做什么、何时要核实、何时会转人工。
- onboarding 不是功能说明墙，而是把示例、边界、默认输入、可撤销操作和能力展示嵌进任务流。
- prompt 素养可以被产品化，但不能把学习成本全部甩给用户。

## 模块 P9：Internationalization / Culture

- AI 输出质量会受语言、文化规范、语气、禁忌、格式和本地法规影响。
- 国际化不是翻译 UI，而是验证不同语言和文化下的可接受输出、风险边界和人工接管策略。
- 面向跨地区用户时，eval dataset 和 trust copy 也要本地化。

## 模块 P10：Accessibility for AI-native UX

- 语音、多模态、动态生成 UI 和实时输出会带来新的无障碍挑战。
- AI-native surface 要考虑屏幕阅读器、键盘操作、字幕、可暂停、可撤销、动态内容提示和替代输入。
- 无障碍不是附加项；它会影响 AI 结果能否被理解、核实和安全操作。

## 当前不进入稳定层的内容

- 模型对齐史的细节表
- benchmark 排名
- 论文快照
- 厂商多模态功能表
- 具体地区文案规范和无障碍实现清单
