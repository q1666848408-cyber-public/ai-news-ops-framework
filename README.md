<div align="center">

# 📰 AI News Ops Framework

[![Claude Code](https://img.shields.io/badge/Claude-Code-D4A843?style=flat-square&logo=anthropic&logoColor=white)](https://claude.com/code)
[![Skills](https://img.shields.io/badge/Skills-12+-7B68EE?style=flat-square)](https://github.com)
[![Slash Commands](https://img.shields.io/badge/Slash-Commands-FF6B35?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

**Claude Code-driven content operations skeleton — Skills + Slash Commands + content library conventions for multi-platform publishing**

> ⚠️ **Showcase Only** — ~15% skeleton. Production skills, internal templates & content library not included.

</div>

---

## ✨ Overview

A reusable scaffolding for AI content teams. It encodes the team's content workflow as Claude Code Skills and Slash Commands — from sourcing trending topics to producing multi-platform copy + video assets — so each new piece of content follows the same proven pipeline.

Pairs with a separate rendering engine (graphic + video) for asset production.

---

## 🏗️ Architecture

```
  Trending Sources              Claude Code Agent
 ┌──────────────┐               ┌──────────────────┐
 │ GitHub       │               │  Skills          │
 │ X / Twitter  │──── intel ───►│  · news-fetch    │
 │ Tech Blogs   │               │  · copywriting   │
 └──────────────┘               │  · multi-platform│
                                │  · render-bridge │
                                └────────┬─────────┘
                                         │
                              ┌──────────▼──────────┐
                              │  Slash Commands     │
                              │  /publish-juejin    │
                              │  /publish-zhihu     │
                              │  /generate-video    │
                              └──────────┬──────────┘
                                         │
                                         ▼
                              ┌─────────────────────┐
                              │  Content Library    │
                              │  (versioned MD)     │
                              └─────────────────────┘
```

---

## 📁 Structure

```
ai-news-ops-framework/
├── .claude/
│   └── skills/
│       ├── news-fetch-skill/
│       │   └── SKILL.md
│       └── copywriting-skill/
│           └── SKILL.md
├── workflow-guide/
│   └── README.md             # End-to-end usage
└── content_library/.gitkeep   # Versioned content output
```

---

## 🔧 Tech Stack

| Layer | Technology |
|---|---|
| Agent Platform | Claude Code |
| Format | Markdown skill files + slash command files |
| Asset Pipeline | Bridges to `ai-content-rendering-engine` |
| Source Control | Git (versioned content) |

---

<div align="center">
<sub>Showcase version · Production skills not included · For portfolio reference only</sub>
</div>
