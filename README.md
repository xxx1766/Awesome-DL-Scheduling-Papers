# Awesome-DL-Scheduling-Papers
🔥 A curated list of DL cluster scheduling papers.

Please feel free to pull requests or open an issue to add papers.


## Table of Content

- [Awesome-DL-Scheduling-Papers](#Awesome-DL-Scheduling-Papers)
  <!-- - [Industrial Traces](#milestone-papers) -->
  - [Schedulers for DL Training](#Schedulers-for-DL-Training)
  - [Schedulers for DL Inference](#Schedulers-for-DL-Inference)
  - [Glossary of Terms](#Glossary-of-Terms)

<!-- ## Industrial Traces -->



## Schedulers for DL Training

> **Update scope (2026-08-17):** This list prioritizes CCF-A conference papers from 2025–2026. A small number of highly relevant MLSys and EuroSys papers are also included as non-CCF-A supplements. New entries are limited to papers with an official proceedings, publisher page, or official conference acceptance record. arXiv-only, workshop-only, and industrial-report-only works are not included in the main tables.

| **Scheduler** | **Year** | **Series** | **Affiliations** | **Method** | **Advantages** | **Paper** | **Objective** | **Heter.** | **Elastic** | **AutoML** | **Code** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Heterogeneity at Hyperscale | 2026 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi26/presentation/li-suyi) | ♠ | ✔ | - | - | - |
| Weave | 2026 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi26/presentation/wu-tianyuan) | ♠♦ | ✔ | - | - | - |
| RollPacker | 2026 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi26/presentation/gao-wei) | ♠♣▲ | - | ✔ | - | [Code](https://github.com/alibaba/ROLL) |
| GFS | 2026 | ASPLOS |||| [Paper](https://www.asplos-conference.org/asplos2026/program/index.html) | ♦ | - | - | - | - |
| SING | 2025 | ASPLOS |||| [Paper](https://doi.org/10.1145/3669940.3707266) | ♠♥ | - | - | - | - |
| Rubick | 2025 | MLSys |||| [Paper](https://proceedings.mlsys.org/paper_files/paper/2025/hash/270339c997293ca2988c62f4308e389f-Abstract-Conference.html) | ♠♣ | - | ✔ | - | [Code](https://github.com/AlibabaPAI/reconfigurable-dl-scheduler) |
| JABAS | 2025 | EuroSys |||| [Paper](https://doi.org/10.1145/3689031.3696078) | ♠♣ | ✔ | ✔ | - | [Code](https://github.com/unist-ssl/JABAS) |
| Acme | 2024 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi24/presentation/hu) | ♣ | - | - | - | [Code](https://github.com/InternLM/AcmeTrace) |
| Cassini | 2024 | NSDI |||| [Paper](https://arxiv.org/abs/2308.00852) | ♠♣♥ | - | ✔ | - | - |
| Sia | 2023 | SOSP |||| [Paper](https://dl.acm.org/doi/10.1145/3600006.3613175) | ♠♣♥ | ✔ | ✔ | ✔ | [Code](https://github.com/siasosp23/artifacts) |
| EasyScale | 2023 | SC |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3581784.3607054) | ♠♣  | ✔ | ✔ | - | [Code](https://github.com/sUntvoOk/EasyScale_info_for_SC23) |
| Hydro | 2023 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi23/presentation/hu) | ♠▲ | ✔ | ✔ | ✔ | [Code](https://github.com/S-Lab-System-Group/Hydro) |
|  Shockwave | 2023 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi23/presentation/zheng) | ♠♣♥ | - | ✔ | - | [Code](https://github.com/uw-mad-dash/shockwave) |
| ModelKeeper | 2023 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi23/presentation/lai-fan) | ♦♣ | - | - | ✔ | [Code](https://github.com/SymbioticLab/ModelKeeper) |
| Lyra | 2023 | EuroSys |||| [Paper](https://dl.acm.org/doi/10.1145/3552326.3587445) | ♠♣  | ✔ | ✔ | - | - |
| SiloD | 2023 | EuroSys |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3552326.3567499) | ♠♣♥ | ✔* | - | - | - |
| FGD | 2023 | ATC |||| [Paper](https://www.usenix.org/conference/atc23/presentation/weng) | ♠♣  | - | - | - | [Code](https://github.com/hkust-adsl/kubernetes-scheduler-simulator) |
| ElasticFlow | 2023 | ASPLOS |||| [Paper](https://dl.acm.org/doi/10.1145/3575693.3575721) | ♣✿ | - | ✔ | - | [Code](https://github.com/pkusys/ElasticFlow) |
| Lucid | 2023 | ASPLOS |||| [Paper](https://dl.acm.org/doi/10.1145/3575693.3575705) | ♠♣  | - | - | - | [Code](https://github.com/S-Lab-System-Group/Lucid) |
| PowerFlow | 2023 | arxiv |||| [Paper](https://arxiv.org/abs/2304.06381) | ♦♣ | - | ✔ | - | - |
| EDL | 2022 | TPDS |||| [Paper](https://ieeexplore.ieee.org/document/9373916) | ♠♣ | - | ✔ | - | - |
| AOnline | 2022 | TCC |||| [Paper](https://ieeexplore.ieee.org/document/9682563) | ♠♣ | - | ✔ | - | - |
| Titan | 2022 | SoCC |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3542929.3563460) | ♠♣  | - | - | - | - |
| Muri | 2022 | SIGCOMM |||| [Paper](https://dl.acm.org/doi/10.1145/3544216.3544224) | ♠♣  | ✔* | - | - | [Code](https://github.com/Rivendile/Muri) |
| Synergy | 2022 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi22/presentation/mohan) | ♣  | - | - | - | [Code](https://github.com/msr-fiddle/synergy) |
| Ali-MLaaS | 2022 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi22/presentation/weng) | ♠♣ | - | - | - | [Code](https://github.com/alibaba/clusterdata/tree/master/cluster-trace-gpu-v2020) |
| GADGET | 2022 | INFOCOM |||| [Paper](https://arxiv.org/abs/2202.01158) | ♠♣ | - | ✔ | - | [Code](https://zenodo.org/record/5847644#.YishWH8zZhE) |
| CloudBrain | 2022 | ICCD |||| [Paper](https://ieeexplore.ieee.org/abstract/document/9978490) | ♠ | - | - | - | [Code](https://openi.pcl.ac.cn/potato/CloudBrain-datasets) |
| Aryl | 2022 | arxiv |||| [Paper](https://arxiv.org/abs/2202.07896) | ♠♣ | - | ✔ | ✔ | - |
| Singularity | 2022 | arxiv |||| [Paper](https://arxiv.org/abs/2202.07848) | ♠♣♦ | - | ✔ | - | - |
| $DL^2$ | 2021 | TPDS |||| [Paper](https://arxiv.org/abs/1909.06040) | ♣ | - | ✔ | - | [Code](https://github.com/pengyanghua/DL2) |
| Astraea | 2021 | TPDS |||| [Paper](https://ieeexplore.ieee.org/document/9655467/) | ♥ | - | - | - | [Code](https://github.com/yzs981130/Astraea_Artifacts) |
| Horus | 2021 | TPDS |||| [Paper](https://ieeexplore.ieee.org/document/9428512) | ♠♣ | - | - | - | - |
| Liquid | 2021 | TPDS |||| [Paper](https://ieeexplore.ieee.org/document/9664375) | ♣  | - | - | - | [Code](https://github.com/PasaLab/Liquid) |
| POP | 2021 | SOSP |||| [Paper](https://dl.acm.org/doi/10.1145/3477132.3483588) | ♥♣ | ✔ | - | - | [Code](https://github.com/stanford-futuredata/POP) |
| Chronus | 2021 | SoCC |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3472883.3486978) | ✿ | - | - | - | [Code](https://github.com/S-Lab-System-Group/ChronusArtifact/) |
| SEER | 2021 | SoCC |||| [Paper](https://dl.acm.org/doi/pdf/10.1145/3472883.3486989) | ▲ | - | ✔ | ✔ | - |
| Helios | 2021 | SC |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3458817.3476223) | ♣♦ | - | - | - | [Code](https://github.com/S-Lab-System-Group/HeliosArtifact) |
| ONES | 2021 | SC |||| [Paper](https://dl.acm.org/doi/10.1145/3458817.3480859) | ♠♣ | - | ✔ | - | [Code](https://github.com/kurisusnowdeng/ones_sc21) |
| Pollux | 2021 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi21/presentation/qiao) | ♠♣♥ | - | ✔ | ✔ | [Code](https://github.com/petuum/adaptdl) |
| AFS | 2021 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi21/presentation/hwang) | ♠♣ | - | ✔ | - | - |
| SMD | 2021 | INFOCOM |||| [Paper](https://arxiv.org/abs/2105.13855) | ♣ | - | - | - | - |
| ANDREAS | 2021 | FCloud |||| [Paper](https://arxiv.org/abs/2105.05080) | ♦ | - | - | - | - |
| RubberBand | 2021 | EuroSys |||| [Paper](https://dl.acm.org/doi/10.1145/3447786.3456245) |  ♦ | - | ✔ | ✔ | - |
| Hermes | 2021 | Electronics |||| [Paper](https://www.mdpi.com/2079-9292/10/3/350) | ♣ | - | - | ✔ | - |
| Jigsaw | 2021 | DistributedML |||| [Paper](https://dl.acm.org/doi/10.1145/3488659.3493778) | ♣ | - | - | - | - |
| DynamoML | 2021 | CLOSER |||| [Paper](https://www.scitepress.org/Papers/2021/104834/104834.pdf) | ♠♣ | - | ✔ | - | - |
| GENIE | 2020 | TPDS | National University of Defense Technology | 轻量级剖析建模；QoS 感知动态放置 | 提高 QoS 保证和系统利用率 | [Paper](https://ieeexplore.ieee.org/document/8778770) | ✿ | - | ✔ | - | - |
| Parrot | 2020 | TCC | - | - | - | [Paper](https://ieeexplore.ieee.org/document/9269382) | ♣ | - | - | - | - |
| Non-Intrusive | 2020 | SC | - | - | - | [Paper](https://dl.acm.org/doi/abs/10.5555/3433701.3433820) | ♠♣ | - | ✔ | - | - |
| Antman | 2020 | OSDI | Alibaba | 动态显存扩缩容；机会计算共置 | 提高 GPU 显存和计算单元利用率 | [Paper](https://www.usenix.org/system/files/osdi20-xiao.pdf) | ♠♣ | - | ✔ | - | [Code](https://github.com/alibaba/GPU-scheduler-for-deep-learning) |
| Gavel | 2020 | OSDI | Stanford University<br>Microsoft Research | 有效吞吐量建模；异构感知优化分配 | 提高负载承载量；降低 JCT 和 makespan | [Paper](https://www.usenix.org/conference/osdi20/presentation/narayanan-deepak) | ♣♥ | ✔ | - | - | [Code](https://github.com/stanford-futuredata/gavel) |
| HiveD | 2020 | OSDI | Peking University<br>Microsoft<br>The University of Hong Kong | 多级 GPU 亲和单元；虚拟私有集群 | 提供共享安全保证；支持生产集群长期运行 | [Paper](https://www.usenix.org/conference/osdi20/presentation/zhao-hanyu) | ♣ | - | - | - | [Code](https://github.com/microsoft/hivedscheduler) |
| Themis | 2020 | NSDI | University of Wisconsin–Madison<br>Microsoft Research | 完工时间公平；两级拍卖调度 | 提高公平性和集群效率 | [Paper](https://www.usenix.org/conference/nsdi20/presentation/mahajan) | ♥ | - | - | - | - |
| Salus | 2020 | MLSys | University of Michigan | 快速作业切换；显存共享 | 支持细粒度 GPU 共享并提高利用率 | [Paper](https://proceedings.mlsys.org/paper/2020/hash/f7177163c833dff4b38fc8d2872f1ec6-Abstract.html) | ♠♣ | - | - | - | [Code](https://github.com/SymbioticLab/Salus) |
| Vaibhav et al. | 2020 | MASCOTS | IBM Research | 动态批大小与资源联合扩缩容 | 改善作业运行时间和集群利用率 | [Paper](https://ieeexplore.ieee.org/abstract/document/9285954) | ♠♣ | - | ✔ | - | - |
| SPIN | 2020 | INFOCOM | - | 通信争用感知的作业调度 | - | [Paper](https://ieeexplore.ieee.org/document/9155445/) | ♣ | - | - | - | - |
| E-LAS | 2020 | ICPP | University of Louisiana at Lafayette | 基于实时 epoch 进度的完成时间无关调度 | 提高训练吞吐量并降低平均完成时间 | [Paper](https://dl.acm.org/doi/fullHtml/10.1145/3404397.3404415) | ♣ | - | - | - | - |
| CODA | 2020 | ICDCS | Shanghai Jiao Tong University<br>China University of Geosciences | CPU 资源反馈分配；争用消除；多阵列调度 | 提高 GPU 利用率且不增加 CPU 作业排队时间 | [Paper](https://ieeexplore.ieee.org/document/9355823) | ♣ | ✔* | - | - | - |
| Elan | 2020 | ICDCS | - | - | - | [Paper](https://ieeexplore.ieee.org/document/9355755) | ♠♣ | - | ✔ | - | - |
| Yeung | 2020 | HotCloud | University of Leeds | 基于计算图的 GPU 利用率预测 | 无需隔离式在线剖析即可预测利用率 | [Paper](https://www.usenix.org/conference/hotcloud20/presentation/yeung) | ♠ | - | - | - | - |
| $Gandiva_{fair}$ | 2020 | EuroSys | Microsoft Research India | Kubernetes 上的异构 GPU 公平共享与资源交易 | 在保证用户级 GPU 时间公平的同时提高集群效率和作业进度 | [Paper](https://dl.acm.org/doi/abs/10.1145/3342195.3387555) | ♥♣ | ✔ | - | - | - |
| MLCloudPrice | 2020 | DISPA | Stanford University<br>Microsoft Research | 跨区域、市场和云实例的动态价格优化 | 降低训练成本；支持速度成本权衡 | [Paper](https://cs.stanford.edu/~matei/papers/2020/dispa_cloud_ml.pdf) |  ♣♦ | - | - | - | [Code](https://github.com/stanford-futuredata/training_on_a_dime) |
| MLFS | 2020 | CoNext | - | 基于作业特征的并行度感知调度 | 降低 JCT 和 makespan | [Paper](https://dl.acm.org/doi/10.1145/3386367.3432588) | ♣✿ | - | - | - | [Code](https://github.com/hiddenlayer2020/ML-Job-Scheduler-MLFS) |
| MARBLE | 2020 | CCGRID | Oak Ridge National Laboratory<br>Virginia Tech | 多 GPU 节点非线性扩展建模与共享调度 | 改善训练性能并降低 JCT | [Paper](https://ieeexplore.ieee.org/document/9407835) | ♠♣ | - | ✔ | - | - |
| Ada-SRSF | 2020 | arxiv | - | 通信争用感知的放置与最短剩余服务时间调度 | 相比无争用或盲目接受争用的策略降低平均 JCT 并提高资源利用率 | [Paper](https://arxiv.org/abs/2002.10105) | ♣ | ✔* | - | - | - |
| Co-scheML | 2020 | ACSOS | - | - | - | [Paper](https://ieeexplore.ieee.org/document/9196380) | ♣ | - | - | - | - |
| HyperSched | 2019 | SoCC | University of California, Berkeley | 截止期驱动的动态资源再分配 | 提高截止期内完成率和资源利用率 | [Paper](https://dl.acm.org/doi/10.1145/3357223.3362719) | ✿ ▲ | - | ✔ | ✔ | - |
| Tiresias | 2019 | NSDI | University of Michigan<br>Microsoft Research | 预估 JCT 的短作业优先与离散分配 | 降低平均 JCT | [Paper](https://www.usenix.org/conference/nsdi19/presentation/gu) | ♣ | - | - | - | [Code](https://github.com/SymbioticLab/Tiresias) |
| FfDL | 2019 | Middleware | IBM Research | 容器化深度学习服务编排与资源调度 | 提供多框架训练服务 | [Paper](https://dl.acm.org/doi/10.1145/3361525.3361538) | ♣ | - | - | - | [Code](https://github.com/IBM/FfDL) |
| JPAS | 2019 | JNCA | - | MAIF 作业进度感知的流优先级调度 | 加速分布式训练早期阶段的探索过程 | [Paper](https://www.sciencedirect.com/science/article/abs/pii/S1084804520300643) | ♣▲ | - | - | ✔ | - |
| Harmony | 2019 | INFOCOM | - | 基于奖励建模的深度强化学习干扰感知放置 | 降低平均 JCT | [Paper](https://ieeexplore.ieee.org/document/8737460) | ♣ | - | - | - | - |
| Cynthia | 2019 | ICPP | - | 轻量级分析模型驱动的云资源配置 | 提供可预测训练性能并降低训练预算 | [Paper](https://dl.acm.org/doi/10.1145/3337821.3337873) | ♦ | - | ✔ | - | - |
| Jahani | 2019 | ICCCS | Politecnico di Milano | MILP 全局优化 GPU 租赁与作业延迟 | 降低租赁成本并维持作业时延 | [Paper](https://ieeexplore.ieee.org/document/8888151) | ♦ | ✔ | ✔ | - | - |
| $Sched^2$ | 2019 | GLOBECOM | - | 深度强化学习驱动的局部性感知训练调度 | - | [Paper](https://ieeexplore.ieee.org/document/9014110) | ♣ | - | - | - | - |
| Dragon | 2019 | CLOSER | - | Kubernetes 集群上的分布式训练作业动态调度与扩缩容 | - | [Paper](https://doi.org/10.5220/0007707605690577) | ♠♣ | - | ✔ | - | - |
| $FC^2$ | 2019 | CC | - | 云端集群自动配置与参数服务器资源规划 | 降低云资源成本并保持训练性能 | [Paper](https://link.springer.com/article/10.1007/s10586-019-02912-6) |  ♦ | ✔* | ✔ | - | - |
| Philly | 2019 | ATC | UNIST<br>University of Wisconsin<br>Microsoft Research<br>Beihang University | 生产多租户 GPU 集群工作负载分析与调度追踪 | 揭示 gang 调度、本地性和故障对集群利用率的影响并给出调度设计指导 | [Paper](https://www.usenix.org/conference/atc19/presentation/jeon) | ♣ | - | - | - | [Code](https://github.com/msr-fiddle/philly-traces) |
| Gandiva | 2018 | OSDI | Beihang University<br>Microsoft Research<br>The University of Hong Kong<br>Huazhong University of Science and Technology<br>Peking University | 运行时剖析；可抢占迭代级 GPU 调度 | 提高 GPU 利用率和作业吞吐 | [Paper](https://www.usenix.org/conference/osdi18/presentation/xiao) | ♠♣ | - | ✔ | ✔ | - |
| OASiS | 2018 | INFOCOM | The University of Hong Kong<br>University of Calgary | 原始-对偶在线调度；联合决定 worker 与 parameter server 数量 | 提高共享集群总体效用并改善训练完成时间 | [Paper](https://ieeexplore.ieee.org/abstract/document/8486422) | ♠♣ | - | ✔ | - | - |
| Optimus | 2018 | EuroSys | The University of Hong Kong<br>ByteDance | 基于性能模型的动态资源调度 | 提高集群利用率并降低 JCT | [Paper](https://i.cs.hku.hk/~cwu/papers/yhpeng-eurosys18.pdf) | ♣  | - | ✔ | - | [Code](https://github.com/pengyanghua/optimus) |
| Dorm | 2017 | SMARTCOMP | - | 容器化动态划分集群；运行时调整应用分区 | 兼顾共享集群的资源效率与公平性 | [Paper](https://www.computer.org/csdl/proceedings-article/smartcomp/2017/07947053/12OmNAlvHZ3) | ♥ | - | - | - | - |
| Topology-Aware | 2017 | SC | Barcelona Supercomputing Center<br>Universitat Politècnica de Catalunya<br>IBM Watson Research Center | 拓扑感知多 GPU 放置 | 提高资源利用率和执行性能 | [Paper](https://dl.acm.org/doi/10.1145/3126908.3126933) | ♣ | - | - | - | [Code](https://github.com/HiEST/gpu-topo-aware) |
| HyperDrive | 2017 | Middleware | Brown University<br>Microsoft<br>University of Nevada, Reno | POP 调度下的超参数探索 | 提高超参数搜索吞吐量 | [Paper](https://dl.acm.org/doi/10.1145/3135974.3135994) | ♣▲ | - | - | ✔ | - |

`Symbols of Training Schedulers`:
| JCT | Utilization | Cost | Fairness | DDL | Accuracy |
|:---:|:---:|:---:|:---:|:---:|:---:|
| ♣ | ♠ | ♦ | ♥ | ✿ | ▲ |

<!-- JCT: ♣ Utilization: ♠ Cost: ♦ Fairness: ♥ DDL: ✿ Accuracy: ▲  -->

## Schedulers for DL Inference

> **Update scope (2026-08-17):** The inference table follows the same publication and CCF-A-priority criteria as the training table. “Batch”, “Share”, and “Cloud” are marked only when the paper explicitly describes the corresponding serving capability.

| **Scheduler** | **Year** | **Series** | **Affiliations** | **Method** | **Advantages** | **Paper** | **Objective** | **Batch** | **Share** | **Cloud** | **Source Code** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| OpenTela | 2026 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi26/presentation/yao) | - | ✔ | - | - | [Code](https://github.com/eth-easl/OpenTela) |
| EcoServe | 2026 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi26/presentation/du) | ♠♦✿ | ✔ | - | - | [Code](https://github.com/MachineLearningSystem/26OSDI-EcoServe) |
| FlexLLM | 2026 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi26/presentation/oliaro) | ♠♦✿ | ✔ | ✔ | - | [Code](https://github.com/FlexLLM/artifact) |
| JITServe | 2026 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi26/presentation/zhang-wei) | ♠♦✿ | ✔ | - | - | [Code](https://github.com/UIUC-MLSys/JITServe) |
| FastServe | 2026 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi26/presentation/wu-bingyang) | ♠♦ | ✔ | - | - | - |
| TAPAS | 2025 | ASPLOS |||| [Paper](https://doi.org/10.1145/3676641.3716025) | ♠♥ | - | - | ✔ | - |
| Past-Future Scheduler | 2025 | ASPLOS |||| [Paper](https://www.asplos-conference.org/asplos2025/program.html) | ♠♦✿ | ✔ | - | - | [Code](https://github.com/ModelTC/LightLLM) |
| Helix | 2025 | ASPLOS |||| [Paper](https://doi.org/10.1145/3669940.3707215) | ♠♦♥ | - | - | ✔ | [Code](https://github.com/Thesys-lab/Helix-ASPLOS25) |
| Dilu | 2025 | ASPLOS |||| [Paper](https://doi.org/10.1145/3669940.3707251) | ♦✿ | - | ✔ | ✔ | - |
| GPU-Disaggregated Serving (Prism) | 2025 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi25/presentation/yang) | ♠♦✿ | - | - | - | - |
| ThunderServe | 2025 | MLSys |||| [Paper](https://proceedings.mlsys.org/paper_files/paper/2025/hash/c2a0e26dd9ee7d57e92bb1c24b39659a-Abstract-Conference.html) | ♠♦♥ | ✔ | - | ✔ | - |
| SOLA | 2025 | MLSys |||| [Paper](https://proceedings.mlsys.org/paper_files/paper/2025/hash/bc82dbfbfa43232be85b8d9838f49c3e-Abstract-Conference.html) | ♠♦ | ✔ | - | - | - |
| SpotServe | 2024 | ASPLOS |||| [Paper](https://arxiv.org/abs/2311.15566) | ♦♥ | ✔ | - | ✔ | [Code](https://github.com/Hsword/SpotServe) |
| DeltaZip | 2023 | arxiv |||| [Paper](https://arxiv.org/abs/2312.05215) | ♥♠ | ✔ | - | - | [Code](https://github.com/eth-easl/deltazip) |
| MOSEL | 2023 | arxiv |||| [Paper](https://arxiv.org/abs/2310.18481) | ♦♠ | ✔ | - | - | - |
| Punica | 2023 | arxiv |||| [Paper](https://arxiv.org/abs/2310.18547) | ♥♠ | - | ✔* | - | [Code](https://github.com/punica-ai/punica) |
| S-LoRA | 2023 | arxiv |||| [Paper](https://arxiv.org/abs/2311.03285) | ♥♠ | - | ✔* | - | [Code](https://github.com/S-LoRA/S-LoRA) |
| Symphony | 2023 | arxiv |||| [Paper](https://arxiv.org/abs/2308.07470) | ✿♠♦ | ✔ | - | - | - |
| DeepPlan | 2023 | EuroSys |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3552326.3567508) | ♦♠ | ✔ | - | - | [Code](https://github.com/csl-ajou/DeepPlan) |
| Tabi | 2023 | EuroSys |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3552326.3587438) | ♦♣ | - | - | ✔ | - |
| Kairos | 2023 | HPDC |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3588195.3592997) | ♦♥♠ | ✔ | - | ✔ | [Code](https://zenodo.org/records/7888058) |
| Shepherd | 2023 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi23/presentation/zhang-hong) | ✿♠♦ | ✔ | - | - | - |
| AlpaServe | 2023 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi23/presentation/li-zhouhan) | ♦♠ | ✔ | ✔ | - | [Code](https://github.com/alpa-projects/mms) |
| Clover | 2023 | SC |||| [Paper](https://dl.acm.org/doi/abs/10.1145/3581784.3607034) | ♥ | ✔ | ✔ | - | [Code](https://zenodo.org/records/8084800) |
| iGniter | 2023 | TPDS |||| [Paper](https://ieeexplore.ieee.org/document/10002315) | ✿♥ | ✔ | ✔ | ✔ | [Code](https://github.com/icloud-ecnu/igniter) |
| Gpulet | 2022 | ATC |||| [Paper](https://www.usenix.org/conference/atc22/presentation/choi-seungbeom) | ✿♠♥ | ✔ | ✔ | - | [Code](https://github.com/casys-kaist/glet) |
| Cocktail | 2022 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi22/presentation/gunasekaran) | ♣♦♥ | - | - | ✔ | [Code](https://github.com/jashwantraj92/cocktail) |
| INFaaS | 2021 | ATC |||| [Paper](https://www.usenix.org/system/files/atc21-romero.pdf) | ♦♥♠ | - | ✔ | ✔ | [Code](https://github.com/stanford-mast/INFaaS) |
| MIG-SERVING | 2021 | CoRR |||| [Paper](http://arxiv.org/abs/2109.11067) | ♦♥ | ✔ | ✔ | - | - |
| Mendoza et al. | 2021 | EuroMLSys |||| [Paper](https://dl.acm.org/doi/10.1145/3437984.3458837) | ♦ | - | ✔ | - | - |
| Abacus | 2021 | SC |||| [Paper](https://dl.acm.org/doi/10.1145/3458817.3476143) |  ♦♠ | - | ✔ | - | [Code](https://github.com/Raphael-Hao/Abacus) |
| Morphling | 2021 | SoCC |||| [Paper](https://dl.acm.org/doi/10.1145/3472883.3486987) | ♥♠ | ✔ | ✔ | ✔ | [Code](https://github.com/kubedl-io/morphling) |
| Irina | 2020 | APNet |||| [Paper](https://dl.acm.org/doi/10.1145/3411029.3411035) | ♦♠✿ | ✔ | ✔ | - | - |
| DyBatch | 2020 | CCGrid |||| [Paper](https://ieeexplore.ieee.org/document/9139602) | ♦♠ | ✔ | ✔ | - | - |
| CMS | 2020 | Future Internet |||| [Paper](https://www.mdpi.com/1999-5903/12/6/102) | ♣✿ | - | - | - | - |
| PERSEUS | 2020 | IC2E |||| [Paper](https://ieeexplore.ieee.org/document/9096261/) | ♦♥♠ | ✔ | - | ✔ | [Code](https://github.com/cake-lab/perseus) |
| AutoDeep | 2020 | Infocom |||| [Paper](https://ieeexplore.ieee.org/document/9155267) | ♦♥♠ | - | ✔ | ✔ | - |
| Clockwork | 2020 | OSDI |||| [Paper](https://www.usenix.org/conference/osdi20/presentation/gujarati) | ♦♠ | ✔ | - | - | [Code](https://gitlab.mpi-sws.org/cld/ml/clockwork) |
| GSLICE | 2020 | SoCC |||| [Paper](https://dl.acm.org/doi/10.1145/3419111.3421284) | ♠✿ | ✔ | ✔ | - | - |
| Inferline | 2020 | SoCC |||| [Paper](https://dl.acm.org/doi/10.1145/3419111.3421285) | ♦♥ | ✔ | - | ✔ | [Code](https://github.com/simon-mo/inferline-models) |
| MArk | 2019 | ATC |||| [Paper](https://www.usenix.org/conference/atc19/presentation/zhang-chengliang) | ♦♥ | ✔ | - | ✔ | [Code](https://github.com/marcoszh/MArk-Project) |
| TrIMS | 2019 | CLOUD |||| [Paper](https://ieeexplore.ieee.org/document/8814494) | ♦♠✿ | ✔ | ✔ | ✔ | [Code](https://github.com/rai-project/trims_mxnet) |
| Kube-Knots | 2019 | CLUSTER |||| [Paper](https://ieeexplore.ieee.org/document/8891040) | ♦✿ | ✔ | ✔ | - | - |
| Gilman et al. | 2019 | DIDL |||| [Paper](https://dl.acm.org/doi/10.1145/3366622.3368147) | ♦♠ | - | ✔ | - | - |
| Nanily | 2019 | HPCC |||| [Paper](https://ieeexplore.ieee.org/document/8855453) |  ♦♠ | ✔ | - | - | - |
| Ebird | 2019 | ICCD |||| [Paper](https://ieeexplore.ieee.org/abstract/document/8988602/) |  ♦♠✿ | ✔ | ✔ | - | [Code](https://github.com/sjtu-epcc/Ebird) |
| Tolerance Tiers | 2019 | ISPASS |||| [Paper](https://ieeexplore.ieee.org/abstract/document/8695638/) | ♣♦♥ | - | - | ✔ | - |
| RRL | 2019 | SC |||| [Paper](https://dl.acm.org/doi/10.1145/3295500.3356164) | ♦ | ✔ | ✔ | - | [Code](https://github.com/HeyangQin/RRL) |
| ParM | 2019 | SOSP |||| [Paper](https://dl.acm.org/doi/10.1145/3341301.3359654) | ♦ | ✔ | - | - | [Code](https://github.com/thesys-lab/parity-models) |
| HiveMind | 2018 | NIPS |||| [Paper](https://www.microsoft.com/en-us/research/publication/accelerating-deep-learning-workloads-through-efficient-multi-model-execution/) | ♠ | ✔ | ✔ | - | - |
| Space-Time | 2018 | NIPS |||| [Paper](http://learningsys.org/nips18/assets/papers/102CameraReadySubmissionGPU_Virtualization%20(8).pdf) | ♠✿ | ✔ | ✔ | - | - |
| Ease.ml | 2018 | VLDB |||| [Paper](https://dl.acm.org/doi/10.1145/3187009.3177737) | ♣ | - | - | - | [Code](https://github.com/easeml/automl) |
| Rafiki | 2018 | VLDB |||| [Paper](https://dl.acm.org/doi/10.14778/3282495.3282499) | ♣♦ | ✔ | - | - | [Code](https://github.com/nginyc/rafiki) |
| Clipper | 2017 | NSDI |||| [Paper](https://www.usenix.org/conference/nsdi17/technical-sessions/presentation/crankshaw) | ♣♦♠ | ✔ | - | - | [Code](https://github.com/ucbrise/clipper) |


`Symbols of Inference Schedulers`:
| Accuracy | Throughput | Latency| Cost | Utilization |
|:---:|:---:|:---:|:---:|:---:|
| ♣ | ♠ | ♦ | ♥ | ✿ |


## Glossary of Terms

| Terminology | Definition                                                  |
|-------------|-------------------------------------------------------------|
| JCT         | Job Completion Time (Job Finish Time - Job Submission Time) |
| Fairness    | a metric to assess whether resources are fairly shared among users or jobs                  |
| QoS         | Quality of Service                                          |
| DDL         | Deadline, a time point where DL job must be completed                                                   |
| SLO         | Service Level Objective                                     |
