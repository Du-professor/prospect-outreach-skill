# Prospect Outreach Skill / 潜在客户外联 Skill

## 中文说明

`prospect-outreach` 是一个 Codex Skill，用于研究我方公司与潜在客户之间的产品、服务、方案、技术和商业合作匹配度，并生成基于证据、循序渐进的外联内容。

V2 将“客户是否值得发展”和“当前是否适合联系”拆开评分，避免因缺少联系人而低估一个具有战略价值的潜客。

### 核心能力

- 深度分析潜客的产品、服务、方案、技术路线、应用场景、业务模式和可能需求。
- 将我方能力映射到潜客的具体工作流，并明确证明、缺口和待确认问题。
- 分别输出 `Account Fit Score` 和 `Outreach Readiness Score`，每项满分 100。
- 应用 P1/P2/P3/P4 优先级、证据上限、联系人准备度和停止联系规则。
- 判断终端客户、OEM、系统集成、渠道经销、技术合作或长期培育路径。
- 输出联系人/购买委员会建议、CRM 字段和重新激活条件。
- 生成潜客当地语言和英文可发送版本；需要时增加中文内部参考译文。
- 支持客户开发、合作伙伴开发、LinkedIn、WhatsApp/微信和电话开场场景。
- 根据真实回复生成后续答复，并为线上或现场会议准备确认邮件、议程、问题和会后跟进。
- 对批量名单进行名称规范化、重复合并、状态保留和优先级排序。

### 双评分与优先级

`Account Fit Score` 衡量战略匹配度：

- 产品/场景匹配：30
- 技术方案匹配：25
- 痛点与需求相关性：20
- 商业合作路径：15
- 证据可信度：10

`Outreach Readiness Score` 衡量当前外联条件：

- 联系人角色：25
- 触发事件与时机：25
- 证据新鲜度：20
- 可用业务联系渠道：15
- 个性化信息充分度：15

Account Fit 决定基础优先级，Outreach Readiness 和证据规则决定最终可执行优先级。缺少联系人只降低外联准备度，不降低账户本身的战略匹配度。

### 输出模式

- `brief`：决策摘要、双评分、优先级和首封允许发送的邮件。
- `standard`：完整客户画像、证据、产品映射、评分、邮件包、CRM 和 QA；默认模式。
- `deep`：增加完整证据台账、技术分析、购买委员会、联系人选择、异议和重新激活条件。
- `batch`：先去重和排序，只默认深入分析 P1/P2 客户。

### 邮件规则

- P1/P2：初始邮件、跟进 1、跟进 2、最终跟进。
- P3：一封研究/路由邮件，以及一封明确标记为可选的跟进。
- P4：默认不生成销售邮件；用户明确要求时仅提供一封中性研究询问。
- 第一封邮件可以说明合作或方案匹配探索意图，但不能硬推产品。
- 任何回复都会暂停原序列；退订、明确拒绝、投诉或永久退信会停止后续联系。

### 安装

将 `prospect-outreach` 文件夹复制到 Codex Skills 目录：

```powershell
Copy-Item -Recurse -Force .\prospect-outreach "$env:USERPROFILE\.codex\skills\prospect-outreach"
```

安装后重启 Codex，或新建任务以刷新 Skill 索引。

### 使用示例

```text
使用 $prospect-outreach 深度分析我们公司和潜在客户，输出双评分、合作路径、中文参考和可发送英文邮件。

我们公司：https://example.com
潜在客户：https://prospect.example
联系人：Head of Automation
输出模式：deep
```

批量示例：

```text
使用 $prospect-outreach 的 batch 模式整理这份公司名单。合并重复公司，保留已联系和拒绝联系状态，优先分析 P1/P2。
```

### 安全边界

该 Skill 只负责研究、评分和撰写草稿，不发送邮件、不连接邮箱或 CRM、不推测私人邮箱、不抓取私人联系人，也不生成大规模自动群发流程。

请勿向公开仓库提交 API Key、令牌、密码、IP 地址、个人工作路径、私人联系人、客户非公开信息、报价、合同或邮件系统配置。

### 贡献者

- Du-professor：Skill 创建者与维护者
- Codex：AI 协作开发与文档支持

---

## English

`prospect-outreach` is a Codex Skill for researching the product, service, solution, technical, and commercial fit between a user's company and prospective accounts, then drafting evidence-based consultative outreach.

V2 separates strategic account quality from the ability to contact an account now, so a missing contact does not incorrectly reduce the account's underlying value.

### Core Capabilities

- Profile prospect products, services, solutions, technology direction, applications, business model, and likely needs.
- Map demonstrated user-company capabilities to specific prospect workflows, proof, gaps, and verification questions.
- Score `Account Fit` and `Outreach Readiness` separately, each out of 100.
- Apply P1/P2/P3/P4 priorities, evidence caps, readiness gates, and stop-contact status.
- Select an end-customer, OEM, systems-integrator, channel/distributor, technical-partnership, or nurture path.
- Produce buying-committee guidance, CRM fields, contact-channel recommendations, and reactivation conditions.
- Generate prospect-local and English sendable versions, plus a Chinese internal-reference translation when needed.
- Support customer development, partner development, LinkedIn, WhatsApp/WeChat, and phone-opening scenarios.
- Draft context-aware replies and prepare online or on-site meeting confirmations, agendas, discovery questions, and recaps.
- Normalize and deduplicate batch account lists while preserving prior-contact status.

### Dual Scoring

`Account Fit Score` evaluates product/scenario fit, technical fit, need relevance, commercial path, and evidence confidence.

`Outreach Readiness Score` evaluates contact-role relevance, trigger/timing, evidence freshness, public business-channel availability, and personalization sufficiency.

Account Fit determines base priority. Readiness, evidence, account status, and risk caps determine final actionable priority.

### Output Modes

- `brief`: decision, dual scores, priority, best angle, and first permitted message.
- `standard`: full profile, evidence, product mapping, scores, outreach, CRM fields, and QA; this is the default.
- `deep`: adds the full evidence ledger, technical hypotheses, buying committee, contact-channel comparison, objections, and reactivation plan.
- `batch`: normalizes and prioritizes a list, then deeply analyzes P1/P2 accounts by default.

### Sequence Rules

- P1/P2: initial email plus three gradual follow-ups.
- P3: one research/routing email and one explicitly optional follow-up.
- P4: no sales sequence by default; one neutral research note only when explicitly requested.
- Any reply pauses the planned sequence. Opt-out, explicit refusal, complaint, or permanent bounce suppresses further outreach.

### Installation

Copy the `prospect-outreach` folder into the Codex Skills directory:

```powershell
Copy-Item -Recurse -Force .\prospect-outreach "$env:USERPROFILE\.codex\skills\prospect-outreach"
```

Restart Codex or start a new task to refresh the Skill index.

### Example

```text
Use $prospect-outreach in deep mode to analyze our company and this prospect, score account fit and outreach readiness, select the best cooperation path, and draft localized outreach.

Our company: https://example.com
Prospect: https://prospect.example
Contact: Head of Automation
```

### Safety Boundary

This Skill researches, prioritizes, and drafts only. It does not send messages, connect email or CRM accounts, infer private addresses, scrape private contacts, or create bulk outreach automation.

Do not commit API keys, tokens, passwords, IP addresses, personal workstation paths, private contacts, non-public customer information, pricing, contracts, or email-system configuration to a public repository.

### Contributors

- Du-professor: Skill creator and maintainer
- Codex: AI-assisted development and documentation support
