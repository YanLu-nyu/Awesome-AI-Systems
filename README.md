# Thanks for your interests.
Because I focus on collaborative learning between [multi-camera networks](https://github.com/YanLu-nyu/Awesome-Multi-Camera-Network) and don't have time to organize recent research works on AI systems, I will not maintain this github. [Awesome-System-for-Machine-Learning](https://github.com/HuaizhengZhang/Awesome-System-for-Machine-Learning) maintained by [HuaizhengZhang](https://github.com/HuaizhengZhang) is an comprehensive list of rencent works on AI systems, especially on distributed machine learning systems.
Research notes and codes for AI-Systems. 
# AI-Systems
As discussed in [1, 2], there are three system-level concerns in real-world AI applications. They are deployment, cost and accessibility. 

[1] [Stoica et al. A Berkeley View of Systems Challenges for AI.](https://arxiv.org/pdf/1712.05855.pdf)<br>
[2] [Ratner et al. MLSys: The New Frontier of Machine Learning Systems.](https://arxiv.org/abs/1904.03257)

## Deployment Concerns
Deployment concerns include **robustness** to adversarial influences or other spurious factors; safety more broadly considered; **privacy** and security, especially as sensitive data is increasingly used; **interpretability**, as is increasingly both legally and operationally required; **fairness**, as ML algorithms begin to have major effects on our everyday lives; and many other similar concerns.<br>
### Popular approaches (todo, summary)
###### Video
1. [Cryptography for Safe Machine Learning. In MLSys'20.](https://www.youtube.com/watch?v=VlfZ7-5bKqk): [Shafi Goldwasser](https://simons.berkeley.edu/people/shafi-goldwasser) presented some techniques about cryptography in machine learning.
###### Paper
1. [Telekine: Secure Computing with Cloud GPUs. In NSDI'20.](https://www.usenix.org/conference/nsdi20/presentation/hunt): they aim to solve some concerns about **privacy** in the recent GPU trusted execution environments (TEE). <br>
2. [Themis: Fair and Efficient GPU Cluster Scheduling. In NSDI'20.](https://www.usenix.org/conference/nsdi20/presentation/mahajan): a **fair** GPU scheduling algorithm. **further reading**<br>
3. [Federated Optimization in Heterogeneous Networks. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1406): they proposed a framework named FedProx to tackle heterogeneity in **federated** networks. Traditional feaderated learning frameworks targeted to solve problems about **privacy** in machine learning but suffered from challenges about systems heterogeneity and statistical heterogeneity (non-identical distributions).<br>
4. [FLEET: Flexible Eﬃcient Ensemble Training for Heterogeneous Deep Neural Networks. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1411): to handle **poor performance of data sharing strategy in a heterogenous set of DNNs**, authors intro duced a ﬂexible ensemble DNN training framework named FLEET.<br>
5. [What is the State of Neural Network Pruning? In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1413): authors prop osed an open-source framework named ShrinkBench to **evaluate pruning methods**.<br>
6. [Attention-based Learning for Missing Data Imputation in HoloClean. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1417): they utilized attention mechanism to **analysis and interpret missing data imputation** problem.<br>
7. [A Systematic Methodology for Analysis of Deep Learning Hardware and Software Platforms. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1435): **an evaluation tool** for deep learning hardware and software platforms.<br>
8. [MLPerf Training Benchmark. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1437): a machine learning benchmark for **training** tasks.
## Cost
Cost on annotation, computation, latency and power. <br>
### Popular approaches (todo, summary)
###### Video
1. [Theory & Systems for Weak Supervision. In MLSys'20.](https://www.youtube.com/watch?v=CR1g2-ZqswE): [Christopher Ré](https://cs.stanford.edu/people/chrismre/) highlighted the importance of **data** in the real world deployments because we aren't usually able to get enough high quality labels for large training data. To bride this gap, he introduced many works from theoretical analysis to real world deployment about weak supervised learning, which only learns from noisy weakly labels. Also, He introduced [Snorkel](https://www.snorkel.org/) which is a popular weak supervised framework developed by Brown University.
###### Paper
1. [Improving Resource Efficiency of Deep Activity Recognition via Redundancy Reduction. In HotMobile'20.](https://dl.acm.org/doi/abs/10.1145/3376897.3377859): they target to reduce cost on **computation and memory** of deep human activity recognition (HAR) models. [Note](https://github.com/YanLu-nyu/Awesome-AI-Systems/blob/master/Notes/HAR_HotMobile_20.md)<br>
2. [Distributed Hierarchical GPU Parameter Server for Massive Scale Deep Learning Ads Systems. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1408): they propsoed a distributed GPU hierarchical parameter server to fit **terabyte-scale parameters** for massive scale deep learnning ads systems. <br>
3. [Resource Elasticity in Distributed Deep Learning. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1409): To relieve the hard assumptions about fixed resource allocation through the lifetime of the job in distributed training, they designed and implemented the first autoscaling engine for these workloads. <br>
4. [SLIDE : In Defense of Smart Algorithms over Hardware Acceleration for Large-Scale Deep Learning Systems. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1410): they prop osed Sub-Linear Deep Learning Engine named SLIDE to handle **fast training on large datasets and eﬃcient utilization on the current hardware**. This engine blends smart randomized algorithms with multicore parallelism and workload optimization.<br>
5. [Breaking the Memory Wall with Optimal Tensor Rematerialization. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1412): they prop osed a new system to **accelerate training under a memory-constraint environment**.<br>
6. [SkyNet: a Hardware-Efficient Method for Object Detection and Tracking on Embedded Systems. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1414): authors proposed SkyNet, a **hardware-efficient** method to deliver the state-of-the-art detection accuracy and speed for embedded systems. <br>
7. [Fine-Grained GPU Sharing Primitives for Deep Learning Applications. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1426): **they identified the importance of fine-grained GPU sharing methods when multiple DL workloads accessed the same GPU but they only tested some simple scheduling algorithms (FIFO, SRTF, PACK and FAIR).** From my perspective, scheduling methods can be customized for specific applications because different context help us design or implement the most suitable scheduling algorithms. [Note](https://github.com/YanLu-nyu/Awesome-AI-Systems/blob/master/Notes/Salus_MLSys20.md) <br> 
8. [Improving the Accuracy, Scalability, and Performance of Graph Neural Networks with Roc. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1427): they proposed a distributed multi-GPU framework for fast GNN training and inference on graphs.<br>
9. [OPTIMUS: OPTImized matrix MUltiplication Structure for Transformer neural network accelerator. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1428): they introduced an eﬃcient **inference accelerator for transformer network** to improve resource utilization on hardware.<br>
10. [PoET-BiN: Power Eﬃcient Tiny Binary Neurons. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1429): authors proposed **a Look-up Table based power** eﬃcient implementation on resource-constrained embedding devices.<br>
11. [Memory-Driven Mixed Low Precision Quantization for Enabling Deep Network Inference on Microcontrollers. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1430): they presented a novel end-to-end methodology for enabling the deployment of high-accuracy deep networks on **microcontrollers** through mixed low-bitwidth compression and integer-only operations.<br>
12. [Trained Quantization Thresholds for Accurate and Eﬃcient Fixed-Point Inference of Deep Neural Networks. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1431): authors presented a new eﬃcient method for **quantization**.<br>
13. [Riptide: Fast End-to-End Binarized Neural Networks. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1432): they proposed **a scheduled library for binarized linear algebra operations** based on their analysis on the underlying challenges on binarized neural networks.<br>
14. [Searching for Winograd-aware Quantized Networks. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1433): a new quantized network.<br>
15. [Blink: Fast and Generic Collectives for Distributed ML. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1434): authors introduced Blink, a collective communication library that **dynamically generates optimal communication primitives by packing spanning trees**.<br>
16. [MotherNets: Rapid Deep Ensemble Learning. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1436): to overcome **large demanding resources when training deep ensemble networks**, they proposed MotherNets to reduce training cost.
17. [Willump: A Statistically-Aware End-to-end Optimizer for Machine Learning Inference. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1416): compared with many optimizers for ML inference, they proposed Willump, an end2end optimizer for machine learning inference pipelines built on two novel optimizations: **cascade feature computations and approximating top-K queries**. [Note](https://github.com/YanLu-nyu/Awesome-AI-Systems/blob/master/Notes/Willump.md)<br>
18. [Server-Driven Video Streaming for Deep Learning Inference. In SIGCOMM'20.](https://dl.acm.org/doi/pdf/10.1145/3387514.3405887): they presented a new video streaming protocol to reduce cost of current video streaming systems.
19. [Reducto: On-Camera Filtering for Resource-Efficient Real-Time Video Analytics. In SIGCOMM'20.](https://dl.acm.org/doi/pdf/10.1145/3387514.3405874): they proposed a novel frame filtering approach to trade-off resource usage and accuracy of real-time video analytics.
## Accessibility
Accessibility to developers and organizations without PhD-level machine learning and systems expertise. From my perspective, most of distributed training works belong to this area because optimizing distributed learning tools could help developers deploy their machine learning algorithms fast.
### Popular approaches (todo, summary)
###### Paper
1. [A System for Massively Parallel Hyperparameter Tuning. In MLSys'20.](https://proceedings.mlsys.org/static/paper_files/mlsys/2020/94-Paper.pdf): they proposed a new **hyperparameter optimization algorithm** named ASHA to solve large-scale hyperparameter optimization problems in distributed training. <br>
2. [PLink: Discovering and Exploiting Locality for Accelerated Distributed Training on the public Cloud. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1405): they introduced a new optimized **communication library** called PLink to speed up distributed training in public cloud. <br>
3. [BPPSA: Scaling Back-propagation by Parallel Scan Algorithm. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1407): they reformulated the commonly used **back-propagation (BP) algorithm** into a scan operation to handle the limitation of BP in a parallel computing environment.<br>
4. [MNN: A Universal and Eﬃcient Inference Engine. In MLSys'20.](https://mlsys.org/Conferences/2020/Schedule?showEvent=1415): they proposed Mobile Neural Network (MNN), a universal and efficient **inference engine tailored to mobile applications**.
# Useful external Resources
## Books for Deep Learning (a popular learning approaches in machine learning)
1. [Dive into Deep Learning](http://d2l.ai/chapter_linear-networks/index.html)
2. [Deep Learning](http://www.deeplearningbook.org/)
3. [智能计算系统 (AI Computing Systems)](https://www.amazon.cn/dp/B085SZ968V/ref=sr_1_1?__mk_zh_CN=%E4%BA%9A%E9%A9%AC%E9%80%8A%E7%BD%91%E7%AB%99&keywords=%E6%99%BA%E8%83%BD%E8%AE%A1%E7%AE%97%E7%B3%BB%E7%BB%9F&qid=1585763990&sr=8-1)
4. [Tutorial on hardware accelerators for deep neural networks (the Energy-Efficient Multimedia Systems group at MIT)](http://eyeriss.mit.edu/tutorial.html)
## Course
1. (UW)[CSE 599W: Systems for ML](http://dlsys.cs.washington.edu/): Low-level optimization in Deep Learning frameworks.
2. (UCB)[AI-Sys: Machine Learning Systems](https://ucbrise.github.io/cs294-ai-sys-fa19/#today): a general course for AI systems.
3. (UMich)[EECS 598: Systems for AI (W'20)](https://github.com/mosharaf/eecs598/tree/w20-ai): a general course for AI systems.
## Conference
1. [SysML: Systems and Machine Learning](https://mlsys.org/Conferences/2019/index.html#body)
2. [SOSP: ACM Symposium on Operating Systems Principles](https://sosp19.rcs.uwaterloo.ca/program.html)
3. [OSDI: USENIX Symposium on Operating Systems Design and Implementation](https://www.usenix.org/conference/osdi18)
## Tools
1. [TVM: End to End Deep Learning Compiler Stack](https://tvm.apache.org/)
