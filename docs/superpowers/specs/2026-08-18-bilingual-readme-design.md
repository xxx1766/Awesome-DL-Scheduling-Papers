# Bilingual README Design

## Goal

Make the repository homepage English-first while preserving the current Chinese metadata as a separate, synchronized README.

## Files

- `README.md`: English homepage.
- `README.zh-CN.md`: Chinese version preserving the current Chinese methods and advantages.
- `docs/paper-metadata-sources.md`: One shared English maintenance and evidence record; do not duplicate it.

## Content rules

- Keep the 138 paper rows, row order, scheduler names, years, series, affiliations, paper links, objective symbols, capability flags, and code links identical between the two README files.
- Translate the README title, introduction, table of contents, section headings, update-scope notes, table headers, glossary labels, `Method`, and `Advantages` in `README.md`.
- Preserve the current Chinese `Method` and `Advantages` text in `README.zh-CN.md`; do not rewrite or retranslate those cells.
- Keep affiliation names, scheduler names, venue names, URLs, symbols, and code links unchanged unless a validation check finds an existing defect.
- Add `English | 简体中文` language links near the top of both files. The English link points to `README.md`; the Chinese link points to `README.zh-CN.md`.

## Translation rules for the English homepage

- Use concise technical English rather than literal word-for-word translations.
- Preserve established abbreviations and explain them once in the English glossary or scope note: JCT, SLO, GPU, LLM, RL, QoS, and KV cache.
- Translate repeated terms consistently:
  - 作业完成时间（JCT） → job completion time (JCT)
  - 服务等级目标（SLO） → service-level objective (SLO)
  - 有效吞吐量 → effective throughput
  - 自动扩缩容 → autoscaling
  - 抢占 → preemption
  - 共置 → colocation
  - 放置 → placement
  - 模型并行 → model parallelism
  - 流水线并行 → pipeline parallelism
- Do not translate proper nouns, scheduler names, institution names, venue names, paper titles, or repository names.
- Keep quantitative claims, experimental boundaries, comparison baselines, and units unchanged in meaning.

## Validation

- Verify that both README files contain 84 training rows and 54 inference rows.
- Verify that each corresponding row has identical non-language metadata and links.
- Verify that the English file contains no Chinese characters in its translated prose or `Method`/`Advantages` cells, except unavoidable proper nouns or URLs.
- Verify that the Chinese file retains the current Chinese method and advantage cells.
- Verify all table rows have the same 12-column structure as the current README.
- Run `git diff --check` and inspect the complete diff for accidental changes to paper metadata.
