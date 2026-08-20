# Learning Coach Skills

三个面向长期系统学习的中文 Agent Skills，分别覆盖数学、编程语言和计算机专业课。它们强调严格判断、循序推进、真实验证和可续接的学习记录，不以学习时长或主观自评代替掌握证据。

## 包含的 Skills

| Skill | 适用范围 | 显式调用 |
| --- | --- | --- |
| Mathematics Learning Coach | 高等数学、线性代数、概率统计、离散数学 | `$mathematics-learning-coach` |
| Programming Language Learning Coach | C、Python、C++、Java、Rust、C#、JavaScript | `$programming-language-learning-coach` |
| Computer Science Learning Coach | 数据结构、计算机组成原理、操作系统、计算机网络、数据库、408 综合复习 | `$computer-science-learning-coach` |

三个 Skill 各自维护课程阶段、练习协议、阶段测试和进度记录，边界清晰：

- 数学 Skill 处理定义、推导、证明、计算和数学考试复习。
- 编程语言 Skill 处理语法、运行机制、代码批改、调试和工程实践。
- 计算机专业课 Skill 处理数据结构与计算机系统课程，并提供自然的网络安全迁移路线。

## 仓库结构

```text
skills/
|-- mathematics-learning-coach/
|   |-- SKILL.md
|   |-- agents/openai.yaml
|   `-- references/
|-- programming-language-learning-coach/
|   |-- SKILL.md
|   |-- agents/openai.yaml
|   `-- references/
`-- computer-science-learning-coach/
    |-- SKILL.md
    |-- agents/openai.yaml
    `-- references/
```

每个目录都是独立 Skill。`SKILL.md` 包含名称、触发范围和核心指令，`references/` 保存按需读取的详细教学协议，`agents/openai.yaml` 提供界面元数据。

## 安装到 Codex

Codex 当前会从用户级 `$HOME/.agents/skills` 和仓库级 `.agents/skills` 等位置发现本地 Skill。选择一种方式安装即可。

### 用户级安装

克隆仓库后，把 `skills` 下的三个完整目录复制到：

```text
$HOME/.agents/skills/
```

Windows PowerShell 示例：

```powershell
git clone https://github.com/zylzjy38-YY/personal-learning-coach-skill.git
New-Item -ItemType Directory -Force "$HOME/.agents/skills" | Out-Null
Copy-Item -Recurse -Force "personal-learning-coach-skill/skills/*" "$HOME/.agents/skills/"
```

### 仓库级安装

如只希望某个项目使用这些 Skill，把所需目录复制到项目的：

```text
.agents/skills/
```

Codex 通常会自动检测 Skill 变化；如果没有出现，重启 Codex。

## 使用示例

```text
使用 $mathematics-learning-coach，先诊断我的高等数学水平，再继续当前课程。
```

```text
使用 $programming-language-learning-coach，带我从零系统学习 C 语言。
```

```text
使用 $computer-science-learning-coach，为我建立数据结构与 408 的学习路线。
```

Skill 也可以在请求与其 `description` 匹配时被隐式调用。显式调用更适合第一次使用或需要明确指定教学教练的场景。

## 进度与数据

这些 Skill 只包含教学协议和空白进度模板，不包含个人学习记录。实际进度由使用者在自己的学习项目中保存，不应提交到本仓库。

## 兼容性说明

本仓库提供可直接阅读和复制的 Skill 源码。GitHub 公开仓库不等于已发布到 OpenAI 插件目录；如果要让其他用户通过插件目录一键安装，还需要按插件规范另行打包和发布。

## 许可证

[MIT License](LICENSE)
