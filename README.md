# AgentMail → Claude Signup Skill

A reusable Codex skill for creating one user-authorized AgentMail inbox and completing Claude personal free-account signup with email verification and human approval at consequential steps.

中文：把「连接 AgentMail → 创建并核验邮箱 → Claude 邮箱验证 → 年龄与条款确认 → 免费套餐和入门设置 → 验证登录完成」整理为可复用 skill。适用于用户本人授权的单个账号；不包含批量注册、绕过验证或真实账号数据。

## Contents

- [SKILL.md](skills/agentmail-claude-signup/SKILL.md): the workflow and approval boundaries
- [Recovery guidance](skills/agentmail-claude-signup/references/recovery.md): resume safely without duplicate accounts
- [Offline dry runs](skills/agentmail-claude-signup/references/dry-runs.md): decision checks without live signup
- `agents/openai.yaml`: skill display metadata

## Use

Copy the `skills/agentmail-claude-signup` folder into a skill location supported by your Codex client, preserving its name and contents. Follow the current [official skill documentation](https://developers.openai.com/codex/skills) for your installation. This repository does not automatically install anything.

Example request:

> Use $agentmail-claude-signup to create one AgentMail inbox for me and help me register for Claude Free. Ask me for the required permissions, age confirmation, and current terms consent.

The runtime needs a supported AgentMail connection and browser controls. Tool names, OAuth setup, and website screens vary. Inspect current schemas and the live official site instead of replaying fixed selectors. A prior successful sequence does not guarantee future availability or acceptance of a particular email provider.

## Safety and privacy

The skill itself grants no permissions. The user retains account responsibility and control of mailbox access. OAuth, age declarations, terms acceptance, CAPTCHAs, privacy choices, and unexpected requirements must follow the user's approvals and the host's stricter rules. Passwords stay in secure user-controlled entry flows. No paid upgrades, mass account creation, or autonomous messaging are included.

All account examples are invented. Never contribute live addresses, verification links, codes, credentials, browser state, screenshots of private accounts, transcripts, or private operational records. Test changes with the offline scenarios, not live registrations.

This project is independent and is not affiliated with or endorsed by AgentMail, Anthropic, or OpenAI. Product names identify the services involved. Service terms and eligibility rules continue to apply.

## License

[MIT](LICENSE) for the original documentation and metadata in this repository. This license does not cover third-party services, branding, or their terms.
