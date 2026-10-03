# AgentMail → Claude 注册技能

一个可复用的 Codex 技能：在用户授权下创建一个 AgentMail 邮箱，并完成 Claude 个人免费账号注册、邮件验证及入门设置，在涉及重要选择时取得用户确认。

流程：连接 AgentMail → 创建并核验邮箱 → Claude 邮箱验证 → 年龄与条款确认 → 免费套餐和入门设置 → 验证登录完成。

适用于用户本人授权的单个账号，不包含批量注册、绕过验证或真实账号数据。

## 文件说明

- [SKILL.md](skills/agentmail-claude-signup/SKILL.md)：执行流程和授权边界
- [中断恢复指南](skills/agentmail-claude-signup/references/recovery.md)：避免重复创建账号，安全恢复流程
- [离线测试场景](skills/agentmail-claude-signup/references/dry-runs.md)：无需真实注册的判断测试
- `agents/openai.yaml`：技能在界面中的展示信息

## 使用方法

将 `skills/agentmail-claude-signup` 文件夹复制到你的 Codex 客户端支持的技能目录，保留文件夹名称和内部结构。安装方式以当前[官方技能文档](https://developers.openai.com/codex/skills)为准。本仓库不会自动安装任何内容。

调用示例：

> 使用 $agentmail-claude-signup 为我创建一个 AgentMail 邮箱，并协助注册 Claude 免费账号。需要权限、年龄确认或同意当前条款时，请先问我。

运行环境需要可用的 AgentMail 连接和浏览器操作能力。工具名称、OAuth 授权方式及网页界面可能变化，应检查当前工具参数和官方网站，不能机械重放固定选择器。过去成功的操作顺序不保证今后仍可用，也不保证服务会接受某一邮箱提供商。

## 安全与隐私

技能本身不授予任何权限。用户承担账号责任，并持续掌握邮箱访问权。OAuth、年龄声明、条款接受、验证码、隐私选项及新增要求，都必须遵守用户授权和运行环境中更严格的规则。密码只能通过安全的用户输入流程处理。本技能不包括付费升级、批量创建账号或自主对外发信。

所有账号示例均为虚构。请勿提交真实邮箱地址、验证链接、验证码、凭据、浏览器状态、私人账号截图、聊天记录或私有操作记录。修改后使用离线场景验证，不要用真实注册来测试文档。

本项目独立维护，与 AgentMail、Anthropic 或 OpenAI 无隶属或官方背书关系。产品名称仅用于指明相关服务，服务条款和资格要求仍然适用。

## 开源许可

仓库中的原创文档和展示信息采用 [MIT 许可证](LICENSE)。许可证保留英文原文，不涵盖第三方服务、品牌标识或服务条款。
