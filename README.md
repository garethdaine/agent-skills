# Agent Skills

> Curated AI agent skills for the AgentOps platform. Contains SKILL.md files, scripts, and resources from trusted open-source skill repositories, bundled as git submodules.

## What This Repository Contains

This repo aggregates **high-quality, vetted agent skills** (SKILL.md format) from trusted sources. Skills are compatible with Claude Code, Codex CLI, Cursor, GitHub Copilot, Gemini CLI, and Windsurf.

### Bundled Skill Repositories

#### Official Vendor Skills

| Submodule | Path | What It Provides |
|---|---|---|
| **anthropics/skills** | `vendor/anthropics/skills/` | Official Anthropic skills: claude-api, mcp-builder, frontend-design, webapp-testing, skill-creator, doc-coauthoring, canvas-design, brand-guidelines, and more. |
| **vercel-labs/agent-skills** | `vendor/vercel-labs/agent-skills/` | React best practices (40+ rules), web design guidelines (100+ rules), composition patterns, React Native skills. |
| **getsentry/skills** | `vendor/getsentry/skills/` | Sentry integration: error tracking, PR review workflows, blog writing, security reviews. |
| **hashicorp/agent-skills** | `vendor/hashicorp/agent-skills/` | Terraform style guide, testing, Azure Verified Modules, Stacks, provider development, Packer builders. |
| **supabase/agent-skills** | `vendor/supabase/agent-skills/` | PostgreSQL best practices: query performance, connection management, schema design, RLS, indexing, N+1, pagination. |
| **LambdaTest/agent-skills** | `vendor/LambdaTest/agent-skills/` | 46+ testing skills: Selenium, Playwright, Cypress, Jest, pytest, Puppeteer, WebDriverIO, TestCafe, Appium, and more. |

#### Security Skills

| Submodule | Path | What It Provides |
|---|---|---|
| **trailofbits/skills** | `vendor/trailofbits/skills/` | Security research, CodeQL/Semgrep static analysis, variant analysis, code auditing, 14+ skills. |
| **agamm/claude-code-owasp** | `vendor/agamm/claude-code-owasp/` | OWASP Top 10:2025, ASVS 5.0, Agentic AI Security (ASI01–ASI10), 20+ language-specific quirks. |
| **netresearch/security-audit-skill** | `vendor/netresearch/security-audit-skill/` | 80+ checkpoints, CWE Top 25, CVSS v4.0, PHP/TYPO3 scanning, DevSecOps (semgrep, trivy, gitleaks). |
| **BehiSecc/VibeSec-Skill** | `vendor/BehiSecc/VibeSec-Skill/` | Secure code patterns, vulnerability prevention. |

#### Framework & Technology Skills

| Submodule | Path | What It Provides |
|---|---|---|
| **onmax/nuxt-skills** | `vendor/onmax/nuxt-skills/` | 17 skills: Vue 3, Nuxt 4+, NuxtHub, Nuxt Content v3, Nuxt UI v4, Vitest, VueUse, TresJS. |
| **Lombiq/Tailwind-Agent-Skills** | `vendor/Lombiq/Tailwind-Agent-Skills/` | Tailwind v4 documentation skill with local docs snapshot and sync script. |
| **addyosmani/web-quality-skills** | `vendor/addyosmani/web-quality-skills/` | Core Web Vitals, WCAG 2.1, Lighthouse performance, accessibility, SEO, best practices (6 skills). |

#### Methodology & Workflow Skills

| Submodule | Path | What It Provides |
|---|---|---|
| **obra/superpowers** | `vendor/obra/superpowers/` | Agentic workflow: brainstorm → write-plan → TDD → systematic-debugging → root-cause-tracing → verification chain. |
| **sickn33/antigravity-awesome-skills** | `vendor/sickn33/antigravity-awesome-skills/` | 1,272+ universal skills. Bundles (role-based) and Workflows (multi-skill playbooks). Compatible with 10+ AI tools. |
| **ccheney/robust-skills** | `vendor/ccheney/robust-skills/` | Clean Architecture + DDD + Hexagonal for Go, Rust, Python, TS, Java, C#; Feature-Sliced Design for frontend. |

## Installation

### As a Composer dependency (recommended for AgentOps)

Add this repository to your project's `composer.json`:

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "git@github.com:garethdaine/agent-skills.git"
        }
    ],
    "require-dev": {
        "garethdaine/agent-skills": "dev-main"
    }
}
```

Then run:

```bash
composer update garethdaine/agent-skills --prefer-source
cd vendor/garethdaine/agent-skills && git submodule update --init --recursive
```

### Standalone clone

```bash
git clone --recurse-submodules git@github.com:garethdaine/agent-skills.git
```

## Key Skill Paths

| Category | Skill | Path |
|---|---|---|
| **AI API** | Claude API | `vendor/anthropics/skills/skills/claude-api/` |
| **AI API** | MCP Builder | `vendor/anthropics/skills/skills/mcp-builder/` |
| **AI API** | Skill Creator | `vendor/anthropics/skills/skills/skill-creator/` |
| **Design** | Frontend Design | `vendor/anthropics/skills/skills/frontend-design/` |
| **Testing** | Webapp Testing | `vendor/anthropics/skills/skills/webapp-testing/` |
| **Docs** | Doc Co-authoring | `vendor/anthropics/skills/skills/doc-coauthoring/` |
| **React** | Best Practices | `vendor/vercel-labs/agent-skills/skills/react-best-practices/` |
| **React** | Composition Patterns | `vendor/vercel-labs/agent-skills/skills/composition-patterns/` |
| **UI** | Web Design Guidelines | `vendor/vercel-labs/agent-skills/skills/web-design-guidelines/` |
| **Vue/Nuxt** | Full ecosystem | `vendor/onmax/nuxt-skills/` |
| **Tailwind** | v4 Docs | `vendor/Lombiq/Tailwind-Agent-Skills/` |
| **PostgreSQL** | Best Practices | `vendor/supabase/agent-skills/` |
| **Security** | Trail of Bits | `vendor/trailofbits/skills/` |
| **Security** | OWASP 2025 | `vendor/agamm/claude-code-owasp/` |
| **Security** | Audit (80+ checks) | `vendor/netresearch/security-audit-skill/` |
| **Terraform** | Style & Testing | `vendor/hashicorp/agent-skills/` |
| **Testing** | 46+ Frameworks | `vendor/LambdaTest/agent-skills/` |
| **Errors** | Sentry Integration | `vendor/getsentry/skills/` |
| **Workflow** | TDD + Debugging | `vendor/obra/superpowers/` |
| **Web Quality** | Lighthouse + CWV | `vendor/addyosmani/web-quality-skills/skills/` |
| **Architecture** | DDD + Clean Arch | `vendor/ccheney/robust-skills/` |

## Updating

```bash
git submodule update --remote --merge
git add . && git commit -m "chore: update skill submodules"
```

## Related

- **[agent-rules](https://github.com/garethdaine/agent-rules)** — Companion repository for .mdc cursor rules and coding standards
- **[agent](https://github.com/garethdaine/agent)** — The AgentOps platform

---

*Maintained as part of the AgentOps platform. See `agent-ops-engineering-rules.md` for the full standards document.*
