# Claude Paper Skills

A collection of Claude Code skills for academic paper workflow automation — from daily paper discovery to reading notes to web publishing.

## Skills Overview

### daily-papers
Automated daily paper recommendation pipeline:
- Fetch trending papers from HuggingFace Daily Papers and arXiv
- Score and filter by configurable keywords and research interests
- Generate opinionated reviews with triage tables (must-read / worth-reading / skip)
- Save as Obsidian-compatible Markdown

### paper-reader
Deep paper reading and note generation:
- Read papers from arXiv URL or local PDF
- Generate structured reading notes with method details, formulas, and critical analysis
- Zotero integration support
- Download and embed paper figures

### daily-papers-web
Static site generator for paper recommendations:
- Convert daily recommendation Markdown files to a browsable HTML site
- Dashboard with calendar, topic trends, and quality timeline
- Topic-based filtering across all dates
- Collapsible detailed reading notes with KaTeX formula rendering
- GitHub Pages deployment

### generate-mocs
Generate Map of Content (MOC) index pages for Obsidian:
- Auto-generate paper index and concept index pages
- Organize by tags, venues, and categories

### _shared
Shared configuration and utilities:
- `user-config.json` — paths, keywords, web settings
- `user_config.py` — config loader used by all skills

## Setup

1. Place this directory under `~/.claude/skills/`
2. Edit `_shared/user-config.json` to configure your Obsidian vault path, research keywords, and GitHub Pages settings
3. Skills are automatically available in Claude Code

## Usage

In Claude Code, use natural language or slash commands:
- "今日论文推荐" / `/daily-papers` — run the full paper recommendation pipeline
- "读论文 [URL]" / `/paper-reader` — deep read a specific paper
- "发布论文网页" / `/daily-papers-web` — generate and deploy the web site
- "更新索引" / `/generate-mocs` — regenerate MOC pages

## License

MIT
