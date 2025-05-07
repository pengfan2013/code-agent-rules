# 核心能力

背景说明: 除开说明规则导入, 以及中文回复等之外其它需要用来辅助复杂编码任务, 需要具备的设置

## 工作流矫正

两个主要方向
- 丰富Agent本身不完善的主工作流
- 丰富子工作流

工作流可能包含以下这些步骤
- Research 问题理解：首先探索代码库结构
- Decomposition 基本都是使用sequential_thinking来分解复杂问题
- Impact Analysis 分析影响
- Plan 计划
- Implementation 执行
- Verification/Review 验证
- 集成评估：使用多数投票选择最佳解决方案
- 多样本生成：为每个问题生成多个候选解决方案
- 集成评估：使用多数投票选择最佳解决方案

## 额外功能辅助

- Chat History记录生成: 定制粒度的历史沟通记录生成
- Task Management/CheckList 任务管理

## 规则列表

### 01 RIPER-5 模式

cursor社区热门

### 02 Task Management 模式

- Sequential Thinking
- Task Management
- Context7 for docs and code examples
- Bright Data for Search and browsing as a real user.
- Test Driven Development
- Security checks
- Legal Complliance

### 03 Augster

**Core Capabilities:**

- **结构化工作流程：** 复杂任务遵循强制性的 ## 1-9 工作流程（分解、影响分析、实现、验证等）。
- **用户输入评估：** 具有逻辑功能(Evaluate_User_Input)来分析任务执行期间收到的用户消息，区分微小调整和需要完全重新规划的输入（触发CoT再次执行）。对于模糊情况使用特定查询(REPLAN_CONFIRMATION_REQUEST)。
- **自主错误处理：** 在 ## 6 中包含详细的程序指导，用于处理实现过程中的工具/代码错误：分析失败原因，尝试直接纠正/重试，评估持续性，考虑变通方法，并系统性地升级/HALT。
- **上下文连续性协议：** 为内部不确定性或上下文衰减而设计；触发自检，包括 ## 1 计划回顾并输出摘要(CONTINUITY_CHECK_SUMMARY)以加强上下文，覆盖默认的"询问继续"行为。
- **影响分析与验证：** 要求分析变更影响（## 2，包括调用者依赖关系）并使用全面的 ## 8 检查清单，验证计划完成、状态管理、协议使用、错误处理遵守、调用者更新和清理。支持部分完成和继续循环。
- **编码原则遵守：** 强制执行原则，如适当复杂性（在YAGNI/KISS与需求之间平衡），主动清理和DRY。捕获超出最小复杂性的想法，用于可选的 ## 9 建议部分。
- **生态系统工具检测：** 包括逻辑（## 4）以识别项目工具。