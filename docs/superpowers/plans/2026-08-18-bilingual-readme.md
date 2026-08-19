# Bilingual README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Make `README.md` the English homepage and preserve the current Chinese metadata in a synchronized `README.zh-CN.md`.

**Architecture:** Create the Chinese README from the current metadata-rich README, then translate only prose, headers, and `Method`/`Advantages` cells in the homepage. Validate both files structurally by extracting table rows and comparing all non-language fields.

**Tech Stack:** Markdown, Python standard library validation, Git.

---

### Task 1: Preserve the Chinese README

**Files:**
- Create: `README.zh-CN.md`
- Modify: `README.md`

- [ ] Copy the current Chinese README content into `README.zh-CN.md`, preserving all 138 rows and Chinese metadata.
- [ ] Add `English | 简体中文` links near the top of both files.
- [ ] Confirm the Chinese copy has 84 Training rows and 54 Inference rows.

### Task 2: Translate the English homepage

**Files:**
- Modify: `README.md`

- [ ] Translate title, introduction, contents, section headings, scope notes, table headers, glossary, and every `Method`/`Advantages` cell into concise technical English.
- [ ] Preserve scheduler names, paper titles, affiliations, links, symbols, quantitative claims, and row order exactly.
- [ ] Keep only unavoidable proper nouns and URLs from Chinese-character exceptions.

### Task 3: Validate synchronization

**Files:**
- Modify: none

- [ ] Parse both Markdown tables with a Python script and verify 84 Training plus 54 Inference rows in each file.
- [ ] Compare every corresponding row after excluding only `Method` and `Advantages`; require all other cells to match byte-for-byte.
- [ ] Verify both tables have 12 columns, run `git diff --check`, and inspect the diff for accidental metadata changes.

### Task 4: Commit and update the PR

**Files:**
- Modify: `README.md`, `README.zh-CN.md`

- [ ] Commit the bilingual README changes with a focused message.
- [ ] Push `add-paper-metadata` and confirm PR #2 remains open with a clean merge state.
