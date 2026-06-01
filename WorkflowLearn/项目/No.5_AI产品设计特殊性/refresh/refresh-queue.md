# refresh-queue

> 最近确认时间：2026-06-01
> 状态：待刷新项已按行业与产品阶段重写

## 待刷新项

- `行业特定的置信度阈值`
  - `reason`: 阈值受行业风险、人工成本和法律责任约束
  - `refresh_when`: 锁定医疗、金融、客服等具体场景时

- `转人工和人工确认的触发条件`
  - `reason`: 与组织 SOP、权限和响应时效绑定
  - `refresh_when`: 写真实 workflow 或上线方案时

- `copy / error state 写法`
  - `reason`: 产品语气、受众和风险披露要求变化快
  - `refresh_when`: 做具体页面或文案包时

- `风险等级映射`
  - `reason`: 同一任务在不同行业的可逆性和合规要求不同
  - `refresh_when`: 做行业化方案时

- `AI-native trust / failure design 趋势`
  - `reason`: 交互形态仍在快速变化
  - `refresh_when`: 更新案例库或作品集截图时

- `反馈到 eval / incident review 的闭环方式`
  - `reason`: 反馈信号、人工复核记录和事故复盘如何进入 eval dataset，取决于真实产品数据链路
  - `refresh_when`: 做 Capstone A/B/C 的上线与运营方案时

## 处理规则

- 只刷新影响产品落地的业务规则和文案
- 不把固定阈值当稳定知识
- 不把某个行业的接管策略直接推广成通用结论
