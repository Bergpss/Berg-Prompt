# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

Berg-Prompt 是一个个人 Prompt 模板库，用 Git 管理和迭代。模板按用途分类（thinking/writing/coding/analysis），每个模板有两个版本：
- `templates/` - 标准格式源文件，包含元数据、用途说明、使用示例
- `.claude/commands/` - Claude Code 可直接调用的精简版本

## 架构

模板采用双文件结构：

1. **源文件** (`templates/<category>/<name>.md`)：包含完整元数据（YAML frontmatter）、用途说明、prompt 正文、使用示例、迭代记录
2. **命令文件** (`.claude/commands/<name>.md`)：仅包含 argument-hint、description 和可执行的 prompt，末尾标注源文件路径

变量占位符：
- 源文件使用 `{{变量名}}` 格式
- 命令文件使用 `$1`, `$2` 格式（Claude Code 参数语法）

## 添加新模板流程

1. 在 `templates/<category>/` 下创建标准格式 `.md` 文件
2. 在 `.claude/commands/` 下创建对应的命令版本（转换占位符格式）
3. 更新 `README.md` 模板索引表
4. 记录变更到 `CHANGELOG.md`

## 模板元数据格式

```yaml
---
name: 模板名称
version: "1.0"
tags: [tag1, tag2]
author: Berg
source: URL（如有原始来源）
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

## Git Commit Message 格式

使用 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```
<type>: <description>
```

常用 type：
- `feat` - 新增模板或功能
- `fix` - 修复错误
- `docs` - 更新文档（README、CHANGELOG）
- `refactor` - 重构模板内容（不改变用途）
- `chore` - 项目配置、维护

示例：
```
feat: add clarify template
docs: update README index
fix: correct variable placeholder in expert template
```
