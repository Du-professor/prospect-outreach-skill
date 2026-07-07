# Prospect Outreach Skill / 潜在客户外联 Skill

## 中文说明

`prospect-outreach` 是一个 Codex skill，用于分析“我方公司”和“潜在客户公司”的业务、产品、服务、方案和技术匹配度，并基于评分生成循序渐进的个性化外联邮件。

它适合用于 B2B 销售、合作伙伴开发、客户匹配分析、潜在客户优先级判断，以及中英文外联邮件草稿生成。

### 核心能力

- 分析我方公司的网站、产品、服务、方案、技术能力和差异化优势。
- 深度分析潜在客户公司的产品内容、服务内容、方案内容、应用场景、技术路线、可能痛点和合作机会。
- 使用 100 分评分框架评估客户匹配度和发展潜力。
- 输出 P1/P2/P3/P4 发送优先级和是否值得发展为客户或合作伙伴。
- 根据评分档位生成循序渐进的外联邮件。
- 同时生成潜在客户当地语言版本和英文版本。
- 第一封邮件可以说明合作或方案匹配探索意图，但不能硬推产品。
- 明确区分事实、推断、未知项和证据不足的部分。
- 增加合规约束、硬性降级规则、发送前 QA、CRM 字段和多潜客优先级表。

### 适用场景

- 输入我方官网和潜在客户官网，判断是否值得主动联系。
- 输入潜在客户联系人信息，生成更贴近角色的外联邮件。
- 对多个潜在客户进行优先级排序。
- 为销售、市场、BD 或合作伙伴团队准备初步客户研究和邮件草稿。

### 输出内容

每次使用该 skill 时，输出通常包含：

- 客户画像分析
- 我方匹配分析
- 匹配评分表
- 外联优先级
- 潜在客户当地语言邮件包
- 英文邮件包
- 合规与风险提示

### 安装方式

将 `prospect-outreach` 文件夹复制到 Codex skills 目录：

```bash
cp -r prospect-outreach ~/.codex/skills/
```

Windows PowerShell 示例：

```powershell
Copy-Item -Recurse -Force .\prospect-outreach "$env:USERPROFILE\.codex\skills\prospect-outreach"
```

安装后重启 Codex，或新建线程以刷新 skill 索引。

### 使用示例

```text
Use $prospect-outreach to analyze our company website and this prospect website, score the fit, and draft local-language plus English outreach emails.

Our company: https://example.com
Prospect company: https://example-prospect.com
Contact: Head of Automation
```

中文示例：

```text
使用 $prospect-outreach 分析我们公司和这个潜在客户公司的匹配度，并生成中文和英文外联邮件。

我们公司：https://example.com
潜在客户：https://example-prospect.com
联系人：自动化负责人
```

### 贡献者

- Du-professor：Skill 创建者与维护者
- Codex：AI 协作开发与文档支持

### 隐私与安全

本仓库不包含 API key、访问令牌、账号密码、IP 地址、个人工作路径、客户私密数据或任何运行时缓存。

使用该 skill 时，请不要在公开仓库中提交真实客户的非公开信息、联系人私人信息、内部报价、合同、凭据或邮件系统配置。

---

## English

`prospect-outreach` is a Codex skill for analyzing the fit between your company and a prospective customer company, then drafting gradual, personalized outbound email sequences based on account scoring.

It is designed for B2B sales, partner development, account research, lead qualification, prospect prioritization, and bilingual outreach drafting.

### Key Capabilities

- Analyze your company's website, products, services, solutions, technical capabilities, and differentiators.
- Deeply profile a prospect's products, services, solutions, application scenarios, technical direction, likely pain points, and cooperation opportunities.
- Use a 100-point scoring framework to evaluate account fit and development potential.
- Assign P1/P2/P3/P4 outreach priority and determine whether the prospect is worth developing as a customer or partner.
- Draft score-aware consultative outreach sequences.
- Generate both the prospect-local language version and an English version.
- Allow the first email to state a restrained cooperation or fit-exploration intent without hard-selling products.
- Clearly separate sourced facts, reasonable inferences, unknowns, and weak evidence.
- Add compliance guardrails, hard downgrade rules, pre-send QA, CRM fields, and multi-prospect priority tables.

### Use Cases

- Compare your company website with a prospect website and decide whether to reach out.
- Draft role-aware outreach emails based on a contact's title or function.
- Prioritize multiple prospective accounts.
- Prepare account research and outreach drafts for sales, marketing, BD, or partner teams.

### Typical Output

The skill normally returns:

- Customer profile analysis
- Your-company fit analysis
- Fit scoring table
- Outreach priority
- Prospect-local language email package
- English email package
- Compliance and risk notes

### Installation

Copy the `prospect-outreach` folder into your Codex skills directory:

```bash
cp -r prospect-outreach ~/.codex/skills/
```

Windows PowerShell example:

```powershell
Copy-Item -Recurse -Force .\prospect-outreach "$env:USERPROFILE\.codex\skills\prospect-outreach"
```

Restart Codex, or start a new thread, so the skill index can refresh.

### Example Prompt

```text
Use $prospect-outreach to analyze our company website and this prospect website, score the fit, and draft local-language plus English outreach emails.

Our company: https://example.com
Prospect company: https://example-prospect.com
Contact: Head of Automation
```

### Contributors

- Du-professor: Skill creator and maintainer
- Codex: AI-assisted development and documentation support

### Privacy and Security

This repository does not include API keys, access tokens, passwords, IP addresses, personal workstation paths, private customer data, or runtime caches.

Do not commit real non-public prospect information, private contact data, internal pricing, contracts, credentials, or email-system configuration to a public repository.
