# Paper Metadata Sources

This file records the evidence used for the `Affiliations`, `Method`, and
`Advantages` columns in `README.md`. Task 1 establishes the record structure
only; no paper metadata is asserted here until it has been verified from a
reliable publication-time source.

## Evidence record template

Create one entry per paper using the following form:

```markdown
### Scheduler (YEAR)

- Affiliations: Institution A; Institution B
- Affiliations source: URL
- Method: 中文方法短语
- Advantages: 中文优点短语
- Method/advantages source: URL
- Verification: confirmed
```

Use the paper or official proceedings as the primary source. Record
publication-time affiliations, normalize institution names without guessing,
and use `-` when a field cannot be confirmed. Keep source URLs attached to the
specific claims they support. `Verification` should state `confirmed` only
after the affiliation, method, and advantages claims have each been checked;
otherwise record the unresolved ambiguity instead of filling it speculatively.

## Batch 1: Training papers, 2017–2020

The README contains 37 rows in this batch. The linked records, rather than
survey names, were used for matching.

### GENIE (2020)
- Affiliations: National University of Defense Technology
- Affiliations source: https://www.computer.org/csdl/journal/td/2020/01/08778770/1fPUi51S3ny
- Method: 轻量级剖析建模；QoS 感知动态放置
- Advantages: 提高 QoS 保证和系统利用率
- Method/advantages source: https://jianbinfang.github.io/files/2019-07-29-tpds.pdf
- Verification: confirmed

### Parrot (2020)
- Affiliations: Hong Kong University of Science and Technology; Tianjin University; Dalian University of Technology
- Affiliations source: http://cic.tju.edu.cn/faculty/liwenxin/pdf/efficient_online_tcc20.pdf
- Method: LPCAS 推断 SRPT 作业；动态作业权重与 LP 加权带宽缩放分配
- Advantages: 提高依赖 coflow 的通信调度效率，较 Aalo 最多降低 58.4% 总 JCT
- Method/advantages source: https://ieeexplore.ieee.org/document/9269382
- Verification: confirmed against the formal TCC paper, "Efficient Online Scheduling for Coflow-Aware Machine Learning Clusters" (DOI 10.1109/TCC.2020.3040312); publication-time affiliations follow the paper's author footnotes.

### Non-Intrusive (2020)
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/abs/10.5555/3433701.3433820
- Method: -
- Advantages: -
- Method/advantages source: https://dl.acm.org/doi/abs/10.5555/3433701.3433820
- Verification: unresolved: the linked DOI resolves to a record whose publication-time affiliation block could not be reliably retrieved.

### Antman (2020)
- Affiliations: Alibaba
- Affiliations source: https://www.usenix.org/system/files/osdi20-xiao.pdf
- Method: 动态显存扩缩容；机会计算共置
- Advantages: 提高 GPU 显存和计算单元利用率
- Method/advantages source: https://www.usenix.org/system/files/osdi20-xiao.pdf
- Verification: confirmed

### Gavel (2020)
- Affiliations: Stanford University; Microsoft Research
- Affiliations source: https://deepakn94.github.io/assets/papers/gavel-osdi20.pdf
- Method: 有效吞吐量建模；异构感知优化分配
- Advantages: 提高负载承载量；降低 JCT 和 makespan
- Method/advantages source: https://www.usenix.org/conference/osdi20/presentation/narayanan-deepak
- Verification: confirmed

### HiveD (2020)
- Affiliations: Peking University; Microsoft; The University of Hong Kong
- Affiliations source: https://www.usenix.org/system/files/osdi20-zhao_hanyu.pdf
- Method: 多级 GPU 亲和单元；虚拟私有集群
- Advantages: 提供共享安全保证；支持生产集群长期运行
- Method/advantages source: https://www.usenix.org/system/files/osdi20-zhao_hanyu.pdf
- Verification: confirmed

### Themis (2020)
- Affiliations: University of Wisconsin–Madison; Microsoft Research
- Affiliations source: https://wisr.cs.wisc.edu/papers/nsdi20-themis.pdf
- Method: 完工时间公平；两级拍卖调度
- Advantages: 提高公平性和集群效率
- Method/advantages source: https://www.usenix.org/conference/nsdi20/presentation/mahajan
- Verification: confirmed

### Salus (2020)
- Affiliations: University of Michigan
- Affiliations source: https://symbioticlab.org/publications/files/salus:mlsys20/salus-mlsys20.pdf
- Method: 快速作业切换；显存共享
- Advantages: 支持细粒度 GPU 共享并提高利用率
- Method/advantages source: https://proceedings.mlsys.org/paper_files/paper/2020/hash/d9cd83bc91b8c36a0c7c0fcca59228f2-Abstract.html
- Verification: confirmed

### Vaibhav et al. (2020)
- Affiliations: IBM Research
- Affiliations source: https://research.ibm.com/publications/effective-elastic-scaling-of-deep-learning-workloads
- Method: 动态批大小与资源联合扩缩容
- Advantages: 改善作业运行时间和集群利用率
- Method/advantages source: https://research.ibm.com/publications/effective-elastic-scaling-of-deep-learning-workloads
- Verification: confirmed

### SPIN (2020)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9155445/
- Method: 通信争用感知的作业调度
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9155445/
- Verification: unresolved: official page was reachable but its publication-time affiliation block and evaluation claims were not reliably extractable.

### E-LAS (2020)
- Affiliations: University of Louisiana at Lafayette
- Affiliations source: https://dl.acm.org/doi/fullHtml/10.1145/3404397.3404415
- Method: 基于实时 epoch 进度的完成时间无关调度
- Advantages: 提高训练吞吐量并降低平均完成时间
- Method/advantages source: https://dl.acm.org/doi/fullHtml/10.1145/3404397.3404415
- Verification: confirmed for method and advantage; affiliation normalized from the publication record.

### CODA (2020)
- Affiliations: Shanghai Jiao Tong University; China University of Geosciences
- Affiliations source: https://www.proceedings.com/content/057/057955webtoc.pdf
- Method: CPU 资源反馈分配；争用消除；多阵列调度
- Advantages: 提高 GPU 利用率且不增加 CPU 作业排队时间
- Method/advantages source: https://cs.sjtu.edu.cn/~leng-jw/resources/Files/zhao20icdcs-coda.pdf
- Verification: confirmed

### Elan (2020)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9355755
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9355755
- Verification: unresolved: the cited arXiv survey is not the Elan paper, so secondary method and advantage claims were removed; the official IEEE record did not expose enough publication text to verify them.

### Yeung (2020)
- Affiliations: University of Leeds
- Affiliations source: https://www.usenix.org/conference/hotcloud20/presentation/yeung
- Method: 基于计算图的 GPU 利用率预测
- Advantages: 无需隔离式在线剖析即可预测利用率
- Method/advantages source: https://www.usenix.org/conference/hotcloud20/presentation/yeung
- Verification: confirmed

### $Gandiva_{fair}$ (2020)
- Affiliations: Microsoft Research India
- Affiliations source: https://www.microsoft.com/en-us/research/wp-content/uploads/2020/05/gandiva-eurosys20.pdf
- Method: Kubernetes 上的异构 GPU 公平共享与资源交易
- Advantages: 在保证用户级 GPU 时间公平的同时提高集群效率和作业进度
- Method/advantages source: https://www.microsoft.com/en-us/research/wp-content/uploads/2020/05/gandiva-eurosys20.pdf
- Verification: confirmed from the EuroSys paper; the PDF identifies all authors with Microsoft Research India and states the fairness, efficiency, and trading benefits.

### MLCloudPrice (2020)
- Affiliations: Stanford University; Microsoft Research
- Affiliations source: https://deepakn94.github.io/assets/papers/trainingonadime-dispa20.pdf
- Method: 跨区域、市场和云实例的动态价格优化
- Advantages: 降低训练成本；支持速度成本权衡
- Method/advantages source: https://deepakn94.github.io/assets/papers/trainingonadime-dispa20.pdf
- Verification: confirmed

### MLFS (2020)
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/10.1145/3386367.3432588
- Method: 基于作业特征的并行度感知调度
- Advantages: 降低 JCT 和 makespan
- Method/advantages source: https://dl.acm.org/doi/10.1145/3386367.3432588
- Verification: unresolved affiliation: the ACM record confirms the paper identity, but a publication-time affiliation block was not reliably retrievable.

### MARBLE (2020)
- Affiliations: Oak Ridge National Laboratory; Virginia Tech
- Affiliations source: https://people.cs.vt.edu/~butta/docs/ccgrid2020-MARBLE.pdf
- Method: 多 GPU 节点非线性扩展建模与共享调度
- Advantages: 改善训练性能并降低 JCT
- Method/advantages source: https://research.ibm.com/publications/marble-a-multi-gpu-aware-job-scheduler-for-deep-learning-on-hpc-systems
- Verification: confirmed

### Ada-SRSF (2020)
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2002.10105
- Method: 通信争用感知的放置与最短剩余服务时间调度
- Advantages: 相比无争用或盲目接受争用的策略降低平均 JCT 并提高资源利用率
- Method/advantages source: https://arxiv.org/abs/2002.10105
- Verification: method and advantage confirmed in the original paper, which names Ada-SRSF as the scheduling algorithm; publication-time affiliation was not reliably extractable.

### Co-scheML (2020)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9196380
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9196380
- Verification: unresolved: the IEEE record did not provide a reliably confirmable publication-time affiliation block or claim text.

### HyperSched (2019)
- Affiliations: University of California, Berkeley
- Affiliations source: https://dl.acm.org/doi/10.1145/3357223.3362719
- Method: 截止期驱动的动态资源再分配
- Advantages: 提高截止期内完成率和资源利用率
- Method/advantages source: https://dl.acm.org/doi/10.1145/3357223.3362719
- Verification: confirmed

### Tiresias (2019)
- Affiliations: University of Michigan; Microsoft Research
- Affiliations source: https://www.usenix.org/system/files/nsdi19-gu.pdf
- Method: 预估 JCT 的短作业优先与离散分配
- Advantages: 降低平均 JCT
- Method/advantages source: https://www.usenix.org/conference/nsdi19/presentation/gu
- Verification: confirmed

### FfDL (2019)
- Affiliations: IBM Research
- Affiliations source: https://dl.acm.org/doi/10.1145/3361525.3361538
- Method: 容器化深度学习服务编排与资源调度
- Advantages: 提供多框架训练服务
- Method/advantages source: https://dl.acm.org/doi/10.1145/3361525.3361538
- Verification: confirmed

### JPAS (2019)
- Affiliations: -
- Affiliations source: https://www.sciencedirect.com/science/article/abs/pii/S1084804520300643
- Method: MAIF 作业进度感知的流优先级调度
- Advantages: 加速分布式训练早期阶段的探索过程
- Method/advantages source: https://www.sciencedirect.com/science/article/abs/pii/S1084804520300643
- Verification: method and advantage confirmed from the official ScienceDirect abstract; publication-time affiliation was not reliably available.

### Harmony (2019)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/8737460
- Method: 基于奖励建模的深度强化学习干扰感知放置
- Advantages: 降低平均 JCT
- Method/advantages source: https://ieeexplore.ieee.org/document/8737460
- Verification: method and advantage confirmed from the official IEEE paper record; affiliation was not exposed reliably.

### Cynthia (2019)
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/10.1145/3337821.3337873
- Method: 轻量级分析模型驱动的云资源配置
- Advantages: 提供可预测训练性能并降低训练预算
- Method/advantages source: https://dl.acm.org/doi/10.1145/3337821.3337873
- Verification: method and advantage confirmed from the official ACM record; the MDPI URL was a Hermes paper and is not used; affiliation was not reliably available.

### Jahani (2019)
- Affiliations: Politecnico di Milano
- Affiliations source: https://ieeexplore.ieee.org/document/8888151
- Method: MILP 全局优化 GPU 租赁与作业延迟
- Advantages: 降低租赁成本并维持作业时延
- Method/advantages source: https://ieeexplore.ieee.org/document/8888151
- Verification: confirmed

### $Sched^2$ (2019)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9014110
- Method: 深度强化学习驱动的局部性感知训练调度
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9014110
- Verification: method confirmed from the formal IEEE paper record; affiliation and advantage were not reliably extractable.

### Dragon (2019)
- Affiliations: -
- Affiliations source: https://closer.scitevents.org/Abstract.aspx?idEvent=uzu18usNf68%3D
- Method: Kubernetes 集群上的分布式训练作业动态调度与扩缩容
- Advantages: -
- Method/advantages source: https://closer.scitevents.org/Abstract.aspx?idEvent=uzu18usNf68%3D
- Verification: method confirmed by the official CLOSER paper record; the prior National Taiwan University affiliation and speed claim came from a secondary copy and were removed.

### $FC^2$ (2019)
- Affiliations: -
- Affiliations source: https://link.springer.com/article/10.1007/s10586-019-02912-6
- Method: 云端集群自动配置与参数服务器资源规划
- Advantages: 降低云资源成本并保持训练性能
- Method/advantages source: https://link.springer.com/article/10.1007/s10586-019-02912-6
- Verification: method and advantage confirmed against the formal Cluster Computing paper record; affiliation was not reliably extractable.

### Philly (2019)
- Affiliations: UNIST; University of Wisconsin; Microsoft Research; Beihang University
- Affiliations source: https://www.usenix.org/system/files/atc19-jeon.pdf
- Method: 生产多租户 GPU 集群工作负载分析与调度追踪
- Advantages: 揭示 gang 调度、本地性和故障对集群利用率的影响并给出调度设计指导
- Method/advantages source: https://www.usenix.org/conference/atc19/presentation/jeon
- Verification: confirmed against the README-linked Philly/ATC publication; the prior five-institution list belonged to Gandiva and was removed.

### Gandiva (2018)
- Affiliations: Beihang University; Microsoft Research; The University of Hong Kong; Huazhong University of Science and Technology; Peking University
- Affiliations source: https://www.usenix.org/system/files/osdi18-xiao.pdf
- Method: 运行时剖析；可抢占迭代级 GPU 调度
- Advantages: 提高 GPU 利用率和作业吞吐
- Method/advantages source: https://www.usenix.org/conference/osdi18/presentation/xiao
- Verification: confirmed

### OASiS (2018)
- Affiliations: The University of Hong Kong; University of Calgary
- Affiliations source: https://i.cs.hku.hk/~cwu/papers/yxbao-infocom18.pdf
- Method: 原始-对偶在线调度；联合决定 worker 与 parameter server 数量
- Advantages: 提高共享集群总体效用并改善训练完成时间
- Method/advantages source: https://i.cs.hku.hk/~cwu/papers/yxbao-infocom18.pdf
- Verification: confirmed against the original paper PDF for the IEEE INFOCOM publication linked by README.

### Optimus (2018)
- Affiliations: The University of Hong Kong; ByteDance
- Affiliations source: https://i.cs.hku.hk/~cwu/papers/yhpeng-eurosys18.pdf
- Method: 基于性能模型的动态资源调度
- Advantages: 提高集群利用率并降低 JCT
- Method/advantages source: https://i.cs.hku.hk/~cwu/papers/yhpeng-eurosys18.pdf
- Verification: confirmed

### Dorm (2017)
- Affiliations: -
- Affiliations source: https://www.computer.org/csdl/proceedings-article/smartcomp/2017/07947053/12OmNAlvHZ3
- Method: 容器化动态划分集群；运行时调整应用分区
- Advantages: 兼顾共享集群的资源效率与公平性
- Method/advantages source: https://arxiv.org/abs/1704.06738
- Verification: method and advantage confirmed against the authors' original paper version; publication-time affiliation was not reliably extractable from the linked proceedings record.

### Topology-Aware (2017)
- Affiliations: Barcelona Supercomputing Center; Universitat Politècnica de Catalunya; IBM Watson Research Center
- Affiliations source: https://upcommons.upc.edu/bitstreams/6244943d-5795-4c80-b2ac-222d1f1dc355/download
- Method: 拓扑感知多 GPU 放置
- Advantages: 提高资源利用率和执行性能
- Method/advantages source: https://research.ibm.com/publications/topology-aware-gpu-scheduling-for-learning-workloads-in-cloud-environments
- Verification: confirmed

### HyperDrive (2017)
- Affiliations: Brown University; Microsoft; University of Nevada, Reno
- Affiliations source: https://www2.cs.uh.edu/~fyan/Paper/Middleware17.pdf
- Method: POP 调度下的超参数探索
- Advantages: 提高超参数搜索吞吐量
- Method/advantages source: https://www2.cs.uh.edu/~fyan/Paper/Middleware17.pdf
- Verification: confirmed

## Batch 2: Training papers, 2021–2024

No paper evidence has been recorded yet.

## Batch 3: Training papers, 2025–2026

No paper evidence has been recorded yet.

## Batch 4: Inference papers, 2016–2021

No paper evidence has been recorded yet.

## Batch 5: Inference papers, 2022–2024

No paper evidence has been recorded yet.

## Batch 6: Inference papers, 2025–2026

No paper evidence has been recorded yet.
