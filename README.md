# AI-News-Ops-Framework

![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)

> **Showcase** — ~15% skeleton. Core implementation not included.

Content operations framework driven by Claude Code CLI. Team workflows are encoded as Skills and Slash Commands. The system collects trending topics, generates multi-platform copy, and produces accompanying image and video assets.

## Stack

- Python, Node.js
- Claude Code CLI (Skills + Slash Commands)
- Feishu Bitable (content database)
- Image/video asset generation integrations

## Concepts

**Skills** — reusable Claude Code skill files that encapsulate a repeatable operation (e.g., `fetch-trends`, `write-copy`, `render-card`).

**Slash Commands** — operator-facing commands that chain skills into a named workflow (e.g., `/daily-run`, `/publish-batch`).

## Workflow

```
/daily-run
    └── fetch-trends skill      # aggregates hot topics
         └── write-copy skill   # generates per-platform copy
              └── render-card skill   # produces image assets
                   └── render-video skill  # produces video assets
                        └── notify skill   # posts summary to Lark
```

## Usage

```bash
# Install dependencies
npm install && pip install -r requirements.txt

# Run the daily pipeline
claude /daily-run

# Fetch trends only
claude /fetch-trends --sources weibo,toutiao

# Generate copy for a specific topic
claude /write-copy --topic "AI news" --platforms juejin,zhihu
```

## Structure

```
AI-News-Ops-Framework/
├── .claude/
│   ├── commands/      # slash command definitions
│   └── skills/        # reusable skill files
├── scripts/           # Python utility scripts
├── templates/         # copy and image templates
└── config.yaml
```

## Adding a Skill

Create a markdown file in `.claude/skills/` describing the skill's purpose, inputs, and expected outputs. Claude Code loads all skills in that directory automatically.
