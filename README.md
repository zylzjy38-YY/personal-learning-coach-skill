# Personal Learning Coach Skill

一个可移植的个人学习教练 Skill，源自长期重积分学习中形成的教学约定，并扩展到高等数学、离散数学、计算机专业课、C、Python 和 Java。

它不替模型增加新的学科知识，也不会训练或微调模型。它提供的是一套可重复执行的教学协议：先读取学习上下文，尊重学习者的真实方法，定位第一处错误，沿原思路修正，按证据评分，必要时比较第二种方法，然后自动推进下一题。

## 工作原理

兼容 Agent Skills 的平台通常分三层加载：

1. 平台始终索引 `SKILL.md` 顶部的 `name` 和 `description`。
2. 当用户请求与描述匹配，或显式调用 `$personal-learning-coach` 时，平台把 `SKILL.md` 正文加入当前模型上下文。
3. Skill 正文再按任务选择性读取 `references/`，例如数学题只加载数学规则。

因此 Skill 更接近“按需加载的操作手册”，不是插件代码，也不是新的 AI 模型。实际触发方式、工具权限和指令优先级由所在平台决定；它不能覆盖平台安全规则或系统级指令。

## 仓库结构

```text
skills/personal-learning-coach/
|-- SKILL.md
|-- agents/openai.yaml
`-- references/
    |-- mathematics.md
    |-- programming-and-cs.md
    `-- progress-record.md
```

## 安装

### OpenAI Codex

把 `skills/personal-learning-coach` 目录复制到：

```text
~/.codex/skills/personal-learning-coach
```

Windows 默认对应：

```text
C:\Users\<用户名>\.codex\skills\personal-learning-coach
```

重新开始下一轮对话后，Codex 会重新发现该 Skill。

### 其他 Agent Skills 平台

把完整的 `personal-learning-coach` 文件夹放入该平台声明的 Skills 目录。不同平台的目录和显式调用语法可能不同，但核心 `SKILL.md` 与 `references/` 不依赖特定工具。

## 使用示例

```text
使用 $personal-learning-coach，继续我的重积分学习。先根据进度判断下一题，不要直接给提示。
```

```text
请按 $personal-learning-coach 批改这张手写答案。先复述我的方法，再指出第一处错误。
```

```text
用 $personal-learning-coach 带我学习 Java 集合。一次一题，代码必须实际编译验证。
```

## 跨会话进度

Skill 本身不会自动拥有长期记忆。平台允许读写文件时，它使用当前学习项目下的 `.learning/personal-learning-progress.md` 保存进度；无文件权限的平台只能依赖当前对话或由用户重新提供进度摘要。

## 许可证

MIT License。可以在个人项目和支持 Agent Skills 的平台中复制、修改和再发布。
