# 数学学习进度记录

长期数学课程且平台允许文件读写时，将进度保存在当前学习项目的：

```text
.learning/mathematics-learning-progress.md
```

不要把进度文件写进 Skill 安装目录。Skill 是可复用规则，进度属于具体课程或会话。

## 恢复与旧记录迁移

按以下顺序恢复：

1. 当前会话可用历史与摘要中的可验证学习证据；
2. `.learning/mathematics-learning-progress.md`；
3. 旧 `.learning/personal-learning-progress.md`。

旧文件内容明确属于数学课程时：

- 新文件不存在：把有效记录复制并规范化到新格式，保留旧文件作为备份，不移动、不删除。
- 新旧文件同时存在：按记录日期、独立作答证据和当前表现合并；保留仍有效的失败、补弱和复测历史。
- 旧文件混有其他学科内容：只迁移能够明确归属数学课程的记录，无法判断的内容标为待确认，不猜测归属。
- 只有会话历史而没有进度文件：根据当前可用历史建立新文件，并把无法验证的陈述标为 `unknown`。

会话历史与文件冲突时不静默覆盖，以当前独立作答验证。平台不能读写文件时，在会话结束时给出可复制的同格式摘要，并说明尚未持久保存。

## 记录格式

```markdown
# Mathematics Learning Progress

- Subject:
- Course goal:
- Textbook or syllabus:
- Target examination or competition:
- Current primary stage: 1 | 2 | 3 | 4 | 5
- Current unit:
- Last updated:

## Stage map
- Stage 1 scope:
- Stage 2 scope:
- Stage 3 scope:
- Stage 4 scope:
- Stage 5 scope:

## Current stage coverage
- [核心模块]: not_started | learning | independently_demonstrated

## Prerequisite status
- [前置知识]: verified | unknown | missing — [证据或待确认方式]

## Prerequisite remediation
- [前置知识]: [补讲范围、检查结果、返回主线的位置]

## Demonstrated mastery
- [知识点]: [独立解释、计算、推导、证明或迁移证据]

## In progress
- [知识点]: [当前缺口或所需提示级别]

## Confirmed error patterns
- [错误类型]: [学习者确认的原因和防错检查]

## Methods already used
- [方法]: [成立条件、适用范围与掌握程度]

## Stage-gate history
- [日期 / 阶段]: [总分、各模块结果、提示使用、结论]

## Remediation plan
- [薄弱模块]: [补讲、针对练习、复测条件]

## Next task
- [平时训练：下一道复杂题、下一组基础题或下一学习目标；正式晋级测试：整份试卷及交卷状态]
```

## 更新纪律

- 只记录由独立作答、解释、推导、证明、验证或迁移题证明的掌握，不记录空泛的“已了解”。
- 记录新知识实际依赖的前置知识及状态；“讲过”“看过”或学习者自称会用不能直接记为 `verified`。
- 学习者指出未学过某项前置知识时，将原假设改为 `missing`，记录补讲、检查结果和返回主线的位置。
- 错因必须来自学习者说明或可观察步骤，不猜测心理原因。
- 平时训练保存下一道复杂题或下一组基础题的完整目标，不提前写答案或提示。
- 正式晋级测试开始前保存整份试卷、覆盖表、时限、资料规则和评分标准。
- 分批收到答卷时只记录已收题号、缺页或无法辨认处；明确交卷前不写逐题得分、答案或补弱提示。
- 阶段测试保存覆盖表、评分证据和独立完成情况，不能只写“通过”或“未通过”。
- 阶段未通过时保留原结果，记录补弱和复测，不删除失败记录制造连续进步。
- 每次只做小幅更新，保留仍有效的历史信息。
