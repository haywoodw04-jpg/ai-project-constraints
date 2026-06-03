# 项目说明

## 一、项目名称

ai-project-constraints

## 二、项目类型

工程约束模板仓库 / AI 编码规范文档仓库。

本仓库用于在新项目初次启动时拉取一套可落地的 AI 协作约束文件，防止后续 AI 编码出现命名混乱、接口不统一、数据库乱改、安全漏洞、状态机失控、重复代码和过度设计。

## 三、项目目标

- 提供一套可复制到任意项目根目录的 AI 编码约束框架。
- 约束 AI 在编码前先读项目事实、接口契约、数据库契约、状态机、安全、UI、命名和测试规则。
- 让每个下游项目在开发前明确修改计划、风险、测试命令和回滚方式。

## 四、当前技术栈

- 文档格式：Markdown
- 版本管理：Git
- 前端框架：无
- 后端框架：无
- 数据库：无
- ORM：无
- 鉴权方式：无
- UI 框架：无
- 包管理器：无
- 测试工具：待人工确认
- 构建命令：无

## 五、主要目录结构

```txt
/
├─ AGENTS.md
├─ PROJECT.md
├─ PROJECT_MEMORY.md
└─ docs/
   ├─ contracts/
   │  ├─ API_CONTRACT.md
   │  ├─ DB_CONTRACT.md
   │  ├─ STATE_MACHINE.md
   │  ├─ SECURITY_RULES.md
   │  ├─ UI_RULES.md
   │  ├─ NAMING_RULES.md
   │  ├─ TESTING_RULES.md
   │  └─ TASK_TEMPLATE.md
   └─ ai-coding/
      ├─ CODEX_WORKFLOW.md
      ├─ REVIEW_CHECKLIST.md
      └─ PROJECT_BOOTSTRAP_TEMPLATE.md
```

## 六、核心业务模块

- AI 编码总规则：`AGENTS.md`
- 项目事实说明：`PROJECT.md`
- 接口、数据库、状态机、安全、UI、命名、测试契约：`docs/contracts/`
- Codex 工作流、人工审查清单、新项目初始化提示词：`docs/ai-coding/`

## 七、当前已经实现的功能

- 首版规范文件结构。
- 通用 AI 编码总规则。
- 下游项目可复制使用的 task 模板。
- 下游项目初始化时可引用的 bootstrap 提示词。
- 对 API、数据库、状态机、UI 等当前仓库不存在的能力均标记为模板或待人工确认。

## 八、当前计划实现的功能

- 根据真实下游项目继续补充不同技术栈的示例版本：待人工确认。
- 增加文档一致性检查脚本：待人工确认。
- 增加一键复制到目标项目的脚本：待人工确认。

## 九、高风险模块

- `AGENTS.md`：会影响所有 AI Agent 的默认行为。
- `docs/contracts/API_CONTRACT.md`：会影响接口返回和前后端协作。
- `docs/contracts/DB_CONTRACT.md`：会影响数据库变更规则。
- `docs/contracts/STATE_MACHINE.md`：会影响订单、支付、任务等状态流转。
- `docs/contracts/SECURITY_RULES.md`：会影响权限、支付、用户数据和日志安全。

## 十、不允许 AI 随意改动的模块

- 不得无任务单直接改 `AGENTS.md`。
- 不得为了某个单一业务项目把本仓库模板改成只适配该项目。
- 不得删除 contract 文件或弱化高风险操作确认规则。
- 不得在模板中写入真实密钥、真实账号、真实支付配置或真实用户数据。

## 十一、常用开发命令

```powershell
git status --short
rg --files
```

## 十二、常用构建命令

当前仓库是 Markdown 文档仓库，无构建命令。

## 十三、常用测试命令

```powershell
git status --short
rg --files docs AGENTS.md PROJECT.md
```

Markdown 链接检查工具：待人工确认。

## 十四、部署注意事项

- 本仓库不部署服务。
- 发布到远端前必须确认没有真实密钥、Token、账号、密码、支付配置或用户数据。
- `git push` 属于高风险 Git 操作，必须由用户明确确认后执行。

## 十五、环境变量说明

当前仓库不需要环境变量。

下游项目如果需要环境变量，必须在下游项目的 `PROJECT.md` 中列出变量名、用途、是否必填、示例格式和禁止明文提交规则。

