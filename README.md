# plain-coding-talk · 写代码时说人话

让 AI 在写代码、调试、评审和汇报结果时，使用简短直白的中文，减少包装词、费解比喻和空话。

例如，把“质量门禁全绿，修复编队交回”写成“两个任务已完成，已运行的测试全部通过”。内容必须符合实际结果。

## 做什么

- 直接说明改了什么、为什么、检查结果及未完成事项。
- 不给普通工作起“根网”“地基缝”等名称，也不换一套新词继续包装。
- 准确使用必要技术术语，需要时用一句白话解释。
- 不奉承、自夸、重复预告或强行凑格式。
- 不为了简短而省略必要工作、错误或尚未验证的事项。

## 安装

下载并解压本仓库，保留文件结构，把整个 `plain-coding-talk` 文件夹放入对应工具的个人技能目录。

| 工具 | 安装后的主文件 |
| --- | --- |
| Codex | `~/.agents/skills/plain-coding-talk/SKILL.md` |
| Claude Code | `~/.claude/skills/plain-coding-talk/SKILL.md` |

重新开始会话后，可在 Codex 中使用 `$plain-coding-talk`，在 Claude Code 中使用 `/plain-coding-talk`。

要在代码任务中默认使用，在自己的个人指令文件里加入：

```text
代码工作默认用简短直白的中文。开始任务时读取并遵守 plain-coding-talk 的 SKILL.md；本会话已读且未更新就沿用。简短不能省略必要工作和说明。
```

Codex 的个人指令文件是 `~/.codex/AGENTS.md`，Claude Code 是 `~/.claude/CLAUDE.md`。建议把上面技能名替换为本机安装后的主文件路径；保留指令文件里原有的其他内容。

其他工具需要自行加载这些指令，安装到一个工具不会让所有 AI 自动遵守。

## 文件

```text
plain-coding-talk/
├── README.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── wording.md
```

规则见 [SKILL.md](SKILL.md)。完整词表见 [references/wording.md](references/wording.md)，只在需要核对具体用词时查看相关部分。

安装与加载方式参考 [Codex 官方文档](https://developers.openai.com/codex/skills/)和 [Claude Code 官方文档](https://code.claude.com/docs/en/skills)。
