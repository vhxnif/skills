# OpenCode Skills

OpenCode Agent 技能仓库，存储可被 Agent 动态加载的技能模块。

## 目录结构

```
.
├── README.md
└── readlink/           # 技能目录
    ├── SKILL.md        # 技能说明（必须）
    └── *.lua           # 技能所需的脚本文件
```

每个技能是一个独立目录，包含一个 `SKILL.md` 文件和相关的资源文件。

## 已有技能

| 技能名称 | 描述 |
|---------|------|
| [readlink](./readlink/SKILL.md) | 读取 URL 内容并转换为干净的 markdown 格式 |

## 添加新技能

1. 在仓库根目录创建新文件夹，以技能名称命名（小写，使用连字符分隔）
2. 在文件夹中创建 `SKILL.md`，包含以下前置元数据：

```markdown
---
name: skill-name
description: 技能的简短描述
---

# Skill Name

[技能的详细说明和使用方法]
```

3. 添加技能所需的其他文件（脚本、配置等）

## 前置要求

使用本仓库的技能前，请确保已安装所需工具：

- **readlink**: 需要 `pandoc` 和 `curl`

安装 pandoc：
```bash
# macOS
brew install pandoc

# Ubuntu/Debian
sudo apt install pandoc

# Windows
choco install pandoc
```