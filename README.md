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

> **Update scope (2026-08-17):** This list prioritizes CCF-A conference papers from 2025–2026. A small number of highly relevant MLSys and EuroSys papers are also included as non-CCF-A supplements. New entries are limited to papers with an official proceedings, publisher page, or official conference acceptance record. arXiv-only, workshop-only, and industrial-report-only works are not included in the main tables. The `Year` column preserves the repository's original year for historical rows. When a preprint year differs from the formal publication year, the row keeps that original year and the formal year is recorded in the evidence entry's `Verification` field. New 2025–2026 rows use the formal conference or publication year.

| **Scheduler** | **Year** | **Series** | **Affiliations** | **Method** | **Advantages** | **Paper** | **Objective** | **Heter.** | **Elastic** | **AutoML** | **Code** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Heterogeneity at Hyperscale | 2026 | OSDI | Hong Kong University of Science and Technology<br>Alibaba Group<br>Fudan University | 生产 AI 集群工作负载刻画；GPU 碎片整理与抢占成本感知 SpotGPU 调度 | 回放实验中，存在资源余量的节点数减少 20.2%；GPU 分配率从 68% 提升至 93% | [Paper](https://www.usenix.org/conference/osdi26/presentation/li-suyi) | ♠ | ✔ | - | - | - |
| Weave | 2026 | OSDI | Hong Kong University of Science and Technology<br>University of Illinois Urbana-Champaign<br>Alibaba Group | 解耦式 RL 后训练跨集群共调度；两级 co-execution group 编排与热启动切换 | 成本效率较标准解耦提升 1.84×、较共置基线提升 1.38×；服务等级目标（SLO）达成率 100% | [Paper](https://www.usenix.org/conference/osdi26/presentation/wu-tianyuan) | ♠♦ | ✔ | - | - | - |
| RollPacker | 2026 | NSDI | Hong Kong University of Science and Technology<br>Alibaba Group | Tail batching 集中长尾 rollout；联合弹性并行、奖励阶段调度与流式训练 | 较 veRL 端到端加速 2.03×–2.56×、较 RLHFuse 最高 2.24×；保持 on-policy 准确性 | [Paper](https://www.usenix.org/conference/nsdi26/presentation/gao-wei) | ♠♣▲ | - | ✔ | - | [Code](https://github.com/alibaba/ROLL) |
| GFS | 2026 | ASPLOS | Shanghai Jiao Tong University<br>Zhejiang University<br>Alibaba Group | 租户 GPU 需求预测；动态 Spot 配额与抢占成本感知调度 | Spot 任务驱逐率降低 33.0%、排队延迟降低 44.1%；GPU 分配率最高提升 22.8% | [Paper](https://doi.org/10.1145/3760250.3762231) | ♦ | - | - | - | - |
| SING | 2025 | ASPLOS | Hong Kong University of Science and Technology | 四层共享 ML 集群栈；优化 FCFS、回填与装箱式资源分配 | 简化校园共享集群运维，通过公平 FCFS、回填等机制改善资源分配；已用于管理 160+ GPU、服务 480+ 活跃用户 | [Paper](https://doi.org/10.1145/3669940.3707266) | ♠♥ | - | - | - | - |
| Rubick | 2025 | MLSys | East China Normal University<br>Alibaba Group<br>Huazhong University of Science and Technology<br>Peng Cheng Laboratory | 性能模型驱动作业执行计划重配置；联合优化多资源分配 | 在 64-GPU 集群实验中，相对论文对比系统，平均作业完成时间（JCT）和 makespan 最多分别降至基线的 31.25% 和 71.4%（即论文所述最高 3.2× 和 1.4× reduction） | [Paper](https://proceedings.mlsys.org/paper_files/paper/2025/hash/270339c997293ca2988c62f4308e389f-Abstract-Conference.html) | ♠♣ | - | ✔ | - | [Code](https://github.com/AlibabaPAI/reconfigurable-dl-scheduler) |
| JABAS | 2025 | EuroSys | UNIST<br>Samsung SDS | 异构 GPU 上联合细粒度自适应 batching 与粗粒度 GPU 自动扩缩容 | 平均训练时间缩短 33.3%、成本降低 54.2%，且无准确率损失 | [Paper](https://doi.org/10.1145/3689031.3696078) | ♠♣ | ✔ | ✔ | - | [Code](https://github.com/unist-ssl/JABAS) |
| Acme | 2024 | NSDI | Shanghai AI Laboratory<br>Nanyang Technological University<br>Peking University<br>Shanghai Jiao Tong University<br>SenseTime Research<br>The Chinese University of Hong Kong | LLM 训练数据中心工作负载画像；故障与资源利用分析 | 揭示 LLM 训练相对传统 DL 的资源低效、并行与故障特征 | [Paper](https://www.usenix.org/conference/nsdi24/presentation/hu) | ♣ | - | - | - | [Code](https://github.com/InternLM/AcmeTrace) |
| Cassini | 2024 | NSDI | Massachusetts Institute of Technology<br>University of Texas at Austin | 基于 Affinity graph 错开共享链路上的通信阶段 | 降低平均/尾部作业完成时间（JCT）；减少 ECN 标记报文 | [Paper](https://arxiv.org/abs/2308.00852) | ♠♣♥ | - | ✔ | - | - |
| Sia | 2023 | SOSP | Carnegie Mellon University<br>Cornell University<br>Petuum | 异构 GPU 有效吞吐量建模；自适应资源与作业调度 | 提高异构集群有效吞吐量；兼顾公平性与效率 | [Paper](https://dl.acm.org/doi/10.1145/3600006.3613175) | ♠♣♥ | ✔ | ✔ | ✔ | [Code](https://github.com/siasosp23/artifacts) |
| EasyScale | 2023 | SC | Beihang University | 弹性训练线程与轻量上下文切换；保持准确率一致 | 机会利用空闲 GPU；提高集群利用率 | [Paper](https://dl.acm.org/doi/abs/10.1145/3581784.3607054) | ♠♣  | ✔ | ✔ | - | [Code](https://github.com/sUntvoOk/EasyScale_info_for_SC23) |
| Hydro | 2023 | OSDI | Nanyang Technological University<br>Shanghai AI Laboratory<br>Peking University<br>National University of Singapore<br>SenseTime Research | 代理模型驱动的超参搜索；作业级与集群级协调 | 提升超参调优效率和集群资源利用率 | [Paper](https://www.usenix.org/conference/osdi23/presentation/hu) | ♠▲ | ✔ | ✔ | ✔ | [Code](https://github.com/S-Lab-System-Group/Hydro) |
|  Shockwave | 2023 | NSDI | University of Wisconsin–Madison<br>University of Texas at Austin | 动态市场机制；随机动态规划预测未来调度 | 提高动态适应作业的 makespan 与公平性 | [Paper](https://www.usenix.org/conference/nsdi23/presentation/zheng) | ♠♣♥ | - | ✔ | - | [Code](https://github.com/uw-mad-dash/shockwave) |
| ModelKeeper | 2023 | NSDI | University of Michigan | 复用相似已训练模型；结构感知权重变换预热 | 训练完成加速且不降低模型准确率 | [Paper](https://www.usenix.org/conference/nsdi23/presentation/lai-fan) | ♦♣ | - | - | ✔ | [Code](https://github.com/SymbioticLab/ModelKeeper) |
| Lyra | 2023 | EuroSys | Tsinghua University | 弹性并行度与资源分配；按作业进度动态调整 | 缩短作业完成时间并提高集群利用率 | [Paper](https://dl.acm.org/doi/10.1145/3552326.3587445) | ♠♣  | ✔ | ✔ | - | - |
| SiloD | 2023 | EuroSys | University of California, Berkeley<br>University of Washington | 隔离式 GPU 共享与深度学习作业调度 | 降低干扰并改善 GPU 利用率 | [Paper](https://dl.acm.org/doi/abs/10.1145/3552326.3567499) | ♠♣♥ | ✔* | - | - | - |
| FGD | 2023 | ATC | Hong Kong University of Science and Technology | GPU 需求预测；面向协同调度作业的公平调度 | 提供可扩展的 GPU 集群调度仿真与比较 | [Paper](https://www.usenix.org/conference/atc23/presentation/weng) | ♠♣  | - | - | - | [Code](https://github.com/hkust-adsl/kubernetes-scheduler-simulator) |
| ElasticFlow | 2023 | ASPLOS | Peking University | 基于流量/进度的弹性资源分配 | 提高训练资源利用率并降低作业完成时间（JCT） | [Paper](https://dl.acm.org/doi/10.1145/3575693.3575721) | ♣✿ | - | ✔ | - | [Code](https://github.com/pkusys/ElasticFlow) |
| Lucid | 2023 | ASPLOS | Shanghai AI Laboratory | 非侵入式在线剖析；可解释的作业配对与调度 | 减少 profiling 开销；改善训练吞吐与可扩展性 | [Paper](https://dl.acm.org/doi/10.1145/3575693.3575705) | ♠♣  | - | - | - | [Code](https://github.com/S-Lab-System-Group/Lucid) |
| PowerFlow | 2023 | arxiv | Peking University | 性能模型驱动的 GPU 分配与频率调节；网络打包与 buddy 放置 | 在能耗预算相同下降低平均作业完成时间（JCT）；减少碎片化能耗 | [Paper](https://arxiv.org/abs/2304.06381) | ♦♣ | - | ✔ | - | - |
| EDL | 2022 | TPDS | The Chinese University of Hong Kong<br>Huawei Technologies Co., Ltd. | 停止无关扩缩容；动态数据管线；弹性调整训练并行度 | 适应负载变化并提高 GPU 利用率；支持迁移与落后者缓解 | [Paper](https://ieeexplore.ieee.org/document/9373916) | ♠♣ | - | ✔ | - | - |
| AOnline | 2022 | TCC | Wuhan University<br>The University of Hong Kong<br>University of Oregon | 在线批处理分组；原始-对偶算法决定作业窗口与 worker/parameter server 配置 | 在多种资源配置下提高资源利用率并降低加权平均完成时间 | [Paper](https://ieeexplore.ieee.org/document/9682563) | ♠♣ | - | ✔ | - | - |
| Titan | 2022 | SoCC | University of California, Berkeley | 面向深度学习作业的 GPU 共享调度 | 提高多租户 GPU 利用率 | [Paper](https://dl.acm.org/doi/abs/10.1145/3542929.3563460) | ♠♣  | - | - | - | - |
| Muri | 2022 | SIGCOMM | University of Washington<br>University of California, Berkeley | 多资源交错调度；利用资源使用互补性共置作业 | 提高资源利用率并降低作业完成时间（JCT） | [Paper](https://dl.acm.org/doi/10.1145/3544216.3544224) | ♠♣  | ✔* | - | - | [Code](https://github.com/Rivendile/Muri) |
| Synergy | 2022 | OSDI | Microsoft Research | 根据 CPU/内存敏感度进行多资源分配 | 减少非 GPU 资源瓶颈并提高集群利用率 | [Paper](https://www.usenix.org/conference/osdi22/presentation/mohan) | ♣  | - | - | - | [Code](https://github.com/msr-fiddle/synergy) |
| Ali-MLaaS | 2022 | NSDI | Alibaba Group | 生产 MLaaS 工作负载分析与调度策略 | 为大规模 MLaaS 集群资源管理提供实证依据 | [Paper](https://www.usenix.org/conference/nsdi22/presentation/weng) | ♠♣ | - | - | - | [Code](https://github.com/alibaba/clusterdata/tree/master/cluster-trace-gpu-v2020) |
| GADGET | 2022 | INFOCOM | Iowa State University<br>Virginia Tech<br>The University of Hong Kong<br>The Ohio State University | 环境建模；贪心 ring-all-reduce 调度与虚拟网络嵌入 | 在线调度 ring-all-reduce 作业并降低作业完成时间（JCT）；提供竞争比保证 | [Paper](https://arxiv.org/abs/2202.01158) | ♠♣ | - | ✔ | - | [Code](https://zenodo.org/record/5847644#.YishWH8zZhE) |
| CloudBrain | 2022 | ICCD | Peng Cheng Laboratory | GPU 集群训练任务资源调度 | 提升 GPU 资源利用率 | [Paper](https://ieeexplore.ieee.org/abstract/document/9978490) | ♠ | - | - | - | [Code](https://openi.pcl.ac.cn/potato/CloudBrain-datasets) |
| Aryl | 2022 | arxiv | ByteDance<br>City University of Hong Kong<br>The Chinese University of Hong Kong | 借用空闲推理服务器；训练作业弹性伸缩；回收时减少抢占 | 提高训练集群利用率并降低排队与完成时间 | [Paper](https://arxiv.org/abs/2202.07896) | ♠♣ | - | ✔ | ✔ | - |
| Singularity | 2022 | arxiv | Microsoft | 透明检查点、迁移与弹性伸缩；全局抢占式调度 | 利用全球空闲容量；支持抢占而不丢失训练进度 | [Paper](https://arxiv.org/abs/2202.07848) | ♠♣♦ | - | ✔ | - | - |
| $DL^2$ | 2021 | TPDS | University of Illinois Urbana-Champaign | 深度强化学习驱动的 GPU 资源调度 | 降低平均作业完成时间（JCT）并提高资源利用率 | [Paper](https://arxiv.org/abs/1909.06040) | ♣ | - | ✔ | - | [Code](https://github.com/pengyanghua/DL2) |
| Astraea | 2021 | TPDS | Peking University<br>SenseTime Research<br>Nanyang Technological University | LTGF 长期 GPU 时间公平度量；两阶段租户/作业调度 | 提高租户与作业公平性，同时不牺牲平均作业完成时间（JCT） | [Paper](https://ieeexplore.ieee.org/document/9655467/) | ♥ | - | - | - | [Code](https://github.com/yzs981130/Astraea_Artifacts) |
| Horus | 2021 | TPDS | Lancaster University<br>University of Leeds | 基于计算图特征预测 GPU 利用率；干扰感知共置 | 减少在线 profiling；提高吞吐与资源效率 | [Paper](https://ieeexplore.ieee.org/document/9428512) | ♠♣ | - | - | - | - |
| Liquid | 2021 | TPDS | Peking University | 弹性深度学习训练的动态资源调度 | 提高资源利用率并缩短训练时间 | [Paper](https://ieeexplore.ieee.org/document/9664375) | ♣  | - | - | - | [Code](https://github.com/PasaLab/Liquid) |
| POP | 2021 | SOSP | Stanford University | 在线预测与分层 GPU 调度 | 提高多租户 GPU 集群利用率 | [Paper](https://dl.acm.org/doi/10.1145/3477132.3483588) | ♥♣ | ✔ | - | - | [Code](https://github.com/stanford-futuredata/POP) |
| Chronus | 2021 | SoCC | Shanghai Jiao Tong University<br>Shanghai AI Laboratory | 面向 DAG 的训练作业关键路径调度 | 降低分布式训练作业完成时间 | [Paper](https://dl.acm.org/doi/abs/10.1145/3472883.3486978) | ✿ | - | - | - | [Code](https://github.com/S-Lab-System-Group/ChronusArtifact/) |
| SEER | 2021 | SoCC | University of California, Berkeley | 动态资源分配；根据超参试验收益调整资源 | 在成本约束下提高超参数搜索效率 | [Paper](https://dl.acm.org/doi/pdf/10.1145/3472883.3486989) | ▲ | - | ✔ | ✔ | - |
| Helios | 2021 | SC | Nanyang Technological University<br>Shanghai AI Laboratory | 大规模 GPU 数据中心工作负载统计与时间序列预测 | 揭示负载、故障和资源利用规律；提供公开 traces | [Paper](https://dl.acm.org/doi/abs/10.1145/3458817.3476223) | ♣♦ | - | - | - | [Code](https://github.com/S-Lab-System-Group/HeliosArtifact) |
| ONES | 2021 | SC | National University of Singapore<br>Nanyang Technological University<br>ByteDance | 在线进化搜索与弹性 batch size 编排 | 降低平均作业完成时间（JCT）；提高 GPU 利用率 | [Paper](https://dl.acm.org/doi/10.1145/3458817.3480859) | ♠♣ | - | ✔ | - | [Code](https://github.com/kurisusnowdeng/ones_sc21) |
| Pollux | 2021 | OSDI | Carnegie Mellon University | 有效吞吐量建模与自适应并行度/资源联合调度 | 提高有效吞吐量并兼顾公平性 | [Paper](https://www.usenix.org/conference/osdi21/presentation/qiao) | ♠♣♥ | - | ✔ | ✔ | [Code](https://github.com/petuum/adaptdl) |
| AFS | 2021 | NSDI | University of Washington | 抢占式云实例上的弹性训练调度 | 降低训练成本并处理实例抢占 | [Paper](https://www.usenix.org/conference/nsdi21/presentation/hwang) | ♠♣ | - | ✔ | - | - |
| SMD | 2021 | INFOCOM | Iowa State University<br>The University of Hong Kong<br>Virginia Tech<br>The Ohio State University | 和式比值多维背包分解；内层资源分配与外层作业选择 | 降低 DNN 作业完成时间并提供近似保证 | [Paper](https://arxiv.org/abs/2105.13855) | ♣ | - | - | - | - |
| ANDREAS | 2021 | FCloud | Politecnico di Milano<br>7bulls<br>University of Milano-Bicocca<br>E4 Computer Engineering | 训练作业 profiling；兼顾能耗与延迟惩罚的 Random Greedy GPU 分配 | 相比基线平均降低 30%–62% 成本 | [Paper](https://arxiv.org/abs/2105.05080) | ♦ | - | - | - | - |
| RubberBand | 2021 | EuroSys | University of California, Berkeley<br>Georgia Institute of Technology | 贝叶斯优化驱动的云端超参调优与资源调度 | 减少超参搜索成本并提高调优效率 | [Paper](https://dl.acm.org/doi/10.1145/3447786.3456245) |  ♦ | - | ✔ | ✔ | - |
| Hermes | 2021 | Electronics | Sogang University<br>SK Telecom | 容器抢占与时间共享；按早期收敛速度动态排序 | 加快超参数搜索并减少时间共享开销 | [Paper](https://www.mdpi.com/2079-9292/10/3/350) | ♣ | - | - | ✔ | - |
| Jigsaw | 2021 | DistributedML | Amazon Alexa AI<br>University of Wisconsin–Madison<br>University of Texas at Austin | 结构化部分反向传播；按迭代粒度进行调度 | 减少反向传播资源开销并提高集群效率 | [Paper](https://dl.acm.org/doi/10.1145/3488659.3493778) | ♣ | - | - | - | - |
| DynamoML | 2021 | CLOSER | National Tsing Hua University | 自动扩缩容、抢占、负载感知调度与弹性 GPU 共享 | 统一管理训练与推理混合负载并提高资源利用率 | [Paper](https://www.scitepress.org/Papers/2021/104834/104834.pdf) | ♠♣ | - | ✔ | - | - |
| GENIE | 2020 | TPDS | National University of Defense Technology | 轻量级剖析建模；QoS 感知动态放置 | 提高 QoS 保证和系统利用率 | [Paper](https://ieeexplore.ieee.org/document/8778770) | ✿ | - | ✔ | - | - |
| Parrot | 2020 | TCC | Hong Kong University of Science and Technology<br>Tianjin University<br>Dalian University of Technology | LPCAS 推断 SRPT 作业；动态作业权重与 LP 加权带宽缩放分配 | 降低具有 coflow 依赖的作业总完成时间（JCT）；在 Microsoft workload 驱动的大规模 trace-driven 仿真、与 Aalo 相同实验设定下，较 Aalo 最多降低总 JCT 58.4% | [Paper](https://ieeexplore.ieee.org/document/9269382) | ♣ | - | - | - | - |
| Non-Intrusive | 2020 | SC | - | - | - | [Paper](https://dl.acm.org/doi/abs/10.5555/3433701.3433820) | ♠♣ | - | ✔ | - | - |
| Antman | 2020 | OSDI | Alibaba Group | 动态显存扩缩容；机会计算共置 | 提高 GPU 显存和计算单元利用率 | [Paper](https://www.usenix.org/system/files/osdi20-xiao.pdf) | ♠♣ | - | ✔ | - | [Code](https://github.com/alibaba/GPU-scheduler-for-deep-learning) |
| Gavel | 2020 | OSDI | Stanford University<br>Microsoft Research | 有效吞吐量建模；异构感知优化分配 | 提高负载承载量；降低作业完成时间（JCT）和 makespan | [Paper](https://www.usenix.org/conference/osdi20/presentation/narayanan-deepak) | ♣♥ | ✔ | - | - | [Code](https://github.com/stanford-futuredata/gavel) |
| HiveD | 2020 | OSDI | Peking University<br>Microsoft<br>The University of Hong Kong | 多级 GPU 亲和单元；虚拟私有集群 | 提供共享安全保证；支持生产集群长期运行 | [Paper](https://www.usenix.org/conference/osdi20/presentation/zhao-hanyu) | ♣ | - | - | - | [Code](https://github.com/microsoft/hivedscheduler) |
| Themis | 2020 | NSDI | University of Wisconsin–Madison<br>Microsoft Research | 完工时间公平；两级拍卖调度 | 提高公平性和集群效率 | [Paper](https://www.usenix.org/conference/nsdi20/presentation/mahajan) | ♥ | - | - | - | - |
| Salus | 2020 | MLSys | University of Michigan | 快速作业切换；显存共享 | 支持细粒度 GPU 共享并提高利用率 | [Paper](https://proceedings.mlsys.org/paper/2020/hash/f7177163c833dff4b38fc8d2872f1ec6-Abstract.html) | ♠♣ | - | - | - | [Code](https://github.com/SymbioticLab/Salus) |
| Vaibhav et al. | 2020 | MASCOTS | IBM Research | 动态批大小与资源联合扩缩容 | 改善作业运行时间和集群利用率 | [Paper](https://ieeexplore.ieee.org/abstract/document/9285954) | ♠♣ | - | ✔ | - | - |
| SPIN | 2020 | INFOCOM | University of Science and Technology of China<br>Weizmann Institute of Science<br>University of Göttingen<br>The University of Hong Kong | 面向放置敏感 BSP 作业的在线调度；基于不准确执行时间估计进行决策 | 在放置敏感 BSP 作业的实验中降低 makespan；对执行时间估计误差具有鲁棒性 | [Paper](https://ieeexplore.ieee.org/document/9155445/) | ♣ | - | - | - | - |
| E-LAS | 2020 | ICPP | University of Louisiana at Lafayette | 基于实时 epoch 进度的完成时间无关调度 | 提高训练吞吐量并降低平均完成时间 | [Paper](https://dl.acm.org/doi/fullHtml/10.1145/3404397.3404415) | ♣ | - | - | - | - |
| CODA | 2020 | ICDCS | Shanghai Jiao Tong University<br>China University of Geosciences | CPU 资源反馈分配；争用消除；多阵列调度 | 提高 GPU 利用率且不增加 CPU 作业排队时间 | [Paper](https://ieeexplore.ieee.org/document/9355823) | ♣ | ✔* | - | - | - |
| Elan | 2020 | ICDCS | - | - | - | [Paper](https://ieeexplore.ieee.org/document/9355755) | ♠♣ | - | ✔ | - | - |
| Yeung | 2020 | HotCloud | University of Leeds | 基于计算图的 GPU 利用率预测 | 无需隔离式在线剖析即可预测利用率 | [Paper](https://www.usenix.org/conference/hotcloud20/presentation/yeung) | ♠ | - | - | - | - |
| $Gandiva_{fair}$ | 2020 | EuroSys | Microsoft Research India | Kubernetes 上的异构 GPU 公平共享与资源交易 | 在保证用户级 GPU 时间公平的同时提高集群效率和作业进度 | [Paper](https://dl.acm.org/doi/abs/10.1145/3342195.3387555) | ♥♣ | ✔ | - | - | - |
| MLCloudPrice | 2020 | DISPA | Stanford University<br>Microsoft Research | 跨区域、市场和云实例的动态价格优化 | 降低训练成本；支持速度成本权衡 | [Paper](https://cs.stanford.edu/~matei/papers/2020/dispa_cloud_ml.pdf) |  ♣♦ | - | - | - | [Code](https://github.com/stanford-futuredata/training_on_a_dime) |
| MLFS | 2020 | CoNext | - | 基于作业特征的并行度感知调度 | 降低作业完成时间（JCT）和 makespan | [Paper](https://dl.acm.org/doi/10.1145/3386367.3432588) | ♣✿ | - | - | - | [Code](https://github.com/hiddenlayer2020/ML-Job-Scheduler-MLFS) |
| MARBLE | 2020 | CCGRID | Oak Ridge National Laboratory<br>Virginia Tech | 多 GPU 节点非线性扩展建模与共享调度 | 改善训练性能并降低作业完成时间（JCT） | [Paper](https://ieeexplore.ieee.org/document/9407835) | ♠♣ | - | ✔ | - | - |
| Ada-SRSF | 2020 | arxiv | - | 通信争用感知的放置与最短剩余服务时间调度 | 相比无争用或盲目接受争用的策略降低平均作业完成时间（JCT）并提高资源利用率 | [Paper](https://arxiv.org/abs/2002.10105) | ♣ | ✔* | - | - | - |
| Co-scheML | 2020 | ACSOS | - | - | - | [Paper](https://ieeexplore.ieee.org/document/9196380) | ♣ | - | - | - | - |
| HyperSched | 2019 | SoCC | University of California, Berkeley | 截止期驱动的动态资源再分配 | 提高截止期内完成率和资源利用率 | [Paper](https://dl.acm.org/doi/10.1145/3357223.3362719) | ✿ ▲ | - | ✔ | ✔ | - |
| Tiresias | 2019 | NSDI | University of Michigan<br>Microsoft Research | 预估作业完成时间（JCT）的短作业优先与离散分配 | 降低平均作业完成时间（JCT） | [Paper](https://www.usenix.org/conference/nsdi19/presentation/gu) | ♣ | - | - | - | [Code](https://github.com/SymbioticLab/Tiresias) |
| FfDL | 2019 | Middleware | IBM Research | 容器化深度学习服务编排与资源调度 | 提供多框架训练服务 | [Paper](https://dl.acm.org/doi/10.1145/3361525.3361538) | ♣ | - | - | - | [Code](https://github.com/IBM/FfDL) |
| JPAS | 2019 | JNCA | - | MAIF 作业进度感知的流优先级调度 | 加速分布式训练早期阶段的探索过程 | [Paper](https://www.sciencedirect.com/science/article/abs/pii/S1084804520300643) | ♣▲ | - | - | ✔ | - |
| Harmony | 2019 | INFOCOM | - | 基于奖励建模的深度强化学习干扰感知放置 | 降低平均作业完成时间（JCT） | [Paper](https://ieeexplore.ieee.org/document/8737460) | ♣ | - | - | - | - |
| Cynthia | 2019 | ICPP | - | 轻量级分析模型驱动的云资源配置 | 提供可预测训练性能并降低训练预算 | [Paper](https://dl.acm.org/doi/10.1145/3337821.3337873) | ♦ | - | ✔ | - | - |
| Jahani | 2019 | ICCCS | Politecnico di Milano | MILP 全局优化 GPU 租赁与作业延迟 | 降低租赁成本并维持作业时延 | [Paper](https://ieeexplore.ieee.org/document/8888151) | ♦ | ✔ | ✔ | - | - |
| $Sched^2$ | 2019 | GLOBECOM | - | 深度强化学习驱动的局部性感知训练调度 | - | [Paper](https://ieeexplore.ieee.org/document/9014110) | ♣ | - | - | - | - |
| Dragon | 2019 | CLOSER | - | Kubernetes 集群上的分布式训练作业动态调度与扩缩容 | - | [Paper](https://doi.org/10.5220/0007707605690577) | ♠♣ | - | ✔ | - | - |
| $FC^2$ | 2019 | CC | - | 云端集群自动配置与参数服务器资源规划 | 降低云资源成本并保持训练性能 | [Paper](https://link.springer.com/article/10.1007/s10586-019-02912-6) |  ♦ | ✔* | ✔ | - | - |
| Philly | 2019 | ATC | UNIST<br>University of Wisconsin–Madison<br>Microsoft Research<br>Beihang University | 生产多租户 GPU 集群工作负载分析与调度追踪 | 揭示协同调度、本地性和故障对集群利用率的影响并给出调度设计指导 | [Paper](https://www.usenix.org/conference/atc19/presentation/jeon) | ♣ | - | - | - | [Code](https://github.com/msr-fiddle/philly-traces) |
| Gandiva | 2018 | OSDI | Beihang University<br>Microsoft Research<br>The University of Hong Kong<br>Huazhong University of Science and Technology<br>Peking University | 运行时剖析；可抢占迭代级 GPU 调度 | 提高 GPU 利用率和作业吞吐 | [Paper](https://www.usenix.org/conference/osdi18/presentation/xiao) | ♠♣ | - | ✔ | ✔ | - |
| OASiS | 2018 | INFOCOM | The University of Hong Kong<br>University of Calgary | 原始-对偶在线调度；联合决定 worker 与 parameter server 数量 | 提高共享集群总体效用并改善训练完成时间 | [Paper](https://ieeexplore.ieee.org/abstract/document/8486422) | ♠♣ | - | ✔ | - | - |
| Optimus | 2018 | EuroSys | The University of Hong Kong<br>ByteDance | 基于性能模型的动态资源调度 | 提高集群利用率并降低作业完成时间（JCT） | [Paper](https://i.cs.hku.hk/~cwu/papers/yhpeng-eurosys18.pdf) | ♣  | - | ✔ | - | [Code](https://github.com/pengyanghua/optimus) |
| Dorm | 2017 | SMARTCOMP | - | 容器化动态划分集群；运行时调整应用分区 | 兼顾共享集群的资源效率与公平性 | [Paper](https://www.computer.org/csdl/proceedings-article/smartcomp/2017/07947053/12OmNAlvHZ3) | ♥ | - | - | - | - |
| Topology-Aware | 2017 | SC | Barcelona Supercomputing Center<br>Universitat Politècnica de Catalunya<br>IBM Watson Research Center | 拓扑感知多 GPU 放置 | 提高资源利用率和执行性能 | [Paper](https://dl.acm.org/doi/10.1145/3126908.3126933) | ♣ | - | - | - | [Code](https://github.com/HiEST/gpu-topo-aware) |
| HyperDrive | 2017 | Middleware | Brown University<br>Microsoft<br>University of Nevada, Reno | POP 调度下的超参数探索 | 提高超参数搜索吞吐量 | [Paper](https://dl.acm.org/doi/10.1145/3135974.3135994) | ♣▲ | - | - | ✔ | - |

`Symbols of Training Schedulers`:
| JCT | Utilization | Cost | Fairness | DDL | Accuracy |
|:---:|:---:|:---:|:---:|:---:|:---:|
| ♣ | ♠ | ♦ | ♥ | ✿ | ▲ |

<!-- JCT: ♣ Utilization: ♠ Cost: ♦ Fairness: ♥ DDL: ✿ Accuracy: ▲  -->

## Schedulers for DL Inference

> **Update scope (2026-08-17):** The inference table follows the same publication, CCF-A-priority, and `Year` semantics as the training table. “Batch”, “Share”, and “Cloud” are marked only when the paper explicitly describes the corresponding serving capability.

| **Scheduler** | **Year** | **Series** | **Affiliations** | **Method** | **Advantages** | **Paper** | **Objective** | **Batch** | **Share** | **Cloud** | **Source Code** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| OpenTela | 2026 | OSDI | ETH Zurich<br>University of Cambridge<br>EPFL<br>Massachusetts Institute of Technology<br>ETH AI Center<br>Hong Kong University of Science and Technology | 用户态去中心化编排覆盖层；CRDT gossip 服务发现、统一异构集群接口与异构感知调度 | 生产部署超过 22 个月，跨机构为 1000+ 研究者、142 个模型处理 1300 万请求和 150 亿 token | [Paper](https://www.usenix.org/conference/osdi26/presentation/yao) | - | ✔ | - | - | [Code](https://github.com/eth-easl/OpenTela) |
| EcoServe | 2026 | OSDI | Sun Yat-Sen University | 面向普通 GPU 集群的部分解耦编排；实例内按时间分离 prefill/decode、跨实例循环激活并自适应路由 | 32 张 L20、以太网集群服务 30B/70B 模型时，有效吞吐量较 vLLM、Sarathi、DistServe、MoonCake 分别提升 1.96×、1.99×、2.51×、2.40× | [Paper](https://www.usenix.org/conference/osdi26/presentation/du) | ♠♦✿ | ✔ | - | - | [Code](https://github.com/MachineLearningSystem/26OSDI-EcoServe) |
| FlexLLM | 2026 | NSDI | Carnegie Mellon University<br>Purdue University<br>Anthropic PBC<br>Mistral AI<br>Stanford University<br>Amazon Web Services | 在共享 GPU 上按 token 融合 LLM 推理与 PEFT 微调；混合 token 调度器按服务等级目标（SLO）动态交错执行 | LLaMA-3.1-8B、Qwen-2.5-14B/32B 端到端实验中，在推理负载最高 20 req/s 时满足服务等级目标（SLO）；微调吞吐在重载/轻载下分别提升 1.9×–4.8×/2.5×–6.8× | [Paper](https://www.usenix.org/conference/nsdi26/presentation/oliaro) | ♠♦✿ | ✔ | ✔ | - | [Code](https://github.com/FlexLLM/artifact) |
| JITServe | 2026 | NSDI | University of Illinois Urbana-Champaign<br>Google<br>Cisco Research | 以渐进修正的不精确请求信息进行服务等级目标（SLO）感知调度；分组 margin-goodput 优化按需分配带宽与组批 | 在聊天、深度研究和智能体流水线等工作负载中，较论文对比方案将服务有效吞吐量提升 1.4×–6.3×，或节省 28.5%–83.2% 资源 | [Paper](https://www.usenix.org/conference/nsdi26/presentation/zhang-wei) | ♠♦✿ | ✔ | - | - | [Code](https://github.com/UIUC-MLSys/JITServe) |
| FastServe | 2026 | NSDI | Peking University | 输出 token 粒度抢占式调度；skip-join 多级反馈队列与 GPU/主存中间状态换入换出 | 论文评测中，吞吐较 vLLM 最高提升 6.1× | [Paper](https://www.usenix.org/conference/nsdi26/presentation/wu-bingyang) | ♠♦ | ✔ | - | - | - |
| TAPAS | 2025 | ASPLOS | University of Illinois at Urbana-Champaign<br>Microsoft Azure Research<br>Microsoft Azure | 热/功耗感知的 GPU VM 放置、LLM 请求路由与实例配置联合调度 | Azure 生产 traces 的大规模评测中保持 P99 推理时延，最高温度和行峰值功耗分别降低 17% 和 23%，在热与功耗封顶时间低于 0.7% 的条件下，支持最多 40% 的服务器超配 | [Paper](https://doi.org/10.1145/3676641.3716025) | ♠♥ | - | - | ✔ | - |
| Past-Future Scheduler | 2025 | ASPLOS | Beihang University<br>SenseTime<br>Peking University | 结合历史输出长度分布与未来各时点 KV-cache 需求预测进行批次准入，平衡排队与请求驱逐 | 多种模型与硬件实验中，LightLLM 的 SLA 有效吞吐量较激进或保守调度器最高提升约 2–3× | [Paper](https://doi.org/10.1145/3676641.3716011) | ♠♦✿ | ✔ | - | - | [Code](https://github.com/ModelTC/LightLLM) |
| Helix | 2025 | ASPLOS | Carnegie Mellon University | 将异构 GPU 与网络建模为最大流；用 MILP 联合优化模型放置并按请求选择流水线 | 24–42 节点异构集群实验中，较异构感知基线吞吐最高提升 3.3×，prompt/decode 平均时延最高降低 66%/24% | [Paper](https://doi.org/10.1145/3669940.3707215) | ♠♦♥ | - | - | ✔ | [Code](https://github.com/Thesys-lab/Helix-ASPLOS25) |
| Dilu | 2025 | ASPLOS | Institute of Computing Technology, Chinese Academy of Sciences<br>University of Chinese Academy of Sciences<br>Zhongguancun Laboratory<br>Nanjing Institute of InforSuperBahn<br>Institute of Intelligent Computing Technology, Suzhou, Chinese Academy of Sciences | 面向 serverless DL 的内省弹性；资源互补放置与 GPU 垂直/实例水平二维协同扩缩容 | 论文评测中，较论文基线减少 10%–46% GPU 碎片，推理/训练吞吐分别提升 1.8×/1.1×，服务等级目标（SLO）违约率降低 11%–71% | [Paper](https://doi.org/10.1145/3669940.3707251) | ♦✿ | - | ✔ | ✔ | - |
| GPU-Disaggregated Serving (Prism) | 2025 | NSDI | Hong Kong University of Science and Technology<br>Alibaba Group | 将 DLRM 自动切分为 CPU/GPU 密集子图并在 RDMA 解耦资源池调度；拓扑感知放置与服务等级目标（SLO）感知通信 | 拥挤 GPU 集群实验中，CPU 和 GPU 碎片分别减少 53% 和 27% | [Paper](https://www.usenix.org/conference/nsdi25/presentation/yang) | ♠♦✿ | - | - | - | - |
| ThunderServe | 2025 | MLSys | University of Cambridge<br>Peking University<br>ETH Zurich | 面向云端异构 GPU/网络联合优化分组、prefill/decode 阶段配置、并行策略与请求路由；轻量重调度 | 在相同价格预算的异构云与同构自建环境实验中，较 HexGen、DistServe 和 vLLM，吞吐最高提升 2.1×、平均提升 1.7×。在论文的 latency-deadline 评测中，可满足的时延期限最高严格 2.5×、平均严格 1.5× | [Paper](https://proceedings.mlsys.org/paper_files/paper/2025/hash/c2a0e26dd9ee7d57e92bb1c24b39659a-Abstract-Conference.html) | ♠♦♥ | ✔ | - | ✔ | - |
| SOLA | 2025 | MLSys | Tsinghua University<br>Infinigence AI<br>Shanghai Jiao Tong University<br>Peking University | 迭代级状态感知调度；按请求与系统状态动态控制执行顺序和工作量，平衡 TTFT/TPOT | A100 上 ShareGPT/LongBench 实验中，服务等级目标（SLO）达成率由 45.5% 提至 99.4%；相对 vLLM-S、vLLM-D、SJF 平均多服务 1.04×–1.27× 请求 | [Paper](https://proceedings.mlsys.org/paper_files/paper/2025/hash/bc82dbfbfa43232be85b8d9838f49c3e-Abstract-Conference.html) | ♠♦ | ✔ | - | - | - |
| SpotServe | 2024 | ASPLOS | Carnegie Mellon University<br>Peking University<br>The Chinese University of Hong Kong | 抢占式 GPU 实例上的动态并行重配置；最小成本上下文迁移与有状态推理恢复 | 在真实抢占 traces 上，P99 尾延迟较最佳基线降低 2.4×–9.1×；较按需实例节省 54% 成本 | [Paper](https://arxiv.org/abs/2311.15566) | ♦♥ | ✔ | - | ✔ | [Code](https://github.com/Hsword/SpotServe) |
| DeltaZip | 2023 | arxiv | ETH Zurich<br>Massachusetts Institute of Technology | 压缩全参数微调模型的权重增量；共享基础模型并批处理增量计算 | 模型增量最高压缩 10×且保持论文评测质量；吞吐较比较系统提升 2×–12× | [Paper](https://arxiv.org/abs/2312.05215) | ♥♠ | ✔ | - | - | [Code](https://github.com/eth-easl/deltazip) |
| MOSEL | 2023 | arxiv | University of Texas at Austin | 按请求准确率与时延约束动态选择多模态输入；截止期感知排队与批处理 | 在论文多模态工作负载中，保证目标准确率时吞吐提升 3.6×、作业完成时间缩短 11× | [Paper](https://arxiv.org/abs/2310.18481) | ♦♠ | ✔ | - | - | - |
| Punica | 2023 | arxiv | University of Washington<br>Duke University | 跨 LoRA 适配器异构批处理 CUDA 内核；共享基础模型并整合多租户请求 | 固定 GPU 集群上，吞吐较论文比较的 LLM serving 系统提升 12×，每 token 仅增加 2 ms 时延 | [Paper](https://arxiv.org/abs/2310.18547) | ♥♠ | - | ✔* | - | [Code](https://github.com/punica-ai/punica) |
| S-LoRA | 2023 | arxiv | University of California, Berkeley<br>Stanford University<br>Shanghai Jiao Tong University | Unified Paging 联合管理 LoRA 权重与 KV cache；异构批处理内核和张量并行 | 较 HuggingFace PEFT 与朴素 vLLM LoRA 支持，吞吐最高提升 4×；单机可服务数千适配器 | [Paper](https://arxiv.org/abs/2311.03285) | ♥♠ | - | ✔* | - | [Code](https://github.com/S-LoRA/S-LoRA) |
| Symphony | 2023 | arxiv | University of Washington<br>Duke University<br>Microsoft | 服务等级目标（SLO）可调度窗口内延迟派发以扩大批次；集中式细粒度协调与负载比例扩缩容 | 同等 GPU 数下有效吞吐量提升 5×；同等工作负载下 GPU 用量减少 60% | [Paper](https://arxiv.org/abs/2308.07470) | ✿♠♦ | ✔ | - | - | - |
| DeepPlan | 2023 | EuroSys | Ajou University | Direct Host Access 边加载边执行；多 GPU 并行传输模型并生成执行计划 | 四张 V100 上，单请求推理加速 1.18×–2.21×；BERT-Base 100 ms 服务等级目标（SLO）实验有效吞吐量达 98%–99% | [Paper](https://dl.acm.org/doi/abs/10.1145/3552326.3567508) | ♦♠ | ✔ | - | - | [Code](https://github.com/csl-ajou/DeepPlan) |
| Tabi | 2023 | EuroSys | Hong Kong University of Science and Technology<br>University of Science and Technology of China<br>Fuzhou University | 小模型置信度路由至大模型的多级推理；注意力词剪枝与加权集成 | 达到 LLM 级准确率目标时，平均时延较 INFaaS 降低 21%–40%、较 Cocktail 降低 11%–26% | [Paper](https://dl.acm.org/doi/abs/10.1145/3552326.3587438) | ♦♣ | - | - | ✔ | - |
| Kairos | 2023 | HPDC | Northeastern University<br>MIT Lincoln Laboratory | 成本预算下近似搜索异构 CPU/GPU 配置；二分图匹配进行 QoS 感知请求路由 | 满足 QoS 与成本预算时，吞吐较满足 QoS 的同构配置高 1.25× 以上 | [Paper](https://dl.acm.org/doi/abs/10.1145/3588195.3592997) | ♦♥♠ | ✔ | - | ✔ | [Code](https://zenodo.org/records/7888058) |
| Shepherd | 2023 | NSDI | University of Waterloo<br>Yale University<br>University of California, Berkeley | 聚合请求流的两级规划/服务；结合抢占与模型批处理特性的在线调度 | 生产工作负载上，有效吞吐量最高提升 18.1×、利用率最高提升 1.8×，并扩展至数百 workers | [Paper](https://www.usenix.org/conference/nsdi23/presentation/zhang-hong) | ✿♠♦ | ✔ | - | - | - |
| AlpaServe | 2023 | OSDI | University of California, Berkeley<br>Peking University<br>University of Pennsylvania<br>Stanford University<br>Google<br>University of California, San Diego | 联合优化多模型放置与模型并行；以统计复用吸收突发请求 | 在生产工作负载上，满足 99% 以上请求时延约束时，请求率最高提升 10×或可承受突发度提升 6× | [Paper](https://www.usenix.org/conference/osdi23/presentation/li-zhouhan) | ♦♠ | ✔ | ✔ | - | [Code](https://github.com/alpa-projects/mms) |
| Clover | 2023 | SC | Northeastern University<br>MIT Lincoln Laboratory | 碳强度感知的混合精度模型选择；MIG GPU 分区与请求调度 | 48 小时 California trace 实验中，满足 SLA 且准确率下降 2%–4% 时，各应用碳排放节省超过 75% | [Paper](https://dl.acm.org/doi/abs/10.1145/3581784.3607034) | ♥ | ✔ | ✔ | - | [Code](https://zenodo.org/records/8084800) |
| iGniter | 2023 | TPDS | East China Normal University<br>University of Louisiana at Lafayette<br>Sun Yat-Sen University<br>Peng Cheng Laboratory<br>Huazhong University of Science and Technology | GPU 共享干扰性能建模；联合优化空间配额与自适应批大小 | 在云 GPU 共置实验中满足时延/吞吐服务等级目标（SLO），并降低资源配置成本 | [Paper](https://ieeexplore.ieee.org/document/10002315) | ✿♥ | ✔ | ✔ | ✔ | [Code](https://github.com/icloud-ecnu/igniter) |
| Gpulet | 2022 | ATC | Korea Advanced Institute of Science and Technology | GPU 空间分区与时间共享统一为 gpulet；干扰感知装箱、批处理和自动扩缩容 | 两台双 RTX 2080 Ti 服务器上，服务等级目标（SLO）保持吞吐较时间共享平均提升 61.7%，干扰建模再提升 7.5% | [Paper](https://www.usenix.org/conference/atc22/presentation/choi-seungbeom) | ✿♠♥ | ✔ | ✔ | - | [Code](https://github.com/casys-kaist/glet) |
| Cocktail | 2022 | NSDI | The Pennsylvania State University | 动态选择满足准确率/时延的模型集成；结合 transient VM 的主动自动扩缩容 | AWS 实验中部署成本降低 1.45×、时延降低 2×，最多 96% 请求满足目标准确率 | [Paper](https://www.usenix.org/conference/nsdi22/presentation/gunasekaran) | ♣♦♥ | - | - | ✔ | [Code](https://github.com/jashwantraj92/cocktail) |
| INFaaS | 2021 | ATC | Stanford University | 模型变体生成与性能/成本/准确率约束下的模型、硬件和优化选择；模型级与虚拟机级自动扩缩容 | 提高吞吐；减少延迟服务等级目标（SLO）违约；降低成本 | [Paper](https://www.usenix.org/system/files/atc21-romero.pdf) | ♦♥♠ | - | ✔ | ✔ | [Code](https://github.com/stanford-mast/INFaaS) |
| MIG-SERVING | 2021 | CoRR | ByteDance | 基于 MIG 的 GPU 分区与服务放置；贪心、遗传算法和蒙特卡洛树搜索联合重配置 | 满足服务级目标；减少所需 GPU 数量 | [Paper](http://arxiv.org/abs/2109.11067) | ♦♥ | ✔ | ✔ | - | - |
| Mendoza et al. | 2021 | EuroMLSys | Stanford University | 干扰预测模型驱动的异构服务共置调度 | 降低共置造成的延迟退化 | [Paper](https://dl.acm.org/doi/10.1145/3437984.3458837) | ♦ | - | ✔ | - | - |
| Abacus | 2021 | SC | Shanghai Jiao Tong University<br>Shanghai AI Laboratory | 基于算子重叠与精确时延预测的在线调度；按 QoS 剩余裕量排序共置服务 | 提高 GPU 利用率；在满足 QoS 的同时提高吞吐 | [Paper](https://dl.acm.org/doi/10.1145/3458817.3476143) |  ♦♠ | - | ✔ | - | [Code](https://github.com/Raphael-Hao/Abacus) |
| Morphling | 2021 | SoCC | Hong Kong University of Science and Technology<br>Alibaba Group | 以性能模型和贝叶斯优化搜索云原生模型服务配置 | 接近最优配置；降低配置搜索开销；改善服务性能 | [Paper](https://dl.acm.org/doi/10.1145/3472883.3486987) | ♥♠ | ✔ | ✔ | ✔ | [Code](https://github.com/kubedl-io/morphling) |
| Irina | 2020 | APNet | City University of Hong Kong<br>Peng Cheng Laboratory | 在线抢占、机会批处理与自适应策略选择相结合的 DNN 推理调度 | 提高吞吐和 GPU 利用率；降低平均与尾部延迟 | [Paper](https://dl.acm.org/doi/10.1145/3411029.3411035) | ♦♠✿ | ✔ | ✔ | - | - |
| DyBatch | 2020 | CCGrid | The University of Sydney<br>Commonwealth Scientific and Industrial Research Organisation<br>RMIT University | 面向时分设备的动态批处理与公平调度；按请求等待和服务等级目标（SLO）调整批次 | 提高吞吐；降低延迟；改善多租户公平性 | [Paper](https://ieeexplore.ieee.org/document/9139602) | ♦♠ | ✔ | ✔ | - | - |
| CMS | 2020 | Future Internet | Zhejiang Sci-Tech University<br>Central South University | 持续机器学习平台统一训练、部署和模型更新；监控资源避免训练与服务争用 | 支持持续模型服务；减少资源争用 | [Paper](https://www.mdpi.com/1999-5903/12/6/102) | ♣✿ | - | - | - | - |
| PERSEUS | 2020 | IC2E | Worcester Polytechnic Institute | 多租户 CNN 服务的测量与性能/成本权衡分析；按模型、硬件和负载评估共置 | 提供吞吐、延迟与成本权衡依据；提高资源利用率 | [Paper](https://ieeexplore.ieee.org/document/9096261/) | ♦♥♠ | ✔ | - | ✔ | [Code](https://github.com/cake-lab/perseus) |
| AutoDeep | 2020 | Infocom | Tsinghua University<br>University of Science and Technology of China<br>Microsoft Research Asia | 基于性能剖析的云端推理自动部署；联合选择实例、副本和模型放置 | 降低部署与运维开销；满足延迟目标并提高资源利用率 | [Paper](https://ieeexplore.ieee.org/document/9155267) | ♦♥♠ | - | ✔ | ✔ | - |
| Clockwork | 2020 | OSDI | Max Planck Institute for Software Systems<br>Emory University | 利用 DNN 执行时间可预测性进行集中式请求排队与精确调度 | 支持大规模模型服务；降低尾延迟并稳定满足延迟目标 | [Paper](https://www.usenix.org/conference/osdi20/presentation/gujarati) | ♦♠ | ✔ | - | - | [Code](https://gitlab.mpi-sws.org/cld/ml/clockwork) |
| GSLICE | 2020 | SoCC | University of California, Riverside<br>Indian Institute of Technology Gandhinagar | 基于 CUDA MPS 的 GPU 空间切分；自调节分区资源并按服务等级目标（SLO）调整批大小 | 提高 GPU 利用率和吞吐；降低推理延迟 | [Paper](https://dl.acm.org/doi/10.1145/3419111.3421284) | ♠✿ | ✔ | ✔ | - | - |
| Inferline | 2020 | SoCC | Microsoft Research<br>University of California, Berkeley<br>Anyscale<br>Databricks<br>Georgia Institute of Technology | 离线剖析与离散事件仿真选择流水线硬件、复制和批处理；在线控制器按负载自动扩缩容 | 降低成本；减少延迟服务等级目标（SLO）违约 | [Paper](https://dl.acm.org/doi/10.1145/3419111.3421285) | ♦♥ | ✔ | - | ✔ | [Code](https://github.com/simon-mo/inferline-models) |
| MArk | 2019 | ATC | Hong Kong University of Science and Technology<br>University of Nevada, Reno | 动态批处理；按负载在 CPU、GPU 等异构硬件间路由并弹性扩缩容 | 降低服务成本；满足服务等级目标（SLO）；提高吞吐 | [Paper](https://www.usenix.org/conference/atc19/presentation/zhang-chengliang) | ♦♥ | ✔ | - | ✔ | [Code](https://github.com/marcoszh/MArk-Project) |
| TrIMS | 2019 | CLOUD | University of Illinois Urbana-Champaign<br>IBM Research | 面向 FaaS 的多层模型缓存与隔离模型共享；减少模型加载和数据搬移 | 降低端到端延迟；提高系统吞吐和内存效率；保持准确率 | [Paper](https://ieeexplore.ieee.org/document/8814494) | ♦♠✿ | ✔ | ✔ | ✔ | [Code](https://github.com/rai-project/trims_mxnet) |
| Kube-Knots | 2019 | CLUSTER | The Pennsylvania State University | GPU 容器动态编排与资源回收；在在线服务和批任务间放置空闲资源 | 提高 GPU 利用率；提升资源收获能力 | [Paper](https://ieeexplore.ieee.org/document/8891040) | ♦✿ | ✔ | ✔ | - | - |
| Gilman et al. | 2019 | DIDL | Worcester Polytechnic Institute | DNN 执行缓存与模型复用；在相同输入或可复用计算间共享中间结果 | 减少重复计算；降低推理延迟和资源开销 | [Paper](https://dl.acm.org/doi/10.1145/3366622.3368147) | ♦♠ | - | ✔ | - | - |
| Nanily | 2019 | HPCC | University of Electronic Science and Technology of China | QoS 感知的 DNN 推理任务放置与资源调度 | 满足 QoS 约束；提高吞吐和资源利用率 | [Paper](https://ieeexplore.ieee.org/document/8855453) |  ♦♠ | ✔ | - | - | - |
| Ebird | 2019 | ICCD | Shanghai Jiao Tong University<br>Shanghai University of Finance and Economics | GPU 常驻内存池、多粒度推理引擎与弹性批处理调度 | 提高吞吐和响应性；降低推理延迟 | [Paper](https://ieeexplore.ieee.org/abstract/document/8988602/) |  ♦♠✿ | ✔ | ✔ | - | [Code](https://github.com/sjtu-epcc/Ebird) |
| Tolerance Tiers | 2019 | ISPASS | Carnegie Mellon University<br>University of California, Berkeley | 将可接受准确率/延迟范围划分为多个容忍等级，支持服务端按等级选择配置 | 提供准确率与延迟的可控权衡；降低延迟或资源成本 | [Paper](https://ieeexplore.ieee.org/abstract/document/8695638/) | ♣♦♥ | - | - | ✔ | - |
| RRL | 2019 | SC | University of Nevada, Reno<br>Google | 基于强化学习的模型服务调度与资源配置 | 降低服务成本；满足延迟服务等级目标（SLO） | [Paper](https://dl.acm.org/doi/10.1145/3295500.3356164) | ♦ | ✔ | ✔ | - | [Code](https://github.com/HeyangQin/RRL) |
| ParM | 2019 | SOSP | Carnegie Mellon University | 用擦除编码训练 parity model，并以编码/解码替代部分副本实现预测恢复 | 降低尾延迟；以更少额外资源提供容错 | [Paper](https://dl.acm.org/doi/10.1145/3341301.3359654) | ♦ | ✔ | - | - | [Code](https://github.com/thesys-lab/parity-models) |
| HiveMind | 2018 | NIPS | Stanford University<br>Microsoft Research | 多模型执行编排与资源共享；按模型执行特征合并 GPU 工作 | 提高 GPU 利用率和多模型吞吐 | [Paper](https://www.microsoft.com/en-us/research/publication/accelerating-deep-learning-workloads-through-efficient-multi-model-execution/) | ♠ | ✔ | ✔ | - | - |
| Space-Time | 2018 | NIPS | University of California, Berkeley<br>Massachusetts Institute of Technology | 基于 GPU 空间与时间切分的动态共置调度 | 提高 GPU 利用率；在满足延迟目标下提升吞吐 | [Paper](http://learningsys.org/nips18/assets/papers/102CameraReadySubmissionGPU_Virtualization%20(8).pdf) | ♠✿ | ✔ | ✔ | - | - |
| Ease.ml | 2018 | VLDB | ETH Zurich<br>University of Rochester<br>Microsoft Research | 面向多租户的声明式模型选择与资源共享；按成本和用户需求选择模型 | 降低多租户模型选择与管理成本；改善资源共享 | [Paper](https://dl.acm.org/doi/10.1145/3187009.3177737) | ♣ | - | - | - | [Code](https://github.com/easeml/automl) |
| Rafiki | 2018 | VLDB | National University of Singapore<br>Beijing Institute of Technology<br>Zhejiang University<br>University of Electronic Science and Technology of China | 覆盖分布式超参数调优、在线集成建模以及延迟/准确率权衡 | 提升训练与推理服务的效率、可扩展性和可用性 | [Paper](https://doi.org/10.14778/3282495.3282499) | ♣♦ | ✔ | - | - | [Code](https://github.com/nginyc/rafiki) |
| Clipper | 2017 | NSDI | University of California, Berkeley<br>University of Chicago | 统一预测抽象与模型选择；请求批处理、结果缓存和自适应副本路由 | 降低延迟；提高吞吐和准确率 | [Paper](https://www.usenix.org/conference/nsdi17/technical-sessions/presentation/crankshaw) | ♣♦♠ | ✔ | - | - | [Code](https://github.com/ucbrise/clipper) |


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
