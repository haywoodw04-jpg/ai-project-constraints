# 命名规则

本文件约束文件、目录、变量、函数、接口、数据库字段和常见业务字段命名。下游项目如已有成熟规范，应在保留有效内容的前提下增量合并。

## 一、文件命名规范

- Markdown 规范文件使用大写英文和下划线，例如 `API_CONTRACT.md`。
- Python 文件使用小写英文和下划线，例如 `order_service.py`。
- Web 组件文件命名由项目框架决定，必须在下游项目确认。
- 禁止同一目录中混用表达同一含义的文件名，例如 `order.ts`、`order_api.ts`、`orderService.ts` 无区分说明。

## 二、目录命名规范

- 目录名必须表达职责，不用含糊名称如 `common2`、`new_utils`、`temp`。
- 合同文档放在 `docs/contracts/`。
- AI 协作流程文档放在 `docs/ai-coding/`。
- 下游项目的源码目录按项目技术栈确认，不在本仓库编造。

## 三、变量命名规范

- 变量名必须表达业务含义。
- 布尔值推荐使用 `is`、`has`、`can`、`should` 开头。
- 列表变量使用复数或明确集合含义。
- 禁止使用 `data1`、`obj2`、`tmpResult` 长期存在于业务代码。

## 四、函数命名规范

- 函数名使用动词开头，表达动作和结果。
- 查询函数使用 `get`、`list`、`find` 等固定前缀。
- 创建、更新、删除函数使用 `create`、`update`、`delete` 或项目统一词。
- 禁止同一动作混用 `handle`、`process`、`do` 而不说明差异。

## 五、组件命名规范

- UI 组件命名必须表达用途和层级。
- 页面级组件、业务组件、基础组件不得混放同名。
- 当前仓库无 UI 组件，规则由下游项目补充。

## 六、API 路由命名规范

- 路由资源名必须稳定，优先使用业务资源名。
- 管理端和用户端路由必须区分。
- 禁止为了临时功能新增语义不清的 endpoint。
- 当前仓库无 API，路由规则由下游项目补充。

## 七、数据库表命名规范

- 表命名风格必须全项目统一。
- 业务表、日志表、关联表必须有清晰命名。
- 当前仓库无数据库，表命名由下游项目补充。

## 八、数据库字段命名规范

- 字段命名必须与统一命名表一致。
- 时间、金额、用户 ID、订单号、状态字段不得混用。
- 当前仓库无数据库，字段命名由下游项目补充。

## 九、枚举命名规范

- 枚举值必须稳定，不得随文案变化。
- 状态枚举必须与 `STATE_MACHINE.md` 一致。
- 枚举值推荐使用大写英文和下划线，例如 `PAYMENT_SUCCESS`。

## 十、常量命名规范

- 全局常量使用大写英文和下划线。
- 配置 key 使用项目已有风格，不得为单个功能新建另一套风格。
- 禁止把可配置业务值写死为散落常量。

## 十一、时间字段命名规范

- 创建时间：`createdAt`
- 更新时间：`updatedAt`
- 删除时间：`deletedAt`
- 支付时间：`paidAt`
- 发货时间：`deliveredAt`
- 过期时间：`expiredAt`

如果项目使用 snake_case，必须整体转换为 `created_at` 等同一风格，不能混用。

## 十二、金额字段命名规范

- 订单金额：`orderAmount`
- 支付金额：`paidAmount`
- 退款金额：`refundAmount`
- 余额：`balance`
- 单价：`unitPrice`
- 总价：`totalPrice`

金额单位必须在字段说明中明确。

## 十三、统一命名表

| 业务含义 | 统一命名 | 禁止混用 |
|---|---|---|
| 手机号 | phone | mobile, tel, phoneNumber |
| 邮箱 | email | mail, emailAddress |
| 用户 ID | userId | uid, user_id 混用 |
| 管理员 ID | adminId | managerId, operatorId 混用 |
| 订单 ID | orderId | oid |
| 订单号 | orderNo | orderNumber, orderCode |
| 支付 ID | paymentId | payId |
| 支付单号 | paymentNo | payNo, transactionNo 混用 |
| 状态 | status | state 混用但不说明区别 |
| 页码 | page | current, pageNo 混用 |
| 每页数量 | pageSize | limit, size 混用 |
| 创建时间 | createdAt | created_at 混用 |
| 更新时间 | updatedAt | updated_at 混用 |
| 金额 | amount | price, money 混用但不定义单位 |
| 订单金额 | orderAmount | amount, price 混用 |
| 支付金额 | paidAmount | payAmount, paymentAmount 混用 |
| 退款金额 | refundAmount | refundMoney |
| 库存 | stock | inventory 混用 |
| 积分 | points | score, credits 混用 |
| 余额 | balance | wallet, money 混用 |

## 十四、禁止事项

- 禁止 `phone` / `mobile` / `tel` 混用。
- 禁止 `userId` / `uid` 混用。
- 禁止 `orderNo` / `orderId` / `orderNumber` 混用且不说明差异。
- 禁止 `status` / `state` 混用但不说明区别。
- 禁止 `created_at` / `createdAt` 混用。
- 禁止 `pageSize` / `limit` 混用。
- 禁止 `amount` / `price` / `money` 混用但不定义单位。

