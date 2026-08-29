# handoff — 对话换窗交接

面向「非专业程序员 + Vibe Coding」人群的会话窗口切换与管理工具。把换窗从十几步手工操作变成一句话 `/handoff`：**信息不丢、思维连续、过程简单**。

## 这是什么

长对话会越聊越慢、越来越"忘事"（上下文漂移、响应变慢、早期指令被稀释）。想换新窗口继续，但交接要自己写清"做到哪、为什么这么做、下一步干嘛"——这正是非程序员最难承担、也最容易中断的一步。

`/handoff` 自动完成交接：

- **旧窗口**：一句话生成交接文档（项目现状、关键决策、下一步、协作偏好）
- **新窗口**：一句话接上所有思路与进度
- **跨设备 / 跨 AI 工具**：无缝续接，信息不丢、思维连续

## 安装

```bash
# 把 skill 放进 Claude Code 技能目录
mkdir -p ~/.claude/skills/handoff
cp -R SKILL.md templates/ ~/.claude/skills/handoff/
```

重启 Claude Code 后，输入 `/handoff` 即可使用。

## 使用

| 场景 | 操作 |
|------|------|
| 换窗续接 | 旧窗口 `/handoff` 生成交接文档 → 新窗口 `/handoff` 自动接手 |
| 里程碑存档 | 进行中输入 `/handoff`，更新交接文档 |
| 跨设备 / 跨工具 | 交接文档随项目进 git，任何工具、任何设备可接手 |

## 目录结构

```
handoff-skill/
├── SKILL.md          # skill 主指令
├── templates/        # 交接文档模板 / 项目规则模板
├── releases/         # 各版本发布快照
└── DESCRIPTION.md    # 对外描述
```

## 协议

[MIT](LICENSE)
