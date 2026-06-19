<div align="center">

<!-- HERO BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4652EB,50:3C48E6,100:4652EB&height=230&section=header&text=Daksh%20Hiran&fontSize=68&fontColor=D1D3EB&fontAlignY=40&desc=Systems%20Engineer%20%E2%80%A2%20Open-Source%20Contributor%20%E2%80%A2%20TypeScript%20Maximalist&descColor=94a3b8&descSize=16&descAlignY=62&animation=twinkling" width="100%" />

<!-- TYPING ANIMATION -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&pause=1000&color=A78BFA&center=true&vCenter=true&width=680&lines=Full-Stack+Engineer+%7C+TypeScript+96.7%25+of+the+time;Docker+Orchestration+%2B+Zero-Downtime+Systems;Model+Context+Protocol+%E2%80%94+AI+%C3%97+Infrastructure;Open-Source+%40+Twenty+%C2%B7+Nhost+%C2%B7+Formbricks;Building+on-chain+%26+off-chain+primitives)](https://git.io/typing-svg)

<br/>

<!-- SOCIAL LINKS -->
<a href="https://daksh-hiran.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-0F0C29?style=for-the-badge&logo=vercel&logoColor=a78bfa"/></a>
<a href="https://www.linkedin.com/in/daksh-hiran-9534b930b"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://x.com/dakshhiran7"><img src="https://img.shields.io/badge/X%20%2F%20Twitter-000000?style=for-the-badge&logo=x&logoColor=white"/></a>
<a href="mailto:daksh.hiran@gmail.com"><img src="https://img.shields.io/badge/Email-A78BFA?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://codolio.com/profile/Daksh7"><img src="https://img.shields.io/badge/DSA%20Profile-FF6B6B?style=for-the-badge&logo=leetcode&logoColor=white"/></a>
<a href="https://bento.me/daksh7"><img src="https://img.shields.io/badge/Bento-FF9500?style=for-the-badge&logo=bento&logoColor=white"/></a>
<a href="https://synthesis-labs.vercel.app/"><img src="https://img.shields.io/badge/Synthesis_Labs-302B63?style=for-the-badge&logo=flask&logoColor=white"/></a>

<br/><br/>

<img src="https://img.shields.io/badge/TypeScript-96.7%25_of_code-3178C6?style=for-the-badge&logo=typescript&logoColor=white&labelColor=0F0C29"/>
<img src="https://img.shields.io/badge/Status-Open%20to%20Mentorship-10b981?style=for-the-badge&labelColor=0F0C29"/>
<img src="https://komarev.com/ghpvc/?username=Dakshx07&style=for-the-badge&color=302B63&label=PROFILE+VIEWS&labelColor=0F0C29"/>

</div>

---

## `$ whoami`

```typescript
const daksh: Engineer = {
  name:       "Daksh Hiran",
  handle:     "@Dakshx07",
  location:   "Jaipur, Rajasthan, India 🇮🇳",
  degree:     "B.Tech Computer Science — JECRC University",

  roles: [
    "Full-Stack Engineer",
    "Mobile App Developer",   // iOS · Swift · React Native
    "Web3 & Blockchain Builder",
    "AI Systems Architect",
    "MCP Agent Integrations",
  ],

  currentlyBuilding: [
    "MCP-orchestrated streaming platforms",
    "Blockchain prescription verification (MediChain)",
    "AI threat intelligence dashboards (Sentinel ML)",
    "Premium research interfaces (Synthesis Labs)",
  ],

  philosophy: [
    "Types are documentation that compiles",
    "Uptime is a product feature, not an afterthought",
    "Contribute upstream before building downstream",
  ],

  funFact:    "96.7% of my code screams TypeScript 💙",
  openTo:     ["LFX Mentorship", "MLH Fellowship", "OSS Collaborations"],
};
```

---

## `$ git log --oneline --upstream` — Open-Source Contributions

> Merged patches in **Y Combinator-backed** and **category-defining** open-source systems.

<details open>
<summary><b>🟣 Twenty CRM &nbsp;|&nbsp; <code>PR #21060</code> — Type-Safe Settings Field Form Architecture</b></summary>

<br/>

**Repository:** [`twentyhq/twenty`](https://github.com/twentyhq/twenty) — YC-backed open-source CRM alternative to Salesforce

**The problem:** A developer `TODO` lived inside Twenty's frontend — unsafe index typings on `SettingsDataModelFieldEditFormValues`, plus a strict TypeScript enum incompatibility between the string union `SettingsFieldType` and its underlying GraphQL counterpart `FieldMetadataType`.

**What I shipped:**
- ✦ Introduced `SettingsDataModelFieldEditFormValues` as a proper discriminated union covering every field variant (text, number, select, relation, currency, etc.)
- ✦ Resolved the `SettingsFieldType` → `FieldMetadataType` enum casting incompatibility under `strict: true`
- ✦ Achieved **0-error** local compilation from a previously type-unsafe module

```typescript
// Before (unsafe) ↓
type SettingsDataModelFieldEditFormValues = Record<string, unknown>;

// After — PR #21060 ↓
type SettingsDataModelFieldEditFormValues =
  | SettingsDataModelFieldTextFormValues
  | SettingsDataModelFieldNumberFormValues
  | SettingsDataModelFieldSelectFormValues
  | SettingsDataModelFieldRelationFormValues;
//  ↑ Exhaustive. Discriminated. Zero escape hatches.
```

</details>

<details>
<summary><b>🟢 Nhost &nbsp;|&nbsp; <code>PR #4391</code> &amp; <code>PR #4333</code> — Unified Spinner System</b></summary>

<br/>

**Repository:** [`nhost/nhost`](https://github.com/nhost/nhost) — Open-source Firebase alternative

**The problem:** Multiple inconsistent spinner implementations across the dashboard caused UI flicker on fast network responses and non-uniform sizing/styling across the onboarding flow and project pages.

**What I shipped:**
- ✦ Upgraded core `<Spinner />` with `size` prop (`sm | md | lg`), configurable `className` overrides, and a `delay` prop to suppress flicker on sub-200ms responses
- ✦ Migrated all dashboard loader instances (onboarding + project pages) to the new unified `<Spinner />` standard
- ✦ Single source of truth — eliminated every ad-hoc loader implementation

```tsx
// PR #4391 — New Spinner API
<Spinner size="md" delay={150} className="text-purple-500" />
//                 ↑ delay prevents flicker on fast connections
```

</details>

<details>
<summary><b>🔵 Formbricks &nbsp;|&nbsp; <code>Issue #8177</code> — Docker Self-Hosted Deployment Triage</b></summary>

<br/>

**Repository:** [`formbricks/formbricks`](https://github.com/formbricks/formbricks) — Open-source product survey & analytics suite

**The problem:** A cluster of critical self-hosted Docker deployment failures affecting Postgres 18 and Node.js healthchecks in production compose stacks.

| # | Bug | Root Cause | Fix |
|---|-----|------------|-----|
| 1 | Postgres 18 container crash on startup | Data directory mount conflict with PG18 init flow | Corrected volume mount strategy for PG18 compatibility |
| 2 | Missing schema on fresh deployments | `POSTGRES_DB` env var absent from compose config | Added `POSTGRES_DB=formbricks` to trigger init scripts |
| 3 | Node.js healthcheck silent failure | `localhost` resolved to `::1` (IPv6); Cube.js only binds `127.0.0.1` (IPv4) | Shifted HTTP probe target from `localhost` → `127.0.0.1` |

```bash
# The silent killer — Node.js healthcheck on IPv6-first stacks:

# Before (fails silently):
CMD node -e "require('http').get('http://localhost:4000/health', ...)"

# After (explicit IPv4 bind):
CMD node -e "require('http').get('http://127.0.0.1:4000/health', ...)"
```

</details>

---

## `$ ls ./projects --filter=production` — Flagship Builds

<div align="center">

| | Project | Stack | Live |
|:---:|---|---|:---:|
| 🤖 | **[Sentinel ML + Supabase](https://github.com/Dakshx07/Sentinel-ML-Supabase)** — AI-powered threat intelligence with real-time anomaly detection & live dashboards | `TypeScript` `Supabase` `ML` | [↗ Live](https://sentinell-ai.netlify.app/) |
| ⛓️ | **[MediChain](https://github.com/ssid18/MediChain)** — Blockchain prescription verification fighting medical fraud via Solidity smart contracts + AI | `TypeScript` `Solidity` `Blockchain` | — |
| 📡 | **[Streaming × MCP Agent](https://github.com/Dakshx07/streaming-platform-powered-by-mcp-agent)** — Full streaming platform (Live, VOD, WebSocket chat, monetization) orchestrated by MCP agents | `TypeScript` `MCP` `WebSockets` `Docker` | — |
| 🧪 | **[Synthesis Labs](https://github.com/Dakshx07/SYNTHESIS-LABS)** — Premium AI/research lab interface for rapid prototyping & scientific experiments | `TypeScript` `React` `Framer Motion` | [↗ Live](https://synthesis-labs.vercel.app/) |
| 🌌 | **[3D Portfolio](https://github.com/Dakshx07/Daksh-Portfolio-Project)** — Personal portfolio with 3D elements, physics-based transitions & Framer Motion choreography | `TypeScript` `Three.js` `Framer Motion` | [↗ Live](https://daksh-hiran.vercel.app/) |

</div>

---

## `$ cat ./skills --verbose` — Technical Arsenal

<div align="center">

**◈ Languages**

<img src="https://skillicons.dev/icons?i=ts,js,python,cpp,solidity,swift,bash&theme=dark" />

**◈ Frontend & UI**

<img src="https://skillicons.dev/icons?i=react,nextjs,redux,tailwind,framer,html,css&theme=dark" />

**◈ Backend & Data**

<img src="https://skillicons.dev/icons?i=nodejs,express,supabase,mongodb,mysql,postgres,firebase&theme=dark" />

**◈ DevOps & Tooling**

<img src="https://skillicons.dev/icons?i=docker,git,vercel,netlify,postman,vscode,xcode&theme=dark" />

</div>

---

## `$ gh stats --user Dakshx07` — GitHub Analytics

<div align="center">

<img width="49%" src="https://github-readme-stats.vercel.app/api?username=Dakshx07&show_icons=true&theme=midnight-purple&count_private=true&hide_border=true&bg_color=0d1117&title_color=a78bfa&icon_color=a78bfa" />
<img width="49%" src="https://github-readme-streak-stats.herokuapp.com/?user=Dakshx07&theme=midnight-purple&hide_border=true&background=0d1117&ring=a78bfa&fire=ff6b6b&currStreakLabel=a78bfa" />

<br/>

<img width="42%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Dakshx07&layout=donut&theme=midnight-purple&hide_border=true&bg_color=0d1117&langs_count=8" />

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Dakshx07&bg_color=0d1117&color=a78bfa&line=7C3AED&point=E0CFFF&area=true&area_color=302B63&border_color=302B63&hide_border=true" width="95%" />

</div>

---

<!--
  UNIQUE SNAKE: Purple-to-indigo palette matching the README aesthetic.
  To generate this SVG in your repo, use the GitHub Action below:

  - uses: Platane/snk@v3
    with:
      github_user_name: Dakshx07
      outputs: |
        dist/github-contribution-grid-snake.svg
        dist/github-contribution-grid-snake-dark.svg?palette=github-dark
      svg_out_path: dist/github-contribution-grid-snake.svg
      color_snake: "#a78bfa"
      color_dots: "#0d1117,#302B63,#6d28d9,#7c3aed,#a78bfa"

  This gives a purple snake eating purple-gradient dots
  instead of the default green — unique to your brand.
-->

## `$ ./pacman --arcade` — Contribution Map

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)"
            srcset="https://raw.githubusercontent.com/Dakshx07/Dakshx07/output/pacman-contribution-graph-dark.svg?v=1" />
    <source media="(prefers-color-scheme: light)"
            srcset="https://raw.githubusercontent.com/Dakshx07/Dakshx07/output/pacman-contribution-graph.svg?v=1" />
    <img alt="Pac-Man contribution graph" src="https://raw.githubusercontent.com/Dakshx07/Dakshx07/output/pacman-contribution-graph-dark.svg?v=1" width="100%" />
  </picture>
</div>

---

## `$ curl -X GET /contact`

<div align="center">

| Channel | Link |
|:-------:|:-----|
| 🌐 Portfolio | [daksh-hiran.vercel.app](https://daksh-hiran.vercel.app/) |
| 💼 LinkedIn | [linkedin.com/in/daksh-hiran-9534b930b](https://www.linkedin.com/in/daksh-hiran-9534b930b) |
| 🐦 X / Twitter | [@dakshhiran7](https://x.com/dakshhiran7) |
| 📧 Email | [daksh.hiran@gmail.com](mailto:daksh.hiran@gmail.com) |
| 🧩 Bento | [bento.me/daksh7](https://bento.me/daksh7) |
| 📊 DSA Profile | [codolio.com/profile/Daksh7](https://codolio.com/profile/Daksh7) |
| 🧪 Synthesis Labs | [synthesis-labs.vercel.app](https://synthesis-labs.vercel.app/) |

<br/>

**Currently open to:** LFX Mentorship • MLH Fellowship • OSS Collaborations • Systems-focused Internships

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24243e,50:302B63,100:0F0C29&height=120&section=footer&animation=twinkling" width="100%"/>

</div>

<!--
  README engineered with intent.
  TypeScript strict mode. Zero `any`. No shortcuts.
  — Daksh Hiran (@Dakshx07)
-->
