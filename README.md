# Berg-Prompt

个人 Prompt 模板库，用 Git 管理，持续迭代。

## 目录结构

```
Berg-Prompt/
├── templates/                # 模板源文件（标准格式，含元数据）
│   ├── thinking/             # 思维类
│   ├── writing/              # 写作类
│   ├── coding/               # 编程类
│   └── analysis/             # 分析类
├── .claude/commands/         # Claude Code 可直接调用的版本
├── archived/                 # 已废弃版本
└── CHANGELOG.md              # 变更记录
```

## 模板索引

### 思维类 (thinking)

| 名称 | 命令 | 用途 |
|:-----|:-----|:-----|
| [专家视角](templates/thinking/expert.md) | `/expert [领域] [问题]` | 以领域顶尖专家视角思考问题 |
| [深度追问](templates/thinking/clarify.md) | `/clarify [问题/需求]` | 通过追问深度理解需求后再给方案 |
| [魔鬼代言人](templates/thinking/debate.md) | `/debate [观点]` | 让AI扮演反方学者挑战你的观点 |
| [失败预演](templates/thinking/premortem.md) | `/premortem [项目/想法]` | 假设项目失败，提前发现风险 |
| [逆向提示词](templates/thinking/reverse.md) | `/reverse [成品范例]` | 从成品范例逆向推导提示词 |
| [双版本解释](templates/thinking/explain.md) | `/explain [问题]` | 同时获得通俗和专业两个版本的解释 |
| [深度挖掘](templates/thinking/dig.md) | `/dig` | 通过AI持续追问，挖掘内心深处的想法 |

### 写作类 (writing)

*待添加*

### 编程类 (coding)

*待添加*

### 分析类 (analysis)

*待添加*

## 使用方式

### 在 Claude Code 中使用

```bash
# 直接调用
/expert LLM prompt管理
/expert 心理学 拖延症
```

### 手动复制使用

打开 `templates/` 下的对应文件，复制 `# Prompt` 部分内容。

## 贡献新模板

1. 在对应分类目录下创建 `.md` 文件
2. 使用标准格式（见下方）
3. 同步到 `.claude/commands/` 供 Claude Code 调用
4. 更新本 README 索引
5. 记录到 CHANGELOG.md

### 模板标准格式

```markdown
---
name: 模板名称
version: "1.0"
tags: [tag1, tag2]
author: Berg
created: 2026-01-17
updated: 2026-01-17
---

# 用途

简要说明这个 prompt 的用途。

# Prompt

[具体的 prompt 内容]

# 使用示例

[示例]

# 迭代记录

- v1.0 (2026-01-17): 初始版本
```
