---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

# Yunkang Cao (曹云康)

I am currently an Assistant Professor at the [School of Artificial Intelligence and Robotics, Hunan University (HNU)](http://robotics.hnu.edu.cn/). 
I am proud to be a core member of the distinguished research team led by **[Yaonan Wang (王耀南院士)](https://robotics.hnu.edu.cn/info/1176/3098.htm)** and **[Hui Zhang (张辉院长)](https://robotics.hnu.edu.cn/info/1176/2966.htm)**. 

I received my Ph.D. from [Huazhong University of Science and Technology (HUST)](http://english.hust.edu.cn/), mentored by [Prof. Weiming Shen](https://scholar.google.com.hk/citations?user=FuSHsx4AAAAJ&hl=en&oi=sra) (FCAE, FIEEE). During my doctoral studies, I was a visiting researcher at [Politecnico di Milano (Polimi)](https://www.polimi.it/) under the supervision of [Prof. Giacomo Boracchi](https://boracchi.faculty.polimi.it/).

**[Research Vision]**
My current research passion lies in constructing a **deployable, full-chain toolchain for industrial anomaly detection**, spanning the entire lifecycle from **Perception (Detection)** to **Cognition (Understanding/Reasoning)**, and finally to **Action (Recovery)**. 
I am actively extending these capabilities to the domain of **Embodied AI and Robotics**, with a specific focus on **Unmanned Autonomous Inspection Systems**. My ultimate goal is to bridge the gap between academic SOTA models and reliable, open-world industrial applications.

Currently, I serve as the **Executive Guest Editor** for the SI of [Foundation Models for Anomaly Detection, Reasoning, and Recovery](https://www.sciencedirect.com/special-issue/326046/foundation-models-for-anomaly-detection-reasoning-and-recovery) in *Pattern Recognition*.

# 🌟 Join Us
### Let's Define the Future of Industrial AI

**We are actively recruiting Master's students, Research Assistants (RA), and Visiting Scholars. Highly motivated undergraduates with a strong mathematical background are also welcome to join as interns.**

We value **genuine problem-solving** over metric-chasing. We are looking for partners who have a keen sense for cutting-edge technologies (e.g., AIGC, Foundation Models) and solid coding skills to explore the boundaries of AI in industry and robotics together.

**What you can expect:**

  * **Deep Collaboration**: I am not just a supervisor, but a comrade-in-arms on your research journey. We will leverage **AIGC** and **MLLMs** to reconstruct traditional industrial vision, tackling system-level challenges from "Perception" to "Recovery".
  * **Diversified Growth**: Whether your goal is publishing in top-tier venues (CVPR/AAAI/TPAMI) or solving critical bottlenecks in real-world deployment, I will provide customized guidance to help you achieve impactful results.

**🔬 Research Focus**

If you are eager to make systematic contributions at the intersection of **Industrial Foundation Models** and **Embodied AI**, join us to explore:

1.  **Industrial Foundation Models**:
    Investigating the application of **Scaling Laws** in industrial vision to build efficient, general-purpose backbones. Leveraging the generalization power of **MLLMs** to solve the **Cold Start** problem, achieving high-precision detection of both known defects and unknown anomalies simultaneously.
2.  **AIGC & Controllable Anomaly Synthesis**:
    Addressing the inherent scarcity of anomaly data by using **Generative AI**. The goal is to synthesize visually realistic, controllable, and **physics-compliant** defect samples, boosting model training through high-quality synthetic data.
3.  **Multimodal Reasoning & Diagnosis**:
    Moving beyond "Perception" to "Cognition". Utilizing **MLLMs** to describe anomalies and analyze their underlying mechanisms. Combining **Agentic AI** to realize a closed loop from problem discovery to autonomous decision-making and repair.
4.  **Embodied AI & Autonomous Inspection**:
    Deploying visual foundation models onto unmanned systems (e.g., mobile robots, manipulators) to enable autonomous perception in **open-world environments**. Focusing on identifying generalized anomalies that violate "safety states" in unstructured scenarios.

**📩 Contact**: Please send your CV to [caoyunkang0207@gmail.com](mailto:caoyunkang0207@gmail.com)

# 🌟 加入我们
**定义工业 AI 的未来：从基础模型到具身智能**


**本课题组长期招收硕士研究生、科研助理（RA）及访问学者，亦欢迎数理基础扎实的本科生提前进组实习。**

我们坚持以**解决真问题**为核心，相比于单纯的“刷榜”，我们更看重技术背后的逻辑与实际价值。如果你对 **AIGC**、**Foundation Models** 等前沿技术充满好奇，且拥有扎实的代码落地能力，欢迎加入我们，共同拓展 AI 在工业与机器人领域的边界。

**在这里，你将获得：**

* **并肩作战**
    在这里，我会成为你科研路上的战友。我将带你深入一线，利用 **AIGC** 和 **MLLMs** 重构传统的工业视觉范式，共同挑战从“感知诊断”到“自主修复”的系统级难题。

* **个性化成长**
    无论你志在冲击顶会（CVPR/AAAI/TPAMI），还是渴望解决工业界的“卡脖子”难题，我都会结合你的特质定制培养方案，让你的成果**既有学术高度，又有落地回响**。
  

**🔬 重点研究方向**

如果你渴望在以下**工业大模型**与**具身智能**的交叉领域做出系统性贡献，欢迎加入我们：

1.  **工业视觉基础模型**
    探索 **Scaling Law** 在工业视觉领域的应用，构建高效、通用的工业视觉底座。致力于利用 **MLLMs** (多模态大语言模型) 强大的泛化能力，解决工业场景下的**冷启动 (Cold Start)** 难题，实现单一大模型对“已知缺陷”与“未知异常”的同时高精度检测。
2.  **AIGC 与可控异常生成**
    针对工业异常数据天然稀缺的痛点，研究基于 **AIGC** 的数据增强技术。目标是合成视觉真实、语义可控且**符合物理规律 (Physics-compliant)** 的缺陷样本，通过高质量的合成数据辅助模型训练，突破数据瓶颈。
3.  **多模态推理与智能诊断**
    超越传统的“感知”边界，向“认知”延伸。利用 **MLLMs** 对异常进行深层语义描述与成因机理分析。结合 **智能体 (Agents)** 技术，实现从“发现问题”到“自主决策”再到“闭环修复”的完整工业智能链路。
4.  **具身智能与自主巡检**
    将视觉大模型部署于无人系统（如移动机器人、机械臂），赋予机器人在**开放环境**下的自主感知与交互能力。重点研究非结构化场景中对不符合“安全状态”的广义异常识别，实现真正的**具身智能**巡检。

**📩 联系方式**: 请发送简历至 [caoyunkang0207@gmail.com](mailto:caoyunkang0207@gmail.com)

-----



# 🔥 News
- *2025.12*: &nbsp;🏆 **[Top Journal]** Our paper on [Zero-shot 3D Anomaly Detection](https://arxiv.org/pdf/2409.13162) has been accepted by **IEEE TSMC** (IF=8.7)!
- *2025.12*: &nbsp;🏆 **[Top Journal]** Our paper *"A Comprehensive Survey for Real-World Industrial Defect Detection"* has been accepted by **Journal of Manufacturing Systems (JMS)** (IF=12.2)!
- *2025.11*: &nbsp;🎉 **[Big News]** **Three papers** have been accepted by **AAAI 2026**! 
  - **2 Orals** regarding Consistent Reasoning (IAD-R1) and High-resolution 3D Anomaly Detection.
  - **1 Poster** regarding Cross-modal Zero-shot Anomaly Generation.
- *2025.09*: &nbsp;📢 I am honored to serve as the **Executive Guest Editor** for the **Pattern Recognition (PR)** Special Issue on *"Foundation Models for Anomaly Detection, Reasoning, and Recovery"*.
- *2025.08*: &nbsp;🎉 Our paper on [Unsupervised Image Anomaly Detection]() has been accepted by **IEEE TCSVT**.
- *2025.07*: &nbsp;🎉 Our paper on [Zero-shot Image Anomaly Detection](https://github.com/hmyao22/GRNR) has been accepted by **IEEE TSMC**.
- *2025.07*: &nbsp;🎉 Our paper on [Zero-shot Image Anomaly Detection](https://arxiv.org/abs/2507.11003) has been accepted by **ICCV ADFM Workshop**.
- *2025.07*: &nbsp;🎉 Two papers on [Point Cloud Anomaly Detection](https://arxiv.org/abs/2507.21555) and [Fully Unsupervised Anomaly Detection](https://github.com/hustzhangyuxin/LLBNAD) have been accepted by **IEEE SMC**.
- *2025.05*: &nbsp;🏆 We are deeply honored to have been awarded the <span style="color:#b02418; font-weight:bold;">Best Student Paper Award</span> at **CSCWD 2025**.
- *2025.04*: &nbsp;🎉 We successfully organized the [CVPR 2025 Pre-conference "Industrial Vision" Special Session](https://mp.weixin.qq.com/s/opOMTAN2s7kLVwVaNfwAfg), attracting over 5,000 online viewers!
- *2025.03*: &nbsp;🎉 Two papers on [Unified Anomaly Detection](https://arxiv.org/pdf/2503.02424) and [Unseen Anomaly Generation](https://arxiv.org/html/2406.01078v2) have been accepted by **CVPR 2025**.

# 📝 Selected Publications 
(For the complete list of publications, please refer to [My Google Scholar Page](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ&view_op=list_works&sortby=pubdate))

# 📝 Selected Publications 

[![Citations](https://img.shields.io/badge/Citations-1200%2B-007ec6?logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ)
[![Top Tier Papers](https://img.shields.io/badge/Top_Tier_Papers-40%2B-FF6B6B?logo=googlescholar&logoColor=white)](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ)
[![GitHub Stars](https://img.shields.io/badge/GitHub_Stars-1.8k%2B-181717?logo=github&logoColor=white)](https://github.com/caoyunkang)

(For the complete list of publications, please refer to [My Google Scholar Page](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ&view_op=list_works&sortby=pubdate))
<span style="color:#b02418; font-weight:bold;">#</span> co-first author | <span style="color:#b02418; font-weight:bold;">*</span> corresponding author <br> 

<ol reversed>

  <li id="TSMC"> 
    Towards zero-shot point cloud anomaly detection: A multi-view projection framework <a href="https://arxiv.org/pdf/2409.13162">[Paper]</a> <a href="https://github.com/hustCYQ/MVP-PCLIP">[Code]</a> <br> 
    Yuqi Cheng#, <span style="color:#b02418; font-weight:bold;">Yunkang Cao#</span>, Guoyang Xie, Zhichao Lu, Weiming Shen* <br>
    <i>IEEE Transactions on Systems, Man, and Cybernetics: Systems <strong>(IEEE TSMC).</strong></i> 2026.
  </li>

<li id="JMS25"> 
  A Comprehensive Survey for Real-World Industrial Defect Detection: Challenges, Approaches, and Prospects  <a href="https://arxiv.org/abs/2507.13378">[Paper]</a> <a href="https://github.com/hustCYQ/Towards-Practical-Industrial-Anomaly-Detection">[Code]</a> <br>
  Yuqi Cheng#, <span style="color:#b02418; font-weight:bold;">Yunkang Cao#</span>, Haiming Yao, Wei Luo, Cheng Jiang, Hui Zhang, Weiming Shen* <br>
  <i>Journal of Manufacturing Systems <strong>(JMS)</strong></i>. 2026. (In Press)
</li>

<li id="AAAI26-1"> 
  IAD-R1: Reinforcing Consistent Reasoning in Industrial Anomaly Detection <br>
  Yanhui Li, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Chengliang Liu, Yuan Xiong, Xinghui Dong, Chao Huang <a href="https://arxiv.org/abs/2508.09178">[Paper]</a> <a href="https://github.com/Yanhui-Lee/IAD-R1">[Code]</a> <br>
  <i>The 40th Annual AAAI Conference on Artificial Intelligence <strong>(AAAI)</strong></i>. 2026. 
  <span style="color:#b02418; font-weight:bold;">(Oral Presentation)</span>
</li>

<li id="AAAI26-2"> 
  Towards High-resolution 3D Anomaly Detection: A Scalable Dataset and Real-time Framework for Subtle Industrial Defects <a href="https://arxiv.org/abs/2507.07435">[Paper]</a> <a href="https://github.com/hustCYQ/MiniShift-Simple3D">[Code]</a> <br>
  Yuqi Cheng, Yihan Sun, Hui Zhang, Weiming Shen, <span style="color:#b02418; font-weight:bold;">Yunkang Cao*</span><span style="color:#b02418; font-weight:bold;"></span><br>
  <i>The 40th Annual AAAI Conference on Artificial Intelligence <strong>(AAAI)</strong></i>. 2026. 
  <span style="color:#b02418; font-weight:bold;">(Oral Presentation)</span>
</li>

<li id="AAAI26-3"> 
  Anomagic: Cross-modal Prompt-driven Zero-shot Anomaly Generation <a href="https://arxiv.org/abs/2511.10020">[Paper]</a> <a href="https://github.com/yuxin-jiang/Anomagic">[Code]</a> <br>
  Yuxin Jiang, Wei Luo, Hui Zhang, Qiyu Chen, Haiming Yao, Weiming Shen, <span style="color:#b02418; font-weight:bold;">Yunkang Cao*</span> <br>
  <i>The 40th Annual AAAI Conference on Artificial Intelligence <strong>(AAAI)</strong></i>. 2026. (Poster Presentation)
</li>


  <li id="OT-Manuscript2"> 
    Global-Regularized Neighborhood Regression for Efficient Zero-Shot Texture Anomaly Detection 
    <a href="https://arxiv.org/abs/2406.07333">[Paper]</a>  
    <a href="https://github.com/hmyao22/GRNR">[Code]</a> <br> 
    Haiming Yao, Wei Luo, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Yiheng Zhang, Wenyong Yu*, Weiming Shen <br>
    <i>IEEE Transactions on Systems, Man, and Cybernetics: Systems <strong>(IEEE TSMC)</strong></i>. 
  </li>

  <li id="FA-Pub10"> 
    Exploring Intrinsic Normal Prototypes within a Single Image for Universal Anomaly Detection <a href="">[Paper]</a> <a href="">[Code]</a> <br> 
    Wei Luo#, <span style="color:#b02418; font-weight:bold;">Yunkang Cao#</span>, Haiming Yao#, Xiaotian Zhang, Jianan Lou, Yuqi Cheng, Weiming Shen, Wenyong Yu* <br>
    <i>IEEE Conference on Computer Vision and Pattern Recognition <strong>(CVPR)</strong></i>. 2025.
  </li>

  <li id="FA-Pub9"> 
    Anomaly Anything: Promptable Unseen Visual Anomaly Generation <a href="https://arxiv.org/html/2406.01078v2">[Paper]</a> <a href="">[Code]</a> <br> 
    Han Sun, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Hao Dong, Olga Fink* <br>
    <i>IEEE Conference on Computer Vision and Pattern Recognition <strong>(CVPR)</strong></i>. 2025.
  </li>

  <li id="FA-Manuscript2"> 
    Customizing Visual-Language Foundation Models for Multi-Modal Anomaly Detection and Reasoning <a href="https://arxiv.org/abs/2403.11083">[Paper]</a> <a href="https://github.com/caoyunkang/GPT4V-for-Generic-Anomaly-Detection">[Code]</a> <br> 
    Xiaohao Xu#, <span style="color:#b02418; font-weight:bold;">Yunkang Cao#</span>, Huaxin Zhang, Nong Sang, Xiaonan Huang, Weiming Shen* <br>
    <i>IEEE International Conference on Computer Supported Cooperative Work in Design <strong>(CSCWD)</strong></i>. 2025. <span style="color:#b02418; font-weight:bold;">Best Student Paper Award</span> 
  </li>

  <li id="FA-Pub8"> 
    Personalizing Vision-Language Models with Hybrid Prompts for Zero-Shot Anomaly Detection <a href="https://arxiv.org/abs/2305.10724">[Paper]</a> <a href="https://github.com/caoyunkang/Segment-Any-Anomaly">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Xiaohao Xu, Yuqi Cheng, Chen Sun, Zongwei Du, Liang Gao, Weiming Shen* <br>
    <i>IEEE Transactions on Cybernetics <strong>(IEEE TCYB)</strong></i>. 2025.
  </li>

  <li id="FA-Pub7"> 
    VarAD: Lightweight High-Resolution Image Anomaly Detection via Visual Autoregressive Modeling <a href="https://ieeexplore.ieee.org/document/10843956">[Paper]</a> <a href="https://github.com/caoyunkang/VarAD">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Haiming Yao, Wei Luo, Weiming Shen* <br>
    <i>IEEE Transactions on Industrial Informatics <strong>(IEEE TII).</strong></i> 2025.
  </li>

  <li id="FA-Pub6"> 
    AdaCLIP: Adapting CLIP with Hybrid Learnable Prompts for Zero-Shot Anomaly Detection <a href="https://arxiv.org/abs/2407.15795">[Paper]</a> <a href="https://github.com/caoyunkang/AdaCLIP">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Jiangning Zhang, Luca Frittoli, Yuqi Cheng, Weiming Shen*, Giacomo Boracchi <br>
    <i>European Conference on Computer Vision <strong>(ECCV).</strong></i> 2024.
  </li>

  <li id="FA-Pub5"> 
    Complementary pseudo multimodal feature for point cloud anomaly detection <a href="https://www.sciencedirect.com/science/article/pii/S0031320324005120">[Paper]</a> <a href="https://github.com/caoyunkang/CPMF">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Xiaohao Xu, Weiming Shen* <br>
    <i>Pattern Recognition <strong>(PR).</strong></i> 2024.
  </li>

  <li id="FA-Pub4"> 
    BiaS: Incorporating Biased Knowledge to Boost Unsupervised Image Anomaly Localization <a href="https://ieeexplore.ieee.org/document/10402554">[Paper]</a> <a href="https://github.com/caoyunkang/CDO">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Xiaohao Xu, Chen Sun, Liang Gao, Weiming Shen* <br>
    <i>IEEE Transactions on Systems, Man, and Cybernetics: Systems <strong>(IEEE TSMC).</strong></i> 2024.
  </li>

  <li id="FA-Pub3"> 
    Collaborative discrepancy optimization for reliable image anomaly localization <a href="https://ieeexplore.ieee.org/document/10034849">[Paper]</a> <a href="https://github.com/caoyunkang/CDO">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Xiaohao Xu, Zhaoge Liu, Weiming Shen* <br>
    <i>IEEE Transactions on Industrial Informatics <strong>(IEEE TII).</strong></i> 2023.
  </li>

  <li id="FA-Pub2"> 
    High-Resolution Image Anomaly Detection via Spatiotemporal Consistency Incorporated Knowledge Distillation <a href="https://ieeexplore.ieee.org/abstract/document/10260338">[Paper]</a>  <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Yiheng Zhang, Weiming Shen* <br>
    <i>IEEE International Conference on Automation Science and Engineering <strong>(IEEE CASE).</strong></i> 2023.
  </li>

  <li id="FA-Pub1"> 
    Informative knowledge distillation for image anomaly segmentation <a href="https://www.sciencedirect.com/science/article/pii/S0950705122004038">[Paper]</a> <a href="https://github.com/caoyunkang/IKD">[Code]</a> <br> 
    <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Qian Wan, Weiming Shen*, Liang Gao <br>
    <i>Knowledge-Based Systems <strong>(KBS).</strong></i> 2022.
  </li>

  <li id="OT-Pub11"> 
    Boosting Global-Local Feature Matching via Anomaly Synthesis for Multi-Class Point Cloud Anomaly Detection
    <br> Yuqi Cheng, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Dongfang Wang, Weiming Shen*, Wenlong Li <br>
    <i>IEEE Transactions on Automation Science and Engineering <strong>(IEEE TASE)</strong></i>. 2025.
  </li>

  <li id="OT-Pub10"> 
    Prototypical Learning Guided Context-Aware Segmentation Network for Few-Shot Anomaly Detection 
    <a href="https://ieeexplore.ieee.org/document/10702559">[Paper]</a> 
    <a href="https://github.com/yuxin-jiang/PCSNet">[Code]</a> <br> 
    Yuxin Jiang, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Weiming Shen* <br>
    <i>IEEE Transactions on Neural Networks and Learning Systems <strong>(IEEE TNNLS)</strong></i>.  2024.
  </li>

  <li id="OT-Pub9"> 
    LogiCode: an LLM-Driven Framework for Logical Anomaly Detection <a href="https://arxiv.org/abs/2406.04687">[Paper]</a> <a href="https://github.com/22strongestme/LOCO-Annotations">[Code]</a> <br> 
    Yiheng Zhang, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Xiaohao Xu, Weiming Shen* <br>
    <i>IEEE Transactions on Automation Science and Engineering <strong>(IEEE TASE)</strong></i>. 2024.
  </li>

  <li id="OT-Pub8"> 
    Prior Normality Prompt Transformer for Multi-class Industrial Image Anomaly Detection <a href="https://ieeexplore.ieee.org/document/10574313">[Paper]</a> <br> 
    Haiming Yao, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Wei Luo, Weihang Zhang, Wenyong Yu*, Weiming Shen <br>
    <i>IEEE Transactions on Industrial Informatics <strong>(IEEE TII).</strong></i> 2024.
  </li>

  <li id="OT-Pub7"> 
    Deep Feature Contrasting for Industrial Image Anomaly Segmentatio <a href="https://ieeexplore.ieee.org/document/10379172">[Paper]</a> <br> 
    Qian Wan, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Liang Gao, Xinyu Li*, Yiping Gao <br>
    <i>IEEE Transactions on Instrumentation and Measurement <strong>(IEEE TIM).</strong></i> 2024.
  </li>

  <li id="OT-Pub6"> 
    Dual-path Frequency Discriminators for Few-shot Anomaly Detection <br> 
    Yuhu Bai#, Jiangning Zhang#, Zhaofeng Chen, Yuhang Dong,  <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Guanzhong Tian* <br>
    <i>Knowledge-Based Systems <strong>(KBS).</strong></i> 2024. 
  </li>

  <li id="OT-Pub5"> 
    Generative Denoise Distillation: Simple Stochastic Noises Induce Efficient Knowledge Transfer for Dense Prediction <br> 
    Zhaoge Liu, Xiaohao Xu, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Weiming Shen* <br>
    <i>Knowledge-Based Systems <strong>(KBS).</strong></i> 2024. 
  </li>

  <li id="OT-Pub4"> 
    RAD: A Comprehensive Dataset for Benchmarking the Robustness of Image Anomaly Detection 
    <a href="https://arxiv.org/abs/2406.07176">[Paper]</a>  
    <a href="https://github.com/hustCYQ/RAD-dataset">[Code]</a> <br> 
    Yuqi Cheng, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Rui Chen, Weiming Shen* <br>
    <i>IEEE International Conference on Automation Science and Engineering <strong>(IEEE CASE).</strong></i> 2024.
  </li>

  <li id="OT-Pub3"> 
    Attention Fusion Reverse Distillation for Multi-Lighting Image Anomaly Detection <a href="https://arxiv.org/abs/2406.04573">[Paper]</a>  <br> 
    Yiheng Zhang, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Tianhang Zhang, Weiming Shen* <br>
    <i>IEEE International Conference on Automation Science and Engineering <strong>(IEEE CASE).</strong></i> 2024.
  </li>

  <li id="OT-Pub2"> 
    A masked reverse knowledge distillation method incorporating global and local information for image anomaly detection <a href="https://www.sciencedirect.com/science/article/pii/S0950705123007323">[Paper]</a> <a href="https://github.com/yuxin-jiang/MRKD">[Code]</a> <br>
    Yuxin Jiang, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Weiming Shen* <br>
    <i>Knowledge-Based Systems <strong>(KBS).</strong></i> 2023.
  </li>
  <li id="OT-Pub1"> 
    Position encoding enhanced feature mapping for image anomaly detection <a href="https://ieeexplore.ieee.org/abstract/document/9926547">[Paper]</a> <a href="https://github.com/caoyunkang/PFM-and-PEFM-for-Image-Anomaly-Detection-and-Segmentation">[Code]</a> <br>
    Qian Wan, <span style="color:#b02418; font-weight:bold;">Yunkang Cao</span>, Liang Gao, Weiming Shen, Xinyu Li* <br>
    <i>IEEE International Conference on Automation Science and Engineering <strong>(IEEE CASE).</strong></i> 2022.
  </li>
</ol>



# 🥇 Selected Awards
- National Scholarship (**the highest scholarship for Ph.D.**), 2024.11
- Provincial Second Prize, China International College Students' Innovation Competition, 2024.08
- **2nd place** in [CVPR VAND Zero-shot Anomaly Detection Challenge](https://sites.google.com/view/vand-cvpr23/challenge)
- First-class Scholarship for Postgraduates, HUST, 2020.09, 2021.09, 2022.09
- Student Award for Research and Innovation, HUST, 2022.05
- **Mathematical Modeling Stars Nomination (TOP 2)** in the 18th China Post-graduate Mathematical Contest, 2022.05
- Merit Postgraduate student, HUST, 2021.09
- Excellent Graduates, HUST, 2019.06
- National Scholarship (**the highest scholarship for B.E**), 2017.09, 2019.09
- Second Class Prize, Undergraduate Electronics Design Contest, Provincial, 2018.09
- Third Class Prize, Undergraduate Intelligent Robotics Contest, National, 2018.05


# 🎓📚 Academic Service 
- **Executive Guest Editor**, *Pattern Recognition* (Elsevier), Special Issue on "Foundation Models for Anomaly Detection, Reasoning, and Recovery".
- *Journal Reviewer*, IEEE TSMC, IEEE TNNLS, IEEE TII, IEEE TKDE, IEEE TCSVT, IEEE TASE, PR, etc.
- *Conference Reviewer*, CVPR, ICCV, ECCV, AAAI, NeurIPS, ICLR, ICRA, IROS.
- *Co-organizer of special sessions*, <a href="https://adfmw.github.io/ijcai24/index.html">[Anomaly Detection with Foundation Models (ADFM)]</a> at IJCAI (2024).
- *Co-organizer of special sessions*, <a href="https://2024.ieeecase.org/special-sessions/">[Industrial Foundation Models and Applications in Smart Manufacturing]</a> at the IEEE International Conference on Automation Science and Engineering (2024).

# 💬 Invited Talks

- *2025.11.23*, Chongqing University (CQU), "Towards General Visual Anomaly Detection" (Invited by Prof. Yan Qin).
- *2025.11.07*, Central South University (CSU), "Towards General Visual Anomaly Detection" (Invited by Prof. Senzhang Wang).
- *2025.10.30*, Sun Yat-sen University (SYSU) & Tencent Youtu Lab, "Towards General Visual Anomaly Detection" (Invited by Prof. Chao Huang).
- *2025.10.12*, Xiangtan, "Towards General Visual Anomaly Detection".
- *2025.07.28*, Lanzhou, "Towards General Visual Anomaly Detection".
- *2024.07*, EPFL, "Application-Oriented Industrial Visual Anomaly Detection" <a href="https://drive.google.com/file/d/1quJnGImn981ZOGiGyvl59o9r6z8FivVO/view?usp=sharing">[Slides]</a>.
- *2023.11*, National University of Defense Technology (NUDT), "Overview of Image Anomaly Detection—Review, Applications, and Future Prospects" <a href="https://drive.google.com/file/d/1IBeVN-x-A_MO2iq6CQAm9f2XICVmkGZB/view?usp=drive_link">[Slides]</a>.


[comment]: <> (# 📖 Education)

[comment]: <> (- ### *2023.10 - 2024.10, Politecnico di Milano*)

[comment]: <> (  Department of Electronics, Information and Bioengineering                              )

[comment]: <> (  ***Visiting Ph.D.*** in Computer Science &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **Advisor**: [Giacomo Boracchi]&#40;https://boracchi.faculty.polimi.it/&#41;)
  
[comment]: <> (- ### *2020.09 - 2025.06, Huazhong University of Science and Technology*)

[comment]: <> (  State Key Laboratory of Digital Manufacturing Equipment and Technology                               )

[comment]: <> (  ***Ph.D. Candidate*** in Mechanical Engineering &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **Advisor**: [Weiming Shen]&#40;https://scholar.google.com/citations?hl=zh-CN&user=FuSHsx4AAAAJ&view_op=list_works&sortby=pubdate&#41;)
 
[comment]: <> (- ### *2016.09 - 2020.06, Huazhong University of Science and Technology*)

[comment]: <> (  ***B.S.*** in Mechanical Design, Manufacture & Automation &nbsp;&nbsp;&nbsp; )

[comment]: <> (# 📋 Work Experience)

[comment]: <> (- ### *2025.06 - Present, Hunan University*)

[comment]: <> (  ***Assistant Professor***, School of Artificial Intelligence and Robotics, Hunan University )
  

<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=300&t=tt&d=QltdrDBXR7cYztdXsLCBfSeruYl8EMVZ7i3zpSoGzP4&co=2d78ad&cmo=3acc3a&cmn=ff5353&ct=ffffff'></script>