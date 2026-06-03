# 新项目约束框架初始化提示词模板

把以下提示词复制给 Codex，用于在新项目中初始化或更新 AI 工程约束框架。

```md
你现在要初始化一个新项目的工程约束框架。

请先阅读本项目中的：

- AGENTS.md
- PROJECT.md
- docs/contracts/API_CONTRACT.md
- docs/contracts/DB_CONTRACT.md
- docs/contracts/STATE_MACHINE.md
- docs/contracts/SECURITY_RULES.md
- docs/contracts/UI_RULES.md
- docs/contracts/NAMING_RULES.md
- docs/contracts/TESTING_RULES.md
- docs/contracts/TASK_TEMPLATE.md

然后结合当前新项目的技术栈和业务目标，创建或更新对应规范文件。

要求：

1. 不要直接写业务代码。
2. 不要引入依赖。
3. 不要修改数据库。
4. 只创建项目规范文件。
5. 每个规范文件必须简洁、可执行、可检查。
6. 不确定的信息标记为“待人工确认”。
7. 已有规范不得粗暴覆盖。
8. 输出最终创建/修改的文件列表。
```

## 使用建议

1. 先把本仓库的 `AGENTS.md`、`PROJECT.md` 和 `docs/` 复制到新项目根目录。
2. 再让 Codex 按上方提示词扫描新项目真实结构。
3. 让 Codex 把模板中的通用规则落地为该项目的真实规则。
4. 不确定的技术栈、命令、接口、数据库、状态机必须保留 `待人工确认`，不要编造。

