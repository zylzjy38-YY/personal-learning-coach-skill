# 课程进度与 408 汇总

## 保存位置

进度属于具体学习项目，不得写入 Skill 安装目录。平台允许文件读写时，保存在当前项目的 `.learning/`：

```text
.learning/data-structures-progress.md
.learning/computer-organization-progress.md
.learning/operating-systems-progress.md
.learning/computer-networks-progress.md
.learning/databases-progress.md
.learning/408-integrated-progress.md
```

课程名称无法安全映射时使用简短小写连字符标识，并在文件内保留原课程名。不同课程不得复用同一文件。

平台不能持久写入时，在实质性学习会话结束输出同结构的可复制摘要，并说明尚未保存。不要把自评或“讲过”当作已验证掌握。

## 单科记录格式

```markdown
# Learning Progress

- Subject:
- Course goal:
- Materials and version:
- Target exam and year:
- Environment:
- Current primary stage: 1 | 2 | 3 | 4 | 5
- Current unit:
- Last updated:

## Stage map
- Stage 1 scope and evidence:
- Stage 2 scope and evidence:
- Stage 3 scope and evidence:
- Stage 4 scope and evidence:
- Stage 5 scope and evidence:

## Module coverage
- [module]: not_started | learning | assisted | independently_demonstrated | retention_gap

## Prerequisite status
- [prerequisite]: verified | unknown | missing — [evidence or check]

## Demonstrated mastery
- [knowledge or ability]: [independent evidence, date]

## In progress
- [knowledge or ability]: [gap or prompt level]

## Practice evidence
- [task]: [environment, prediction, result, verification, remaining gap]

## Active technical English
- [term]: [current contextual meaning] — [where encountered; evidence or next natural reuse]

## Confirmed error patterns
- [type]: [observable evidence or learner explanation; prevention check]

## Stage-gate history
- [date / stage]: [scope, score, module results, hints, time, practice evidence, decision]

## Retention checks
- [date / prior stage]: [integrated task, result, action]

## Remediation plan
- [gap]: [minimal reteaching, practice, retest condition]

## Next task
- [one complete next task or formal-exam state]
```

## 更新纪律

- 只记录独立解释、作答、实现、实验、验证和迁移证明的掌握。
- “听懂”“看过”或自称会用只能记为学习经历，不能写成 `independently_demonstrated`。
- 新知识实际依赖的前置知识必须记录状态；用户指出未学过时把原假设改为 `missing`，记录补讲和返回主线位置。
- 错因只能来自可观察步骤或用户说明，不猜测心理原因。
- 实践记录包含目标、环境、预测、实际结果和有效验证；环境失败单独记录。
- `Active technical English` 只保留仍需在真实任务中自然复现的少量术语。能够在代码、报错、工具或文档中正确理解和使用后移出活跃区，不建立永久增长的背词表。
- 技术英语不单独计入阶段晋级分数，也不因孤立单词记忆阻止专业课晋级；只记录它是否影响了当前真实技术任务。
- 正式考试开始前保存范围、覆盖表、试卷、时限、资料规则和评分标准；交卷前只记录收卷状态，不记录逐题正确性、答案或补弱提示。
- 阶段未通过时保留原结果，追加补弱和复测，不删除失败历史。
- 旧知识暴露遗忘时标记 `retention_gap`；修复后追加证据，不改写过去已经发生的晋级事实。
- 每次只做必要的小幅更新，保留仍有效历史。

## 会话恢复

优先读取进度文件，再结合当前对话判断下一任务。文件缺失、损坏或与对话冲突时：

1. 只恢复能够从现有证据确认的内容；
2. 标记不确定项，不补造学习经历；
3. 使用短诊断验证关键前提；
4. 说明恢复后的主阶段、缺口和依据。

## 408 单科摘要

单科阶段末生成以下可移植摘要，供 408 综合对话导入：

```markdown
# 408 Subject Evidence Capsule

- Subject:
- Scope and material version:
- Current stage:
- Last verified date:
- Stage-gate scores and conditions:
- Core modules independently demonstrated:
- Unresolved gaps:
- Retention status:
- Timed performance:
- Practice and transfer evidence:
- Suggested next integrated checks:
```

综合对话必须检查四门摘要是否齐全、范围是否匹配、证据是否独立以及日期是否过旧。数据库摘要不得加入 408 四科总分。综合对话使用相同原则记录完整模拟、分科得分、时间分配、错因趋势和补弱安排。
