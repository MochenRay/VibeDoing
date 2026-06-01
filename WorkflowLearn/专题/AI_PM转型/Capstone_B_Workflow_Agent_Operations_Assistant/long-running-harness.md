# Long-running Harness

> 最近确认时间：2026-04-16

## 目标

支持一类可能跨多步骤、跨系统、跨等待状态的运营工单流程，而不是一次性回答。

## 结构

### Initializer

- 读取工单
- 识别任务类型
- 建立初始 state

### Session Startup

- 载入工具
- 载入权限范围
- 载入当前工单上下文

### Incremental Loop

1. 判断下一步
2. 调工具
3. 更新 state
4. 记录 artifact
5. 判断是否继续、暂停或 handoff

### Failure Handling

- 临时失败：可重试
- 权限失败：打回人工
- 证据不足：收窄输出
- 高风险：停机并升级

### Cleanup

- 写入最终 artifact
- 更新工单状态
- 记录下轮待处理项
