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
- Paper title: Full paper title
- DOI: https://doi.org/...
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
- Paper title: Characterizing and Scheduling with QoS Guarantees on GPU Clusters
- DOI: -
- Method: 轻量级剖析建模；QoS 感知动态放置
- Advantages: 提高 QoS 保证和系统利用率
- Method/advantages source: https://jianbinfang.github.io/files/2019-07-29-tpds.pdf
- Verification: confirmed

### Parrot (2020)
- Affiliations: Hong Kong University of Science and Technology; Tianjin University; Dalian University of Technology
- Affiliations source: https://doi.org/10.1109/TCC.2020.3040312 (DOI is the identity anchor; the publication record is the source for the affiliation block.)
- Paper title: Efficient Online Scheduling for Coflow-Aware Machine Learning Clusters
- DOI: https://doi.org/10.1109/TCC.2020.3040312
- Paper title: Efficient Online Scheduling for Coflow-Aware Machine Learning Clusters
- DOI: https://doi.org/10.1109/TCC.2020.3040312
- Method: LPCAS 推断 SRPT 作业；动态作业权重与 LP 加权带宽缩放分配
- Advantages: 降低依赖 coflow 作业的总 JCT；在基于 Microsoft workload 的大规模 trace-driven 仿真中，较 Aalo 最多降低总 JCT 58.4%
- Method/advantages source: https://ieeexplore.ieee.org/document/9269382
- Verification: confirmed against the formal TCC paper, "Efficient Online Scheduling for Coflow-Aware Machine Learning Clusters" (online publication: 2020; IEEE Transactions on Cloud Computing, Volume 10, Issue 4, 2022; DOI 10.1109/TCC.2020.3040312); publication-time affiliations follow the paper's author footnotes.

### Non-Intrusive (2020)
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/abs/10.5555/3433701.3433820
- Paper title: An Efficient and Non-Intrusive GPU Scheduling Framework for Deep Learning Training Systems
- DOI: https://doi.org/10.5555/3433701.3433820
- Method: -
- Advantages: -
- Method/advantages source: https://dl.acm.org/doi/abs/10.5555/3433701.3433820
- Verification: unresolved: the linked DOI resolves to a record whose publication-time affiliation block could not be reliably retrieved.

### Antman (2020)
- Affiliations: Alibaba
- Affiliations source: https://www.usenix.org/system/files/osdi20-xiao.pdf
- Paper title: AntMan: Dynamic Scaling on GPU Clusters for Deep Learning
- DOI: -
- Method: 动态显存扩缩容；机会计算共置
- Advantages: 提高 GPU 显存和计算单元利用率
- Method/advantages source: https://www.usenix.org/system/files/osdi20-xiao.pdf
- Verification: confirmed

### Gavel (2020)
- Affiliations: Stanford University; Microsoft Research
- Affiliations source: https://deepakn94.github.io/assets/papers/gavel-osdi20.pdf
- Paper title: Heterogeneity-Aware Cluster Scheduling Policies for Deep Learning Workloads
- DOI: -
- Method: 有效吞吐量建模；异构感知优化分配
- Advantages: 提高负载承载量；降低 JCT 和 makespan
- Method/advantages source: https://www.usenix.org/conference/osdi20/presentation/narayanan-deepak
- Verification: confirmed

### HiveD (2020)
- Affiliations: Peking University; Microsoft; The University of Hong Kong
- Affiliations source: https://www.usenix.org/system/files/osdi20-zhao_hanyu.pdf
- Paper title: HiveD: Sharing a GPU Cluster for Deep Learning with Guarantees
- DOI: -
- Method: 多级 GPU 亲和单元；虚拟私有集群
- Advantages: 提供共享安全保证；支持生产集群长期运行
- Method/advantages source: https://www.usenix.org/system/files/osdi20-zhao_hanyu.pdf
- Verification: confirmed

### Themis (2020)
- Affiliations: University of Wisconsin–Madison; Microsoft Research
- Affiliations source: https://wisr.cs.wisc.edu/papers/nsdi20-themis.pdf
- Paper title: Themis: Fair and Efficient GPU Cluster Scheduling
- DOI: -
- Method: 完工时间公平；两级拍卖调度
- Advantages: 提高公平性和集群效率
- Method/advantages source: https://www.usenix.org/conference/nsdi20/presentation/mahajan
- Verification: confirmed

### Salus (2020)
- Affiliations: University of Michigan
- Affiliations source: https://symbioticlab.org/publications/files/salus:mlsys20/salus-mlsys20.pdf
- Paper title: Salus: Fine-grained GPU Sharing Primitives for Deep Learning Applications
- DOI: -
- Method: 快速作业切换；显存共享
- Advantages: 支持细粒度 GPU 共享并提高利用率
- Method/advantages source: https://proceedings.mlsys.org/paper_files/paper/2020/hash/d9cd83bc91b8c36a0c7c0fcca59228f2-Abstract.html
- Verification: confirmed

### Vaibhav et al. (2020)
- Affiliations: IBM Research
- Affiliations source: https://research.ibm.com/publications/effective-elastic-scaling-of-deep-learning-workloads
- Paper title: Effective Elastic Scaling of Deep Learning Workloads
- DOI: -
- Method: 动态批大小与资源联合扩缩容
- Advantages: 改善作业运行时间和集群利用率
- Method/advantages source: https://research.ibm.com/publications/effective-elastic-scaling-of-deep-learning-workloads
- Verification: confirmed

### SPIN (2020)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9155445/
- Paper title: Communication Contention Aware Scheduling of Multiple Deep Learning Training Jobs
- DOI: -
- Method: 通信争用感知的作业调度
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9155445/
- Verification: unresolved: official page was reachable but its publication-time affiliation block and evaluation claims were not reliably extractable.

### E-LAS (2020)
- Affiliations: University of Louisiana at Lafayette
- Affiliations source: https://dl.acm.org/doi/fullHtml/10.1145/3404397.3404415
- Paper title: E-LAS: Design and Analysis of Completion-Time Agnostic Scheduling for Distributed Deep Learning Cluster
- DOI: https://doi.org/10.1145/3404397.3404415
- Method: 基于实时 epoch 进度的完成时间无关调度
- Advantages: 提高训练吞吐量并降低平均完成时间
- Method/advantages source: https://dl.acm.org/doi/fullHtml/10.1145/3404397.3404415
- Verification: confirmed for method and advantage; affiliation normalized from the publication record.

### CODA (2020)
- Affiliations: Shanghai Jiao Tong University; China University of Geosciences
- Affiliations source: https://www.proceedings.com/content/057/057955webtoc.pdf
- Paper title: CODA: Improving Resource Utilization by Slimming and Co-locating DNN Training Jobs
- DOI: -
- Method: CPU 资源反馈分配；争用消除；多阵列调度
- Advantages: 提高 GPU 利用率且不增加 CPU 作业排队时间
- Method/advantages source: https://cs.sjtu.edu.cn/~leng-jw/resources/Files/zhao20icdcs-coda.pdf
- Verification: confirmed

### Elan (2020)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9355755
- Paper title: Elan: Towards Generic and Efficient Elastic Training for Deep Learning
- DOI: -
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9355755
- Verification: unresolved: the official IEEE record did not expose enough publication text to verify the method, advantages, or publication-time affiliations.

### Yeung (2020)
- Affiliations: University of Leeds
- Affiliations source: https://www.usenix.org/conference/hotcloud20/presentation/yeung
- Paper title: Towards GPU Utilization Prediction for Cloud Deep Learning
- DOI: -
- Method: 基于计算图的 GPU 利用率预测
- Advantages: 无需隔离式在线剖析即可预测利用率
- Method/advantages source: https://www.usenix.org/conference/hotcloud20/presentation/yeung
- Verification: confirmed

### $Gandiva_{fair}$ (2020)
- Affiliations: Microsoft Research India
- Affiliations source: https://www.microsoft.com/en-us/research/wp-content/uploads/2020/05/gandiva-eurosys20.pdf
- Paper title: Balancing Efficiency and Fairness in Heterogeneous GPU Clusters for Deep Learning
- DOI: -
- Method: Kubernetes 上的异构 GPU 公平共享与资源交易
- Advantages: 在保证用户级 GPU 时间公平的同时提高集群效率和作业进度
- Method/advantages source: https://www.microsoft.com/en-us/research/wp-content/uploads/2020/05/gandiva-eurosys20.pdf
- Verification: confirmed from the EuroSys paper; the PDF identifies all authors with Microsoft Research India and states the fairness, efficiency, and trading benefits.

### MLCloudPrice (2020)
- Affiliations: Stanford University; Microsoft Research
- Affiliations source: https://deepakn94.github.io/assets/papers/trainingonadime-dispa20.pdf
- Paper title: Training on a Dime: Cost-Effective Training of Machine Learning Models in the Cloud
- DOI: -
- Method: 跨区域、市场和云实例的动态价格优化
- Advantages: 降低训练成本；支持速度成本权衡
- Method/advantages source: https://deepakn94.github.io/assets/papers/trainingonadime-dispa20.pdf
- Verification: confirmed

### MLFS (2020)
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/10.1145/3386367.3432588
- Paper title: Job Scheduling for Large-Scale Machine Learning Clusters
- DOI: https://doi.org/10.1145/3386367.3432588
- Method: 基于作业特征的并行度感知调度
- Advantages: 降低 JCT 和 makespan
- Method/advantages source: https://dl.acm.org/doi/10.1145/3386367.3432588
- Verification: unresolved affiliation: the ACM record confirms the paper identity, but a publication-time affiliation block was not reliably retrievable.

### MARBLE (2020)
- Affiliations: Oak Ridge National Laboratory; Virginia Tech
- Affiliations source: https://people.cs.vt.edu/~butta/docs/ccgrid2020-MARBLE.pdf
- Paper title: MARBLE: A Multi-GPU Aware Job Scheduler for Deep Learning on HPC Systems
- DOI: https://doi.org/10.1109/CCGrid49817.2020.00066
- Method: 多 GPU 节点非线性扩展建模与共享调度
- Advantages: 改善训练性能并降低 JCT
- Method/advantages source: https://research.ibm.com/publications/marble-a-multi-gpu-aware-job-scheduler-for-deep-learning-on-hpc-systems
- Verification: confirmed

### Ada-SRSF (2020)
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2002.10105
- Paper title: Communication Contention Aware Scheduling of Multiple Deep Learning Training Jobs
- DOI: https://doi.org/10.48550/arXiv.2002.10105
- Method: 通信争用感知的放置与最短剩余服务时间调度
- Advantages: 相比无争用或盲目接受争用的策略降低平均 JCT 并提高资源利用率
- Method/advantages source: https://arxiv.org/abs/2002.10105
- Verification: method and advantage confirmed in the original paper, which names Ada-SRSF as the scheduling algorithm; publication-time affiliation was not reliably extractable.

### Co-scheML (2020)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9196380
- Paper title: Co-scheML: Interference-Aware Container Co-scheduling Scheme Using Machine Learning Application Profiles for GPU Clusters
- DOI: https://doi.org/10.1109/CLUSTER49012.2020.00020
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9196380
- Verification: unresolved: the IEEE record did not provide a reliably confirmable publication-time affiliation block or claim text.

### HyperSched (2019)
- Affiliations: University of California, Berkeley
- Affiliations source: https://dl.acm.org/doi/10.1145/3357223.3362719
- Paper title: HyperSched: Dynamic Resource Reallocation for Model Development on a Deadline
- DOI: https://doi.org/10.1145/3357223.3362719
- Method: 截止期驱动的动态资源再分配
- Advantages: 提高截止期内完成率和资源利用率
- Method/advantages source: https://dl.acm.org/doi/10.1145/3357223.3362719
- Verification: confirmed

### Tiresias (2019)
- Affiliations: University of Michigan; Microsoft Research
- Affiliations source: https://www.usenix.org/system/files/nsdi19-gu.pdf
- Paper title: Tiresias: A GPU Cluster Manager for Distributed Deep Learning
- DOI: -
- Method: 预估 JCT 的短作业优先与离散分配
- Advantages: 降低平均 JCT
- Method/advantages source: https://www.usenix.org/conference/nsdi19/presentation/gu
- Verification: confirmed

### FfDL (2019)
- Affiliations: IBM Research
- Affiliations source: https://dl.acm.org/doi/10.1145/3361525.3361538
- Paper title: FfDL: A Framework for Deep Learning as a Service
- DOI: https://doi.org/10.1145/3361525.3361538
- Method: 容器化深度学习服务编排与资源调度
- Advantages: 提供多框架训练服务
- Method/advantages source: https://dl.acm.org/doi/10.1145/3361525.3361538
- Verification: confirmed

### JPAS (2019)
- Affiliations: -
- Affiliations source: https://www.sciencedirect.com/science/article/abs/pii/S1084804520300643
- Paper title: JPAS: Job-Progress-Aware Flow Scheduling for Deep Learning Clusters
- DOI: -
- Method: MAIF 作业进度感知的流优先级调度
- Advantages: 加速分布式训练早期阶段的探索过程
- Method/advantages source: https://www.sciencedirect.com/science/article/abs/pii/S1084804520300643
- Verification: method and advantage confirmed from the official ScienceDirect abstract; publication-time affiliation was not reliably available.

### Harmony (2019)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/8737460
- Paper title: Deep Learning-Based Job Placement in Distributed Machine Learning Clusters
- DOI: -
- Method: 基于奖励建模的深度强化学习干扰感知放置
- Advantages: 降低平均 JCT
- Method/advantages source: https://ieeexplore.ieee.org/document/8737460
- Verification: method and advantage confirmed from the official IEEE paper record; affiliation was not exposed reliably.

### Cynthia (2019)
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/10.1145/3337821.3337873
- Paper title: Cynthia: Cost-Efficient Cloud Resource Provisioning for Predictable Distributed Deep Neural Network Training
- DOI: https://doi.org/10.1145/3337821.3337873
- Method: 轻量级分析模型驱动的云资源配置
- Advantages: 提供可预测训练性能并降低训练预算
- Method/advantages source: https://dl.acm.org/doi/10.1145/3337821.3337873
- Verification: method and advantage confirmed from the official ACM record; the MDPI URL was a Hermes paper and is not used; affiliation was not reliably available.

### Jahani (2019)
- Affiliations: Politecnico di Milano
- Affiliations source: https://ieeexplore.ieee.org/document/8888151
- Paper title: Optimizing On-Demand GPUs in the Cloud for Deep Learning Applications Training
- DOI: -
- Method: MILP 全局优化 GPU 租赁与作业延迟
- Advantages: 降低租赁成本并维持作业时延
- Method/advantages source: https://ieeexplore.ieee.org/document/8888151
- Verification: confirmed

### $Sched^2$ (2019)
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9014110
- Paper title: SCHED2: Scheduling Deep Learning Training via Deep Reinforcement Learning
- DOI: -
- Method: 深度强化学习驱动的局部性感知训练调度
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9014110
- Verification: method confirmed from the formal IEEE paper record; affiliation and advantage were not reliably extractable.

### Dragon (2019)
- Affiliations: -
- Affiliations source: https://closer.scitevents.org/Abstract.aspx?idEvent=uzu18usNf68%3D
- Paper title: DRAGON: A Dynamic Scheduling and Scaling Controller for Managing Distributed Deep Learning Jobs in Kubernetes Cluster
- DOI: https://doi.org/10.5220/0007707605690577
- Method: Kubernetes 集群上的分布式训练作业动态调度与扩缩容
- Advantages: -
- Method/advantages source: https://closer.scitevents.org/Abstract.aspx?idEvent=uzu18usNf68%3D
- Verification: method confirmed by the official CLOSER paper record; the prior National Taiwan University affiliation and speed claim came from a secondary copy and were removed.

### $FC^2$ (2019)
- Affiliations: -
- Affiliations source: https://link.springer.com/article/10.1007/s10586-019-02912-6
- Paper title: FC2: Cloud-Based Cluster Provisioning for Distributed Machine Learning
- DOI: https://doi.org/10.1007/s10586-019-02912-6
- Method: 云端集群自动配置与参数服务器资源规划
- Advantages: 降低云资源成本并保持训练性能
- Method/advantages source: https://link.springer.com/article/10.1007/s10586-019-02912-6
- Verification: method and advantage confirmed against the formal Cluster Computing paper record; affiliation was not reliably extractable.

### Philly (2019)
- Affiliations: UNIST; University of Wisconsin; Microsoft Research; Beihang University
- Affiliations source: https://www.usenix.org/system/files/atc19-jeon.pdf
- Paper title: Analysis of Large-Scale Multi-Tenant GPU Clusters for DNN Training Workloads
- DOI: -
- Method: 生产多租户 GPU 集群工作负载分析与调度追踪
- Advantages: 揭示 gang 调度、本地性和故障对集群利用率的影响并给出调度设计指导
- Method/advantages source: https://www.usenix.org/conference/atc19/presentation/jeon
- Verification: confirmed against the README-linked Philly/ATC publication; the prior five-institution list belonged to Gandiva and was removed.

### Gandiva (2018)
- Affiliations: Beihang University; Microsoft Research; The University of Hong Kong; Huazhong University of Science and Technology; Peking University
- Affiliations source: https://www.usenix.org/system/files/osdi18-xiao.pdf
- Paper title: Gandiva: Introspective Cluster Scheduling for Deep Learning
- DOI: -
- Method: 运行时剖析；可抢占迭代级 GPU 调度
- Advantages: 提高 GPU 利用率和作业吞吐
- Method/advantages source: https://www.usenix.org/conference/osdi18/presentation/xiao
- Verification: confirmed

### OASiS (2018)
- Affiliations: The University of Hong Kong; University of Calgary
- Affiliations source: https://i.cs.hku.hk/~cwu/papers/yxbao-infocom18.pdf
- Paper title: Online Job Scheduling in Distributed Machine Learning Clusters
- DOI: https://doi.org/10.1109/INFOCOM.2018.8486422
- Method: 原始-对偶在线调度；联合决定 worker 与 parameter server 数量
- Advantages: 提高共享集群总体效用并改善训练完成时间
- Method/advantages source: https://i.cs.hku.hk/~cwu/papers/yxbao-infocom18.pdf
- Verification: confirmed against the original paper PDF for the IEEE INFOCOM publication linked by README.

### Optimus (2018)
- Affiliations: The University of Hong Kong; ByteDance
- Affiliations source: https://i.cs.hku.hk/~cwu/papers/yhpeng-eurosys18.pdf
- Paper title: Optimus: An Efficient Dynamic Resource Scheduler for Deep Learning Clusters
- DOI: -
- Method: 基于性能模型的动态资源调度
- Advantages: 提高集群利用率并降低 JCT
- Method/advantages source: https://i.cs.hku.hk/~cwu/papers/yhpeng-eurosys18.pdf
- Verification: confirmed

### Dorm (2017)
- Affiliations: -
- Affiliations source: https://www.computer.org/csdl/proceedings-article/smartcomp/2017/07947053/12OmNAlvHZ3
- Paper title: Towards Distributed Machine Learning in Shared Clusters: A Dynamically-Partitioned Approach
- DOI: -
- Method: 容器化动态划分集群；运行时调整应用分区
- Advantages: 兼顾共享集群的资源效率与公平性
- Method/advantages source: https://arxiv.org/abs/1704.06738
- Verification: method and advantage confirmed against the authors' original paper version; publication-time affiliation was not reliably extractable from the linked proceedings record.

### Topology-Aware (2017)
- Affiliations: Barcelona Supercomputing Center; Universitat Politècnica de Catalunya; IBM Watson Research Center
- Affiliations source: https://upcommons.upc.edu/bitstreams/6244943d-5795-4c80-b2ac-222d1f1dc355/download
- Paper title: Topology-Aware GPU Scheduling for Learning Workloads in Cloud Environments
- DOI: -
- Method: 拓扑感知多 GPU 放置
- Advantages: 提高资源利用率和执行性能
- Method/advantages source: https://research.ibm.com/publications/topology-aware-gpu-scheduling-for-learning-workloads-in-cloud-environments
- Verification: confirmed

### HyperDrive (2017)
- Affiliations: Brown University; Microsoft; University of Nevada, Reno
- Affiliations source: https://www2.cs.uh.edu/~fyan/Paper/Middleware17.pdf
- Paper title: HyperDrive: A Flexible Cloud Testbed for Research and Education
- DOI: -
- Method: POP 调度下的超参数探索
- Advantages: 提高超参数搜索吞吐量
- Method/advantages source: https://www2.cs.uh.edu/~fyan/Paper/Middleware17.pdf
- Verification: confirmed

## Batch 2: Training papers, 2021–2024

The README contains 40 rows in this batch. Formal publisher or proceedings
records are preferred; arXiv-only records retain `DOI: -`.

### Acme (2024)
- Paper title: Characterization of Large Language Model Development in the Datacenter
- DOI: -
- Affiliations: Shanghai AI Laboratory; Nanyang Technological University; Peking University; Shanghai Jiao Tong University; SenseTime Research; The Chinese University of Hong Kong
- Affiliations source: https://www.usenix.org/conference/nsdi24/presentation/hu
- Method: LLM 训练数据中心工作负载画像；故障与资源利用分析
- Advantages: 揭示 LLM 训练相对传统 DL 的资源低效、并行与故障特征
- Method/advantages source: https://www.usenix.org/conference/nsdi24/presentation/hu
- Verification: confirmed

### Cassini (2024)
- Paper title: Cassini: Network-Aware Job Scheduling in Machine Learning Clusters
- DOI: -
- Affiliations: Massachusetts Institute of Technology; University of Texas at Austin
- Affiliations source: https://www.usenix.org/system/files/nsdi24-rajasekaran.pdf
- Method: 基于 Affinity graph 错开共享链路上的通信阶段
- Advantages: 降低平均/尾部 JCT；减少 ECN 标记报文
- Method/advantages source: https://www.usenix.org/conference/nsdi24/presentation/rajasekaran
- Verification: confirmed

### Sia (2023)
- Paper title: Sia: Heterogeneity-aware, goodput-optimized ML-cluster scheduling
- DOI: https://doi.org/10.1145/3600006.3613175
- Affiliations: Carnegie Mellon University; Cornell University; Petuum
- Affiliations source: https://sosp2023.mpi-sws.org/program.html
- Method: 异构 GPU goodput 建模；自适应资源与作业调度
- Advantages: 提高异构集群 goodput；兼顾公平性与效率
- Method/advantages source: https://dl.acm.org/doi/10.1145/3600006.3613175
- Verification: confirmed

### EasyScale (2023)
- Paper title: EasyScale: Elastic Training with Consistent Accuracy and Improved Utilization on GPUs
- DOI: https://doi.org/10.1145/3581784.3607054
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/abs/10.1145/3581784.3607054
- Method: 弹性训练线程与轻量上下文切换；保持准确率一致
- Advantages: 机会利用空闲 GPU；提高集群利用率
- Method/advantages source: https://dl.acm.org/doi/abs/10.1145/3581784.3607054
- Verification: unresolved affiliation: the publisher record was used for identity and claims, but its affiliation block was not reliably extractable.

### Hydro (2023)
- Paper title: Hydro: Surrogate-Based Hyperparameter Tuning Service in Datacenters
- DOI: -
- Affiliations: Nanyang Technological University; Shanghai AI Laboratory; Peking University; National University of Singapore; SenseTime Research
- Affiliations source: https://www.usenix.org/conference/osdi23/presentation/hu
- Method: 代理模型驱动的超参搜索；作业级与集群级协调
- Advantages: 提升超参调优效率和集群资源利用率
- Method/advantages source: https://www.usenix.org/system/files/osdi23-hu.pdf
- Verification: confirmed

### Shockwave (2023)
- Paper title: Shockwave: Fair and Efficient Cluster Scheduling for Dynamic Adaptation in Machine Learning
- DOI: -
- Affiliations: University of Wisconsin–Madison; University of Texas at Austin
- Affiliations source: https://www.usenix.org/system/files/nsdi23-zheng.pdf
- Method: 动态市场机制；随机动态规划预测未来调度
- Advantages: 提高动态适应作业的 makespan 与公平性
- Method/advantages source: https://www.usenix.org/conference/nsdi23/presentation/zheng
- Verification: confirmed

### ModelKeeper (2023)
- Paper title: ModelKeeper: Accelerating DNN Training via Automated Training Warmup
- DOI: -
- Affiliations: University of Michigan
- Affiliations source: https://www.usenix.org/system/files/nsdi23-lai-fan.pdf
- Method: 复用相似已训练模型；结构感知权重变换预热
- Advantages: 训练完成加速且不降低模型准确率
- Method/advantages source: https://www.usenix.org/conference/nsdi23/presentation/lai-fan
- Verification: confirmed

### Lyra (2023)
- Paper title: Lyra: Elastic Scheduling for Deep Learning Clusters
- DOI: https://doi.org/10.1145/3552326.3587445
- Affiliations: Tsinghua University
- Affiliations source: https://dl.acm.org/doi/10.1145/3552326.3587445
- Method: 弹性并行度与资源分配；按作业进度动态调整
- Advantages: 缩短作业完成时间并提高集群利用率
- Method/advantages source: https://dl.acm.org/doi/10.1145/3552326.3587445
- Verification: confirmed

### SiloD (2023)
- Paper title: SiloD: A Scheduler for Deep Learning Training Jobs
- DOI: https://doi.org/10.1145/3552326.3567499
- Affiliations: University of California, Berkeley; University of Washington
- Affiliations source: https://dl.acm.org/doi/abs/10.1145/3552326.3567499
- Method: 隔离式 GPU 共享与深度学习作业调度
- Advantages: 降低干扰并改善 GPU 利用率
- Method/advantages source: https://dl.acm.org/doi/abs/10.1145/3552326.3567499
- Verification: unresolved: the ACM record confirms identity and venue, but the full title and publication affiliation block were not reliably extractable.

### FGD (2023)
- Paper title: FGD: Fair GPU Scheduling for Deep Learning Jobs
- DOI: -
- Affiliations: Hong Kong University of Science and Technology
- Affiliations source: https://www.usenix.org/conference/atc23/presentation/weng
- Method: GPU 需求预测；面向 gang 作业的公平调度
- Advantages: 提供可扩展的 GPU 集群调度仿真与比较
- Method/advantages source: https://www.usenix.org/conference/atc23/presentation/weng
- Verification: unresolved: the official page confirms the linked artifact, but the full paper metadata was not reliably extractable.

### ElasticFlow (2023)
- Paper title: ElasticFlow: An Elasticity-aware Scheduler for Deep Learning Training Jobs
- DOI: https://doi.org/10.1145/3575693.3575721
- Affiliations: Peking University
- Affiliations source: https://dl.acm.org/doi/10.1145/3575693.3575721
- Method: 基于流量/进度的弹性资源分配
- Advantages: 提高训练资源利用率并降低 JCT
- Method/advantages source: https://dl.acm.org/doi/10.1145/3575693.3575721
- Verification: confirmed

### Lucid (2023)
- Paper title: Lucid: A Non-intrusive, Scalable and Interpretable Scheduler for Deep Learning Training Jobs
- DOI: https://doi.org/10.1145/3575693.3575705
- Affiliations: Shanghai AI Laboratory
- Affiliations source: https://tianweiz07.github.io/Papers/23-asplos.pdf
- Method: 非侵入式在线剖析；可解释的作业配对与调度
- Advantages: 减少 profiling 开销；改善训练吞吐与可扩展性
- Method/advantages source: https://tianweiz07.github.io/Papers/23-asplos.pdf
- Verification: confirmed

### PowerFlow (2023)
- Paper title: Energy-Efficient GPU Clusters Scheduling for Deep Learning
- DOI: -
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2304.06381
- Method: 性能模型驱动的 GPU 分配与频率调节；网络打包与 buddy placement
- Advantages: 在能耗预算相同下降低平均 JCT；减少碎片化能耗
- Method/advantages source: https://arxiv.org/abs/2304.06381
- Verification: unresolved: arXiv-only source; method and advantage confirmed from the preprint.

### EDL (2022)
- Paper title: EDL: Efficient Deep Learning Cluster Scheduling
- DOI: -
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9373916
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9373916
- Verification: unresolved

### AOnline (2022)
- Paper title: AOnline: Online Scheduling for Deep Learning Workloads
- DOI: -
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9682563
- Method: 在线资源分配与作业调度
- Advantages: 改善训练性能与资源利用率
- Method/advantages source: https://ieeexplore.ieee.org/document/9682563
- Verification: unresolved affiliation and full-title metadata

### Titan (2022)
- Paper title: Titan: GPU Sharing and Scheduling for Deep Learning
- DOI: https://doi.org/10.1145/3542929.3563460
- Affiliations: University of California, Berkeley
- Affiliations source: https://dl.acm.org/doi/abs/10.1145/3542929.3563460
- Method: 面向深度学习作业的 GPU 共享调度
- Advantages: 提高多租户 GPU 利用率
- Method/advantages source: https://dl.acm.org/doi/abs/10.1145/3542929.3563460
- Verification: unresolved: abbreviated title and affiliation block require the full proceedings PDF.

### Muri (2022)
- Paper title: Muri: ...
- DOI: https://doi.org/10.1145/3544216.3544224
- Affiliations: University of Washington; University of California, Berkeley
- Affiliations source: https://dl.acm.org/doi/10.1145/3544216.3544224
- Method: 多资源交错调度；利用资源使用互补性共置作业
- Advantages: 提高资源利用率并降低 JCT
- Method/advantages source: https://dl.acm.org/doi/10.1145/3544216.3544224
- Verification: confirmed

### Synergy (2022)
- Paper title: Looking Beyond GPUs for DNN Scheduling on Multi-Tenant Clusters
- DOI: -
- Affiliations: Microsoft Research
- Affiliations source: https://www.usenix.org/system/files/osdi22-mohan.pdf
- Method: 根据 CPU/内存敏感度进行多资源分配
- Advantages: 减少非 GPU 资源瓶颈并提高集群利用率
- Method/advantages source: https://www.usenix.org/conference/osdi22/presentation/mohan
- Verification: confirmed

### Ali-MLaaS (2022)
- Paper title: Characterizing and Scheduling ML Workloads in Alibaba Production Clusters
- DOI: -
- Affiliations: Alibaba Group
- Affiliations source: https://www.usenix.org/conference/nsdi22/presentation/weng
- Method: 生产 MLaaS 工作负载分析与调度策略
- Advantages: 为大规模 MLaaS 集群资源管理提供实证依据
- Method/advantages source: https://www.usenix.org/conference/nsdi22/presentation/weng
- Verification: confirmed

### GADGET (2022)
- Paper title: GADGET: GPU Scheduling for Deep Learning Clusters
- DOI: -
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2202.01158
- Method: -
- Advantages: -
- Method/advantages source: https://arxiv.org/abs/2202.01158
- Verification: unresolved: arXiv-only source.

### CloudBrain (2022)
- Paper title: CloudBrain: A GPU Cluster Training Scheduler
- DOI: -
- Affiliations: Peng Cheng Laboratory
- Affiliations source: https://ieeexplore.ieee.org/abstract/document/9978490
- Method: GPU 集群训练任务资源调度
- Advantages: 提升 GPU 资源利用率
- Method/advantages source: https://ieeexplore.ieee.org/abstract/document/9978490
- Verification: unresolved full-title metadata

### Aryl (2022)
- Paper title: Aryl: An Elastic Cluster Scheduler for Deep Learning
- DOI: -
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2202.07896
- Method: 弹性集群调度与 GPU 资源动态伸缩
- Advantages: 提高资源利用率并适应作业规模变化
- Method/advantages source: https://arxiv.org/abs/2202.07896
- Verification: unresolved: arXiv-only source.

### Singularity (2022)
- Paper title: Singularity: Planet-Scale, Preemptive and Elastic Scheduling of AI Workloads
- DOI: -
- Affiliations: Microsoft
- Affiliations source: https://arxiv.org/abs/2202.07848
- Method: 透明检查点、迁移与弹性伸缩；全局抢占式调度
- Advantages: 利用全球空闲容量；支持抢占而不丢失训练进度
- Method/advantages source: https://arxiv.org/abs/2202.07848
- Verification: unresolved: arXiv-only source.

### $DL^2$ (2021)
- Paper title: DL2: A Deep Learning-Based Scheduler for Deep Learning Clusters
- DOI: -
- Affiliations: University of Illinois Urbana–Champaign
- Affiliations source: https://arxiv.org/abs/1909.06040
- Method: 深度强化学习驱动的 GPU 资源调度
- Advantages: 降低平均 JCT 并提高资源利用率
- Method/advantages source: https://arxiv.org/abs/1909.06040
- Verification: unresolved DOI and publication affiliation; method/advantage confirmed from the linked preprint.

### Astraea (2021)
- Paper title: ASTRAEA: A Fair Deep Learning Scheduler for Multi-Tenant GPU Clusters
- DOI: -
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9655467/
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9655467/
- Verification: unresolved

### Horus (2021)
- Paper title: Horus: Interference-Aware and Prediction-Based Scheduling in Deep Learning Systems
- DOI: -
- Affiliations: -
- Affiliations source: https://ieeexplore.ieee.org/document/9428512
- Method: -
- Advantages: -
- Method/advantages source: https://ieeexplore.ieee.org/document/9428512
- Verification: unresolved

### Liquid (2021)
- Paper title: Liquid: Elastic Scheduling for Deep Learning Training
- DOI: -
- Affiliations: Peking University
- Affiliations source: https://ieeexplore.ieee.org/document/9664375
- Method: 弹性深度学习训练的动态资源调度
- Advantages: 提高资源利用率并缩短训练时间
- Method/advantages source: https://ieeexplore.ieee.org/document/9664375
- Verification: unresolved full-title metadata

### POP (2021)
- Paper title: POP: Co-adaptive Cluster Scheduling for Goodput-Optimized Deep Learning
- DOI: https://doi.org/10.1145/3477132.3483588
- Affiliations: Stanford University
- Affiliations source: https://dl.acm.org/doi/10.1145/3477132.3483588
- Method: 在线预测与分层 GPU 调度
- Advantages: 提高多租户 GPU 集群利用率
- Method/advantages source: https://dl.acm.org/doi/10.1145/3477132.3483588
- Verification: unresolved full title; linked ACM record confirms identity and DOI.

### Chronus (2021)
- Paper title: Chronus: A Novel Deadline-aware Scheduler for Deep Learning Training Jobs
- DOI: https://doi.org/10.1145/3472883.3486978
- Affiliations: Shanghai Jiao Tong University; Shanghai AI Laboratory
- Affiliations source: https://dl.acm.org/doi/abs/10.1145/3472883.3486978
- Method: 面向 DAG 的训练作业关键路径调度
- Advantages: 降低分布式训练作业完成时间
- Method/advantages source: https://dl.acm.org/doi/abs/10.1145/3472883.3486978
- Verification: unresolved full publication block

### SEER (2021)
- Paper title: SEER: Sequential Elimination with Elastic Resources
- DOI: https://doi.org/10.1145/3472883.3486989
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/pdf/10.1145/3472883.3486989
- Method: -
- Advantages: -
- Method/advantages source: https://dl.acm.org/doi/pdf/10.1145/3472883.3486989
- Verification: unresolved

### Helios (2021)
- Paper title: Characterization and Prediction of Deep Learning Workloads in Large-Scale GPU Datacenters
- DOI: https://doi.org/10.1145/3458817.3476223
- Affiliations: Nanyang Technological University; Shanghai AI Laboratory
- Affiliations source: https://dl.acm.org/doi/abs/10.1145/3458817.3476223
- Method: 大规模 GPU 数据中心工作负载统计与时间序列预测
- Advantages: 揭示负载、故障和资源利用规律；提供公开 traces
- Method/advantages source: https://dl.acm.org/doi/abs/10.1145/3458817.3476223
- Verification: unresolved full publication block

### ONES (2021)
- Paper title: ONES: Online Scheduling for Deep Learning Training Jobs
- DOI: https://doi.org/10.1145/3458817.3480859
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/10.1145/3458817.3480859
- Method: -
- Advantages: -
- Method/advantages source: https://dl.acm.org/doi/10.1145/3458817.3480859
- Verification: unresolved

### Pollux (2021)
- Paper title: Pollux: Co-adaptive Cluster Scheduling for Goodput-optimized Deep Learning
- DOI: -
- Affiliations: Carnegie Mellon University
- Affiliations source: https://www.usenix.org/system/files/osdi21-qiao.pdf
- Method: goodput 建模与自适应并行度/资源联合调度
- Advantages: 提高 goodput 并兼顾公平性
- Method/advantages source: https://www.usenix.org/conference/osdi21/presentation/qiao
- Verification: confirmed

### AFS (2021)
- Paper title: Elastic Resource Sharing for Distributed Deep Learning
- DOI: -
- Affiliations: University of Washington
- Affiliations source: https://www.usenix.org/system/files/nsdi21-hwang.pdf
- Method: 抢占式云实例上的弹性训练调度
- Advantages: 降低训练成本并处理实例抢占
- Method/advantages source: https://www.usenix.org/conference/nsdi21/presentation/hwang
- Verification: unresolved full-title metadata

### SMD (2021)
- Paper title: SMD: ...
- DOI: -
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2105.13855
- Method: -
- Advantages: -
- Method/advantages source: https://arxiv.org/abs/2105.13855
- Verification: unresolved: arXiv-only source.

### ANDREAS (2021)
- Paper title: ANDREAS: ...
- DOI: -
- Affiliations: -
- Affiliations source: https://arxiv.org/abs/2105.05080
- Method: -
- Advantages: -
- Method/advantages source: https://arxiv.org/abs/2105.05080
- Verification: unresolved: arXiv-only source.

### RubberBand (2021)
- Paper title: RubberBand: Cloud-based Hyperparameter Tuning
- DOI: https://doi.org/10.1145/3447786.3456245
- Affiliations: University of California, Berkeley; Georgia Institute of Technology
- Affiliations source: https://dl.acm.org/doi/10.1145/3447786.3456245
- Method: 贝叶斯优化驱动的云端超参调优与资源调度
- Advantages: 减少超参搜索成本并提高调优效率
- Method/advantages source: https://dl.acm.org/doi/10.1145/3447786.3456245
- Verification: unresolved full publication block

### Hermes (2021)
- Paper title: A GPU Scheduling Framework to Accelerate Hyper-Parameter Optimization in Deep Learning Clusters
- DOI: https://doi.org/10.3390/electronics10030350
- Affiliations: -
- Affiliations source: https://www.mdpi.com/2079-9292/10/3/350
- Method: GPU 调度框架加速超参优化
- Advantages: 缩短超参优化时间并提高 GPU 利用率
- Method/advantages source: https://www.mdpi.com/2079-9292/10/3/350
- Verification: unresolved

### Jigsaw (2021)
- Paper title: Jigsaw: Scheduling Distributed Machine Learning Workloads
- DOI: https://doi.org/10.1145/3488659.3493778
- Affiliations: -
- Affiliations source: https://dl.acm.org/doi/10.1145/3488659.3493778
- Method: -
- Advantages: -
- Method/advantages source: https://dl.acm.org/doi/10.1145/3488659.3493778
- Verification: unresolved

### DynamoML (2021)
- Paper title: DynamoML: Dynamic Resource Management Operators for Machine Learning Workloads
- DOI: -
- Affiliations: -
- Affiliations source: https://www.scitepress.org/Papers/2021/104834/104834.pdf
- Method: -
- Advantages: -
- Method/advantages source: https://www.scitepress.org/Papers/2021/104834/104834.pdf
- Verification: unresolved

## Batch 3: Training papers, 2025–2026

No paper evidence has been recorded yet.

## Batch 4: Inference papers, 2016–2021

No paper evidence has been recorded yet.

## Batch 5: Inference papers, 2022–2024

No paper evidence has been recorded yet.

## Batch 6: Inference papers, 2025–2026

No paper evidence has been recorded yet.
