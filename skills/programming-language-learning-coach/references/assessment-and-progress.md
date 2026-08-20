# 阶段测试与分语言进度

## 进度文件

长期课程且平台允许文件读写时，使用：

```text
.learning/programming-language-<language-slug>-progress.md
```

固定 slug：

- C：`c`
- Python：`python`
- C++：`cpp`
- Java：`java`
- Rust：`rust`
- C#：`csharp`
- JavaScript：`javascript`

当前主线语言对应：

```text
.learning/programming-language-c-progress.md
.learning/programming-language-python-progress.md
.learning/programming-language-cpp-progress.md
.learning/programming-language-java-progress.md
```

每门语言单独保存，不把多个语言的阶段结论写进同一文件。进度属于具体课程，不写进 Skill 安装目录。

## 恢复与兼容

1. 先从当前会话可用历史与摘要恢复证据。
2. 再读取当前语言的进度文件。
3. 若发现旧 `.learning/personal-learning-progress.md`，只迁移明确属于当前语言的记录；新文件不存在时复制并规范化，新旧同时存在时按日期和证据合并。
4. 保留旧文件作为备份，不移动、不删除。混合或无法判断的记录标为待确认，不猜测归属。
5. 会话与文件冲突时保留两边证据，以当前独立任务复核。

## 记录格式

```markdown
# Programming Language Learning Progress

- Language:
- Language version:
- Route: systems_and_resource | managed_static | dynamic_high_level
- Priority: first | second | extension
- IDE and version:
- Compiler / interpreter / runtime:
- Build and dependency tools:
- Course goal:
- Current stage: 1 | 2 | 3 | 4 | 5 | 6
- Current unit:
- Last updated:

## Stage coverage
- [核心能力]: not_started | introduced | practicing | independently_demonstrated | needs_review

## Prerequisites
- [前置知识]: verified | unknown | missing — [证据或检查方式]

## Demonstrated mastery
- [能力]: [独立实现、解释、调试、测试或迁移证据]

## Projects and artifacts
- [项目]: [功能、运行环境、测试、独立完成情况]

## Diagnosed failures
- [故障]: [复现、调用栈、根因、最小修复、回归测试]

## Incidental technical English
- [术语或阅读能力]: [出现语境、中文理解、后续独立识别证据]

## Confirmed error patterns
- [错误模式]: [可观察原因和防错检查]

## Hint history
- [任务]: [最高提示等级及是否需要独立复测]

## Stage-gate history
- [日期 / 阶段]: [覆盖、得分、核心项、提示、结论]

## Remediation plan
- [薄弱项]: [补讲、练习和复测条件]

## Next task
- [下一项完整任务]
```

只记录由独立实现、解释、编译或运行、调试、测试和迁移证明的掌握。失败、补弱和复测历史不得删除。

技术英语记录只用于低频复现和观察阅读进步，不建立独立阶段、不计入编程测试得分，也不能阻止编程晋级。

## 正式阶段测试

开始时一次发布完整任务、范围、环境、时限、资料规则、评分标准和交卷方式。学习者可以分批提交文件，但明确交卷前只确认收件、缺失文件和环境问题，不逐段批改或提供实质性提示。

晋级必须同时满足：

- 总分至少 80 分；
- 每项核心能力至少 70%；
- 至少一个未见迁移任务独立完成；
- 不存在未纠正的基础机制错误；
- 核心任务未依赖超过一级提示；
- 程序经过实际编译或运行和有效测试。

根据阶段调整题型，但不能为了晋级在测试后降低门槛。

## 各阶段考核

### 第一阶段

一个未见控制台需求、基础输入校验、核心语法解释和基础故障修复。不使用冷僻语法问答替代程序。

### 第二阶段

重构一个混乱或单文件程序，设计数据表示，拆分职责，补充错误处理和基本测试，并解释结构选择。

### 第三阶段

完成当前语言专属的状态追踪、结果预测、机制解释和因错误心智模型产生的缺陷修复。

### 第四阶段

接收带有真实故障的小项目，完成复现、调用栈、根因、最小修复和回归测试。接受实质性定位提示后必须换故障复测。

### 第五阶段

从干净环境构建包含多模块、依赖、测试、配置和持久化的中型项目，提交可复现步骤并解释关键配置。

### 第六阶段

验收真实项目、设计说明、测试、故障审查和一个未提前告知的维护任务。跟随教程完成、核心部分依赖逐步提示或只成功运行一次都不能通过。

## 未通过时

按需求理解、语言语义、程序结构、工具链、故障诊断、测试和工程化建立缺口表。只补真正薄弱的前提，安排少量针对练习和不同任务复测；保留原测试结果。

## 会话收尾

结束实质性学习回合时更新进度文件，并给学习者简短说明：本次证明了什么、仍不稳定什么、当前阶段、覆盖缺口和下一任务。平台不能写文件时输出可复制的同格式摘要，并说明尚未持久保存。
