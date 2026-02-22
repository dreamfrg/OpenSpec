<p align="center">
  <a href="https://github.com/Fission-AI/OpenSpec">
    <picture>
      <source srcset="assets/openspec_bg.png">
      <img src="assets/openspec_bg.png" alt="OpenSpec logo">
    </picture>
  </a>
</p>

<p align="center">
  <a href="https://github.com/Fission-AI/OpenSpec/actions/workflows/ci.yml"><img alt="CI" src="https://github.com/Fission-AI/OpenSpec/actions/workflows/ci.yml/badge.svg" /></a>
  <a href="https://www.npmjs.com/package/@fission-ai/openspec"><img alt="npm version" src="https://img.shields.io/npm/v/@fission-ai/openspec?style=flat-square" /></a>
  <a href="./LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square" /></a>
  <a href="https://discord.gg/YctCnvvshC"><img alt="Discord" src="https://img.shields.io/discord/1411657095639601154?style=flat-square&logo=discord&logoColor=white&label=Discord&suffix=%20online" /></a>
</p>

<details>
<summary><strong>The most loved spec framework.</strong></summary>

[![Stars](https://img.shields.io/github/stars/Fission-AI/OpenSpec?style=flat-square&label=Stars)](https://github.com/Fission-AI/OpenSpec/stargazers)
[![Downloads](https://img.shields.io/npm/dm/@fission-ai/openspec?style=flat-square&label=Downloads/mo)](https://www.npmjs.com/package/@fission-ai/openspec)
[![Contributors](https://img.shields.io/github/contributors/Fission-AI/OpenSpec?style=flat-square&label=Contributors)](https://github.com/Fission-AI/OpenSpec/graphs/contributors)

</details>
<p></p>
Our philosophy:

```text
→ fluid not rigid
→ iterative not waterfall
→ easy not complex
→ built for brownfield not just greenfield
→ scalable from personal projects to enterprises
```

> [!TIP]
> **New workflow now available!** We've rebuilt OpenSpec with a new artifact-guided workflow.
>
> Run `/opsx:onboard` to get started. → [Learn more here](docs/opsx.md)

<p align="center">
  Follow <a href="https://x.com/0xTab">@0xTab on X</a> for updates · Join the <a href="https://discord.gg/YctCnvvshC">OpenSpec Discord</a> for help and questions.
</p>

### Teams

Using OpenSpec in a team? [Email here](mailto:teams@openspec.dev) for access to our Slack channel.

<!-- TODO: Add GIF demo of /opsx:new → /opsx:archive workflow -->

## See it in action

```text
You: /opsx:new add-dark-mode
AI:  Created openspec/changes/add-dark-mode/
     Ready to create: proposal

You: /opsx:ff   # "fast-forward" - generate all planning docs
AI:  ✓ proposal.md — why we're doing this, what's changing
     ✓ specs/       — requirements and scenarios
     ✓ design.md    — technical approach
     ✓ tasks.md     — implementation checklist
     Ready for implementation!

You: /opsx:apply
AI:  Implementing tasks...
     ✓ 1.1 Add theme context provider
     ✓ 1.2 Create toggle component
     ✓ 2.1 Add CSS variables
     ✓ 2.2 Wire up localStorage
     All tasks complete!

You: /opsx:archive
AI:  Archived to openspec/changes/archive/2025-01-23-add-dark-mode/
     Specs updated. Ready for the next feature.
```

<details>
<summary><strong>OpenSpec Dashboard</strong></summary>

<p align="center">
  <img src="assets/openspec_dashboard.png" alt="OpenSpec dashboard preview" width="90%">
</p>

</details>

## Quick Start

**Requires Node.js 20.19.0 or higher.**

Install OpenSpec globally:

```bash
npm install -g @fission-ai/openspec@latest
```

Then navigate to your project directory and initialize:

```bash
cd your-project
openspec init
```

Now tell your AI: `/opsx:new <what-you-want-to-build>`

> [!NOTE]
> Not sure if your tool is supported? [View the full list](docs/supported-tools.md) – we support 20+ tools and growing.
>
> Also works with pnpm, yarn, bun, and nix. [See installation options](docs/installation.md).

## Docs

→ **[Getting Started](docs/getting-started.md)**: first steps<br>
→ **[Workflows](docs/workflows.md)**: combos and patterns<br>
→ **[Commands](docs/commands.md)**: slash commands & skills<br>
→ **[CLI](docs/cli.md)**: terminal reference<br>
→ **[Supported Tools](docs/supported-tools.md)**: tool integrations & install paths<br>
→ **[Concepts](docs/concepts.md)**: how it all fits<br>
→ **[Multi-Language](docs/multi-language.md)**: multi-language support<br>
→ **[Customization](docs/customization.md)**: make it yours


## Why OpenSpec?

AI coding assistants are powerful but unpredictable when requirements live only in chat history. OpenSpec adds a lightweight spec layer so you agree on what to build before any code is written.

- **Agree before you build** — human and AI align on specs before code gets written
- **Stay organized** — each change gets its own folder with proposal, specs, design, and tasks
- **Work fluidly** — update any artifact anytime, no rigid phase gates
- **Use your tools** — works with 20+ AI assistants via slash commands

### How we compare

**vs. [Spec Kit](https://github.com/github/spec-kit)** (GitHub) — Thorough but heavyweight. Rigid phase gates, lots of Markdown, Python setup. OpenSpec is lighter and lets you iterate freely.

**vs. [Kiro](https://kiro.dev)** (AWS) — Powerful but you're locked into their IDE and limited to Claude models. OpenSpec works with the tools you already use.

**vs. nothing** — AI coding without specs means vague prompts and unpredictable results. OpenSpec brings predictability without the ceremony.

## Updating OpenSpec

**Upgrade the package**

```bash
npm install -g @fission-ai/openspec@latest
```

**Refresh agent instructions**

Run this inside each project to regenerate AI guidance and ensure the latest slash commands are active:

```bash
openspec update
```

## Usage Notes

**Model selection**: OpenSpec works best with high-reasoning models. We recommend Opus 4.5 and GPT 5.2 for both planning and implementation.

**Context hygiene**: OpenSpec benefits from a clean context window. Clear your context before starting implementation and maintain good context hygiene throughout your session.

## Contributing

**Small fixes** — Bug fixes, typo corrections, and minor improvements can be submitted directly as PRs.

**Larger changes** — For new features, significant refactors, or architectural changes, please submit an OpenSpec change proposal first so we can align on intent and goals before implementation begins.

When writing proposals, keep the OpenSpec philosophy in mind: we serve a wide variety of users across different coding agents, models, and use cases. Changes should work well for everyone.

**AI-generated code is welcome** — as long as it's been tested and verified. PRs containing AI-generated code should mention the coding agent and model used (e.g., "Generated with Claude Code using claude-opus-4-5-20251101").

### Development

- Install dependencies: `pnpm install`
- Build: `pnpm run build`
- Test: `pnpm test`
- Develop CLI locally: `pnpm run dev` or `pnpm run dev:cli`
- Conventional commits (one-line): `type(scope): subject`

## Other

<details>
<summary><strong>Telemetry</strong></summary>

OpenSpec collects anonymous usage stats.

We collect only command names and version to understand usage patterns. No arguments, paths, content, or PII. Automatically disabled in CI.

**Opt-out:** `export OPENSPEC_TELEMETRY=0` or `export DO_NOT_TRACK=1`

</details>

<details>
<summary><strong>Maintainers & Advisors</strong></summary>

See [MAINTAINERS.md](MAINTAINERS.md) for the list of core maintainers and advisors who help guide the project.

</details>



## License

MIT


# 最受喜爱的规范框架

我们的理念：

```
text → fluid not rigid → iterative not waterfall → easy not complex → built for brownfield not just greenfield → scalable from personal projects to enterprises
```

（译：文字 → 灵活而非僵硬 → 迭代而非瀑布 → 简单而非复杂 → 为已有项目而非仅新项目构建 → 可从个人项目扩展到企业级）

> 新工作流现已可用！  
> 我们使用新的基于 artifact（工件）的工作流重建了 OpenSpec。  
> 运行 `/opsx:onboard` 开始。 → 在 docs/opsx.md 中了解更多

关注 @0xTab 的 X 获取更新 · 加入 OpenSpec Discord 获取帮助与交流。

如需团队使用 OpenSpec？请发送邮件至 teams@openspec.dev 获取访问 Slack 的权限。

---

## 实例演示

```
You: /opsx:new add-dark-mode
AI: Created openspec/changes/add-dark-mode/
    Ready to create: proposal
You: /opsx:ff   # “fast-forward” — 生成所有规划文档
AI: ✓ proposal.md — 为什么要做，变更内容是什么，影响范围
    ✓ specs/ — 需求和场景
    ✓ design.md — 技术实现方案
    ✓ tasks.md — 实施任务清单
    Ready for implementation!
You: /opsx:apply
AI: Implementing tasks…
    ✓ 1.1 Add theme context provider
    ✓ 1.2 Create toggle component
    ✓ 2.1 Add CSS variables
    ✓ 2.2 Wire up localStorage
    All tasks complete!
You: /opsx:archive
AI: Archived to openspec/changes/archive/2025-01-23-add-dark-mode/
    Specs updated. Ready for the next feature.
```

---

## 快速开始

需要 Node.js 20.19.0 或更高版本。

全局安装 OpenSpec：

```bash
npm install -g @fission-ai/openspec@latest
```

然后进入你的项目目录并初始化：

```bash
cd your-project
openspec init
```

现在告诉你的 AI：`/opsx:new `

> 注意  
> 不确定你的工具是否受支持？查看 docs/supported-tools.md —— 我们支持 20+ AI 工具，并持续增长。  
> 同样支持 pnpm、yarn、bun 和 nix。

---

## 文档目录

- 初学者指南（Getting Started）：第一步入门  
- 工作流（Workflows）：组合与模式  
- 命令（Commands）：斜杠命令和技能  
- CLI：终端参考  
- 支持的工具：集成与安装路径  
- 概念（Concepts）：整体运作逻辑  
- 多语言支持  
- 自定义：定制你的版本  

---

## 为什么选择 OpenSpec？

AI 编码助手虽然强大，但当需求只存在于聊天历史中时，输出往往难以预测。OpenSpec 增加了一层轻量的规范（spec）机制，让你在写任何代码之前先对齐要做什么，为你提供确定性和可审查的输出结果。

### 核心优势

- 先达成一致，再构建 —— 人类与 AI 在写代码前先对齐规范  
- 保持有序 —— 每个变更都有自己的文件夹：proposal、specs、design、tasks  
- 灵活迭代 —— 可随时更新任意制品，无僵硬阶段门槛  
- 使用你现有的工具 —— 通过斜杠命令支持 20+ AI 编码助手  

---

## 我们如何对比

与 Spec Kit（GitHub）相比 —— 规范齐全但偏重，阶段门槛严格，Markdown 多，需 Python 环境。  
OpenSpec 更轻量，更适合自由迭代。

与 Kiro（AWS）相比 —— 功能强大但受限于 IDE，并且模型选择受限（主要是 Claude）。OpenSpec 可与现有工具协作。

与没有规范相比 —— 仅靠聊天做 AI 编程容易产生模糊需求和不可预测的实现。OpenSpec 在不增加太多仪式感前提下带来更可预期的结果。

---

## 更新 OpenSpec

升级包版本：

```bash
npm install -g @fission-ai/openspec@latest
```

刷新代理指令（在每个项目里运行）：

```bash
openspec update
```

用于重新生成 AI 指引，并确保最新斜杠命令可用。

---

## 使用注意

- 模型选择：OpenSpec 最适合高推理能力模型，推荐用于规划与实现阶段。  
- 上下文卫生：在开始实现前清理上下文，并在整个会话中保持良好的上下文卫生，以提升效果。

---

## 贡献指南

- 小修小补 —— Bug 修复、错别字修正和小改进可以直接提交 PR。  
- 较大改动 —— 对于新功能、重大重构或架构调整，请先提交一个 OpenSpec 变更提案（change proposal），在实施前对齐意图和目标。

在撰写提案时，请牢记 OpenSpec 的理念：我们服务于各种编码代理、模型和使用场景。改动应能满足所有人。  
AI 生成代码同样欢迎 —— 只要经过测试和验证。PR 中含有 AI 代码时，请注明使用的编码代理与模型。

---

## 开发

```bash
# 安装依赖
pnpm install

# 构建
pnpm run build

# 测试
pnpm test

# 本地开发 CLI
pnpm run dev
或
pnpm run dev:cli

# 约定式提交（单行）
type(scope): subject
```

---

## 其它

### 遥测（Telemetry）

OpenSpec 收集匿名使用统计，仅收集命令名和版本号以理解使用模式。不会收集参数、路径、内容或任何个人信息。CI 环境中自动禁用。可以通过环境变量关闭：

```bash
export OPENSPEC_TELEMETRY=0
export DO_NOT_TRACK=1
```

---

## 许可证

MIT
