# Paper Metadata Enrichment Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add verified affiliations, Chinese method summaries, and Chinese advantage summaries to all 138 training and inference scheduler rows in README.

**Architecture:** Research metadata in six year-based batches, recording evidence before changing the presentation table. Use the paper or official proceedings as the primary source, normalize affiliations and terminology centrally, and apply table changes only after each batch passes coverage and format checks.

**Tech Stack:** Markdown, official paper PDFs/proceedings, conference and publisher pages, Python read-only validation scripts, git.

---

### Task 1: Add the table schema and evidence document

**Files:**
- Modify: `README.md`
- Create: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Add the three headers to the training table**

  Insert `Affiliations`, `Method`, and `Advantages` after `Series`, and add three placeholder cells to every training row. Do not alter existing values or row order.

- [ ] **Step 2: Add the three headers to the inference table**

  Apply the same schema change to the inference table and add three placeholder cells to every inference row.

- [ ] **Step 3: Create the evidence record**

  Add sections for the six research batches. Each paper entry must use this form:

  ```markdown
  ### Scheduler (YEAR)

  - Affiliations: Institution A; Institution B
  - Affiliations source: URL
  - Method: 中文方法短语
  - Advantages: 中文优点短语
  - Method/advantages source: URL
  - Verification: confirmed
  ```

- [ ] **Step 4: Validate placeholder coverage**

  Run a Python check that finds the two scheduler tables, verifies that every paper row contains 12 cells, and reports `training=84`, `inference=54`.

- [ ] **Step 5: Commit the schema**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add paper metadata columns"
  ```

### Task 2: Research training papers from 2017–2020

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Map the user-provided summaries to README rows**

  Match scheduler names without survey reference numbers. Treat spelling differences such as `Gandivafair` and `GandivaFair` as aliases only after checking the linked paper.

- [ ] **Step 2: Verify affiliations**

  For every training row dated 2017–2020, read the linked paper's author-affiliation block and record deduplicated institution names in first-appearance order.

- [ ] **Step 3: Verify methods and advantages**

  Compare the supplied Chinese summary with each paper's abstract, system overview, and evaluation claims. Correct mistranslations or unsupported benefits before recording the fields.

- [ ] **Step 4: Fill README and evidence entries**

  Replace all three placeholders for the batch. Use `<br>` between affiliations and `；` between Chinese method or advantage phrases.

- [ ] **Step 5: Check batch completeness**

  Verify that no 2017–2020 training row retains a placeholder and that every row has one matching evidence entry.

- [ ] **Step 6: Commit the batch**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add 2017-2020 training paper metadata"
  ```

### Task 3: Research training papers from 2021–2024

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Map the supplied training summaries**

  Remove survey citation numbers and align the supplied scheduler names with the README paper links.

- [ ] **Step 2: Verify affiliations from publication-time sources**

  Record every institution shown in each paper's affiliation block, excluding departments and addresses while retaining distinct universities, companies, and research institutes.

- [ ] **Step 3: Verify Chinese methods and advantages**

  Check each supplied phrase against the paper. Preserve established terms such as `有效吞吐量`, `服务等级目标（SLO）`, and `作业完成时间（JCT）`.

- [ ] **Step 4: Research training rows missing from the supplied table**

  Derive concise method and advantage phrases from the paper's design and evaluation, using `-` only when a reliable source is unavailable.

- [ ] **Step 5: Fill README and evidence entries**

  Complete the three new cells and one evidence entry for every 2021–2024 training paper.

- [ ] **Step 6: Validate and commit**

  Confirm complete year coverage and 12-cell rows, then commit:

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add 2021-2024 training paper metadata"
  ```

### Task 4: Research training papers from 2025–2026

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Verify the seven new training papers**

  Use OSDI, NSDI, ASPLOS, MLSys, and EuroSys official pages and PDFs to verify publication-time affiliations.

- [ ] **Step 2: Summarize methods**

  Describe each scheduler's core mechanism, including cluster heterogeneity handling, co-scheduling, rollout packing, preemption-aware placement, resource allocation, or elastic training as applicable.

- [ ] **Step 3: Summarize evidence-backed advantages**

  Record only benefits supported by the paper, such as utilization, cost, JCT, fairness, or accuracy preservation.

- [ ] **Step 4: Fill README and evidence entries**

  Complete all 2025–2026 training rows with source records.

- [ ] **Step 5: Validate and commit**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add 2025-2026 training paper metadata"
  ```

### Task 5: Research inference papers from 2016–2021

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Verify affiliations for each inference paper**

  Read publication-time affiliations from the linked paper or official proceedings. Do not infer affiliations from current author profiles.

- [ ] **Step 2: Derive Chinese method summaries**

  Identify the scheduling mechanism, such as batching, model placement, caching, GPU sharing, routing, autoscaling, or interference-aware scheduling.

- [ ] **Step 3: Derive Chinese advantages**

  Summarize demonstrated improvements in throughput, latency, utilization, cost, or accuracy.

- [ ] **Step 4: Fill README and evidence entries**

  Complete every inference row dated 2016–2021.

- [ ] **Step 5: Validate and commit**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add 2016-2021 inference paper metadata"
  ```

### Task 6: Research inference papers from 2022–2024

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Verify publication-time affiliations**

  Record normalized, deduplicated affiliations from papers or official proceedings.

- [ ] **Step 2: Derive methods and advantages**

  Cover LLM serving mechanisms such as continuous batching, KV-cache management, disaggregation, heterogeneous placement, speculative execution, request routing, and spot-instance handling where supported.

- [ ] **Step 3: Fill README and evidence entries**

  Complete all inference rows dated 2022–2024 and add matching source records.

- [ ] **Step 4: Validate and commit**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add 2022-2024 inference paper metadata"
  ```

### Task 7: Research inference papers from 2025–2026

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Verify the twelve new inference papers**

  Use OSDI, NSDI, ASPLOS, and MLSys official sources to confirm affiliations and system identity.

- [ ] **Step 2: Summarize methods and advantages**

  Distinguish request scheduling, GPU sharing, model placement, elastic serving, heterogeneous serving, resource disaggregation, and inference/finetuning co-serving.

- [ ] **Step 3: Fill README and evidence entries**

  Complete the three metadata cells and evidence record for every 2025–2026 inference row.

- [ ] **Step 4: Validate and commit**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: add 2025-2026 inference paper metadata"
  ```

### Task 8: Normalize and verify all metadata

**Files:**
- Modify: `README.md`
- Modify: `docs/paper-metadata-sources.md`

- [ ] **Step 1: Normalize affiliation names**

  Merge spelling variants within a paper, remove department/address suffixes, preserve publication-time institution names, and keep first-appearance order.

- [ ] **Step 2: Normalize Chinese terminology**

  Apply the terminology specified in the design document consistently across both tables.

- [ ] **Step 3: Verify coverage**

  Run a Python check that asserts:

  - training rows: 84;
  - inference rows: 54;
  - every paper row: 12 cells;
  - every row has non-empty `Affiliations`, `Method`, and `Advantages` cells;
  - every row has exactly one evidence heading.

- [ ] **Step 4: Verify Markdown and links**

  Run `git diff --check`, inspect the rendered table structure, and check every newly added evidence URL.

- [ ] **Step 5: Conduct independent review**

  Review for wrong-paper matches, current-vs-publication affiliation mistakes, unsupported advantages, terminology inconsistency, and table corruption.

- [ ] **Step 6: Apply review fixes**

  Correct every Critical or Important issue and rerun all coverage and format checks.

- [ ] **Step 7: Commit final normalization**

  ```bash
  git add README.md docs/paper-metadata-sources.md
  git commit -m "docs: normalize and verify paper metadata"
  ```

### Task 9: Final branch verification and PR

**Files:**
- Verify: `README.md`
- Verify: `docs/paper-metadata-sources.md`
- Verify: `docs/superpowers/specs/2026-08-18-paper-affiliations-methods-advantages-design.md`

- [ ] **Step 1: Verify branch state**

  Confirm the branch is based on the latest `origin/master`, the worktree is clean, and only intended documentation files changed.

- [ ] **Step 2: Review the complete diff**

  Check table headers, all 138 rows, evidence records, terminology, and absence of unrelated edits.

- [ ] **Step 3: Push the branch**

  ```bash
  git push -u origin add-paper-metadata
  ```

- [ ] **Step 4: Create the pull request**

  Create a PR targeting `master` with counts, source policy, verification results, and unresolved `-` fields in the description.
