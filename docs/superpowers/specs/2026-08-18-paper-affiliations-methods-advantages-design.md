# 论文单位、方法与优点元数据设计

## 目标

为 README 中全部训练和推理调度论文补充作者署名单位、方法和优点三类元数据。当前范围为训练论文 84 篇、推理论文 54 篇，共 138 篇。

## 表格结构

训练表新增三列：

```text
Scheduler | Year | Series | Affiliations | Method | Advantages | Paper | Objective | Heter. | Elastic | AutoML | Code
```

推理表新增三列：

```text
Scheduler | Year | Series | Affiliations | Method | Advantages | Paper | Objective | Batch | Share | Cloud | Source Code
```

`Affiliations` 放在 `Series` 之后，`Method` 和 `Advantages` 紧随其后，保留原有其他字段和行顺序。

## 作者单位规则

- 记录论文发表版本中的作者署名单位，而不是作者当前任职单位。
- 优先读取正式论文 PDF 首页及 affiliation block，其次使用官方 proceedings、出版社页面或会议 presentation 页面。
- 使用英文机构名称，删除院系、邮政地址等不影响识别的下级信息。
- 同一机构在一篇论文中只保留一次，按论文中的首次出现顺序排列。
- 多个机构使用 `<br>` 分隔。
- 保留可识别的公司或研究机构主体，如 `Microsoft Research`、`Alibaba Cloud`、`ByteDance`。
- 作者同时署名多个机构时，所有署名机构都应纳入。
- 不能从可靠来源确认时填 `-`，不根据作者主页或搜索摘要猜测。

## 方法与优点规则

- 调度器名称保持原文，不附加综述参考文献编号。
- `Method` 和 `Advantages` 使用中文，采用简洁技术短语。
- 多个短语使用中文分号 `；` 分隔。
- 方法描述调度器的核心机制，而不是复述问题背景。
- 优点只记录论文目标、设计论证或实验结果明确支持的收益。
- 不写“先进”“高效”等没有比较对象或证据的宣传性描述。
- 用户提供的训练调度器汇总表作为初始输入，仍需和仓库链接对应的论文核对。
- README 中未被用户汇总表覆盖的训练论文、全部推理论文及 2025–2026 新论文，需要根据正式论文补齐。

## 术语约定

- Job Completion Time：作业完成时间（JCT）
- Service-Level Objective：服务等级目标（SLO）
- Goodput：有效吞吐量
- Gang Scheduling：协同调度
- Placement：放置
- Autoscaling：自动扩缩容
- Colocation：共置
- Preemption：抢占
- Model Parallelism：模型并行
- Pipeline Parallelism：流水线并行

## 证据记录

新增 `docs/paper-metadata-sources.md`，按论文记录：

- 调度器名称和年份；
- 作者单位依据；
- 方法与优点依据；
- 核验状态或歧义说明。

README 保持面向读者的精简展示，证据记录面向维护者。正式论文链接本身能同时支持三类字段时，可以复用该链接；如使用不同来源，应在证据记录中列出。

## 分批执行

1. 训练论文 2017–2020。
2. 训练论文 2021–2024。
3. 训练论文 2025–2026。
4. 推理论文 2016–2021。
5. 推理论文 2022–2024。
6. 推理论文 2025–2026。
7. 全表术语统一、机构去重和证据检查。
8. Markdown 列数、链接及最终差异验证。

## 验收标准

- 两张表中的 138 篇论文均具有三个新增字段。
- 每个非 `-` 的单位、方法和优点都可追溯到论文或官方来源。
- 单位名称使用发表时信息，并在单篇论文内去重。
- 方法和优点为中文，术语在两张表中保持一致。
- 表格每行列数正确，既有字段、链接和行顺序不被无关修改。
- 无法确认的内容明确标记为 `-`，不存在推测性填充。
