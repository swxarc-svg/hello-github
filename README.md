# PhD Research Wiki — Quick Start Guide
# 博士科研 Wiki — 快速上手指南

---

## What is this? / 這是什麼？

This is an LLM-maintained knowledge base for your PhD dissertation research, following Andrej Karpathy's LLM Wiki pattern. You never write the wiki yourself — Claude does all the summarising, cross-referencing, and maintenance. You direct the research.

這是一個由 LLM 維護的博士論文知識庫，基於 Karpathy 的 LLM Wiki 模式。你不需要自己寫 wiki — Claude 負責所有的總結、交叉引用和維護工作。你負責引導研究方向。

---

## Setup steps / 搭建步驟

### 1. Install tools / 安裝工具

- **Obsidian** — https://obsidian.md (free)
  - Open the `wiki/` folder as an Obsidian vault
  - 把 `wiki/` 文件夾作為 Obsidian vault 打開

- **Obsidian Web Clipper** — browser extension
  - For clipping web articles directly to `raw/articles/`
  - 用於把網頁文章直接存到 `raw/articles/`

- **Zotero + Better BibTeX** — https://zotero.org
  - Install Better BibTeX plugin
  - Set auto-export to `raw/zotero-library.bib`
  - 安裝 Better BibTeX 插件，設置自動導出到 `raw/zotero-library.bib`

- **Claude Code** (or Claude Desktop with Code tab)
  - Navigate to `phd-wiki/` folder and start a session
  - 打開 `phd-wiki/` 文件夾，開始一個 session

### 2. Configure Obsidian / 配置 Obsidian

Open Obsidian, then:
1. Open `wiki/` as a vault
2. Install recommended plugins:
   - **Dataview** — for dynamic queries over frontmatter
   - **Marp Slides** — for generating presentations from wiki content
   - **Templater** — (optional) for custom templates
   - **Calendar** — (optional) for log.md navigation
3. The `.obsidian/app.json` is pre-configured to save attachments to `raw/assets/`

### 3. Configure Zotero / 配置 Zotero

1. Install Better BibTeX: https://retorque.re/zotero-better-bibtex/
2. Right-click your library → Export Library → Better BibLaTeX
3. Check "Keep updated"
4. Save to `phd-wiki/raw/zotero-library.bib`

Now every paper you add to Zotero will automatically appear in the .bib file.
現在你每次在 Zotero 加論文，.bib 文件會自動更新。

### 4. Initialize git / 初始化 Git

```bash
cd phd-wiki
git init
git add .
git commit -m "Initial wiki setup"
```

This gives you version history. Commit after each major ingest session.
這樣你就有了版本歷史。每次大的 ingest session 後 commit 一次。

---

## Daily workflow / 日常工作流

### Adding a new paper / 加入新論文

1. Add the PDF to Zotero (auto-syncs to .bib)
2. Copy the PDF to `raw/papers/`
3. Open Claude Code in `phd-wiki/`
4. Say: **"Ingest this new paper: raw/papers/filename.pdf"**
5. Claude reads it, creates wiki pages, updates cross-references
6. Browse results in Obsidian

### Asking research questions / 問研究問題

In Claude Code:
- "What methods have been used to evaluate thermal comfort in shading studies?"
- "Compare fixed canopy vs retractable shading based on all ingested sources"
- "What are the research gaps in typhoon-resistant lightweight structures?"
- "Draft a literature review section on CFD simulation methods for urban wind"

Claude searches the wiki, synthesises an answer, and offers to file it back.

### Maintenance / 維護

Periodically ask:
- **"Lint the wiki"** — find orphan pages, broken links, stale content
- **"What concepts are mentioned but don't have their own page yet?"**
- **"Are there any contradictions between sources that need attention?"**

---

## Folder structure / 文件夾結構

```
phd-wiki/
├── raw/                    # 原始資料（不可修改）
│   ├── papers/             # PDF 論文
│   ├── articles/           # 網頁文章 (.md)
│   ├── assets/             # 圖片、圖表
│   └── clips/              # 快速筆記、截圖
├── wiki/                   # LLM 維護的知識庫（Obsidian vault）
│   ├── sources/            # 每篇論文一個頁面
│   ├── concepts/           # 概念頁面（CFD、遮陽、抗颱等）
│   ├── entities/           # 人物、機構、項目、標準
│   ├── comparisons/        # 對比分析
│   ├── synthesis/          # 文獻綜述草稿
│   ├── index.md            # 主目錄
│   ├── log.md              # 操作日誌
│   └── overview.md         # 研究全景概覽
└── schema/
    └── CLAUDE.md           # Wiki 操作規則（給 Claude 讀的）
```

---

## Tips / 小技巧

- **Start small**: Ingest 3-5 core papers first. Don't try to dump 100 papers at once.
  先 ingest 3-5 篇核心論文，不要一次倒 100 篇。

- **Stay involved during ingest**: Read Claude's summaries, correct misunderstandings, guide emphasis.
  Ingest 過程中保持參與，讀 Claude 的摘要，糾正誤解，引導重點。

- **File back your explorations**: When a query produces good analysis, save it to the wiki.
  好的分析結果要回存到 wiki，讓知識持續累積。

- **Use Obsidian Graph View**: See the shape of your knowledge — which concepts are dense, which are orphans.
  用 Obsidian 的 Graph View 看知識的形狀。

- **Git commit regularly**: After each session, `git add . && git commit -m "session notes"`.
  每次 session 後記得 git commit。

- **The wiki is yours**: It's just markdown files. You can read them in any editor, grep them, move them.
  Wiki 只是 markdown 文件，任何編輯器都能打開。
