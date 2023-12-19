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

Hello! I'm Yunkang CAO (曹云康), a Ph.D. candidate at [Huazhong University of Science and Technology (HUST)](http://english.hust.edu.cn), where I'm fortunate to be working under the guidance of [Prof. Weiming Shen](https://scholar.google.com.hk/citations?user=FuSHsx4AAAAJ&hl=en&oi=sra). I hold a bachelor's degree in Mechanical Design, Manufacture & Automation, also from HUST.

My academic interests revolve around **Deep Learning** and **Computer Vision**, with a specific focus on **Multi-modal Anomaly Detection**. Lately, my research has been centered on the application of foundational models like vision-language models in anomaly detection tasks, alongside my exploration of **Zero/Few-shot Anomaly Detection**.

I leverage these techniques to address challenges within the domain of **Industrial Inspection**, where my work is concentrated on advancing **Robotized Intelligent Manufacturing**. The primary goal is to develop swift and precise quality inspection solutions for large-scale multi-view objects.

If you find my research intriguing, please don't hesitate to get in touch with me. I welcome any inquiries or discussions regarding my work! 😊

# 🔥 News
- *2023.12*: &nbsp;🎉🎉 Our paper addressed [Semi-supervised Image Anomaly Detection]() is accepted by IEEE Transactions on Instrumentation and Measurement.
- *2023.12*: &nbsp;🎉🎉 Our paper addressed [Semi-supervised Image Anomaly Detection]() is accepted by IEEE Transactions on Systems, Man, and Cybernetics: Systems.
- *2023.11*: &nbsp;🎉🎉 We released [Towards Generic Anomaly Detection and Understanding: Large-scale Visual-linguistic Model (GPT-4V) Takes the Lead](https://arxiv.org/abs/2311.02782)
  [(Code)](https://github.com/caoyunkang/GPT4V-for-Generic-Anomaly-Detection), the first comprehensive evaluation on GPT-4V for generic anomaly detection.
- *2023.09*: &nbsp;🎉🎉 Our paper addressed [Unsupervised Image Anomaly Detection](https://www.sciencedirect.com/science/article/abs/pii/S0950705123007323) is accepted by Knowledge-based Systems.
- *2023.06*: &nbsp;🎉🎉 We won the 2nd place in [CVPR VAND Zero-shot Anomaly Detection Challenge](https://sites.google.com/view/vand-cvpr23/challenge).
- *2023.05*: &nbsp;🎉🎉 We released **Segment Any Anomaly without Training via Hybrid Prompt Regularization** [(Paper)]((http://arxiv.org/abs/2305.10724)) [(Code)](https://github.com/caoyunkang/Segment-Any-Anomaly) for zero-shot anomaly segmentation.
- *2023.05*: &nbsp;🎉🎉 Our paper addressed [High-Resolution Image Anomaly Detection](https://ieeexplore.ieee.org/abstract/document/10260338) has been accepted by IEEE CASE 2023.
- *2023.03*: &nbsp;🎉🎉 We released [Complementary Pseudo Multimodal Feature for Point Cloud Anomaly Detection](https://arxiv.org/abs/2303.13194) for point cloud anomaly detection.
- *2023.01*: &nbsp;🎉🎉 Our paper addressed [Unsupervised Image Anomaly Detection](https://ieeexplore.ieee.org/document/10034849) is accepted by IEEE TII.
- *2022.09*: &nbsp;🎉🎉 One paper is accepted by Knowledge-based Systems.
- *2022.05*: &nbsp;🎉🎉 One paper is accepted by IEEE CASE 2022.
- *2022.05*: &nbsp;🎉🎉 We get **The Mathematical Modeling Stars Nomination** in the 18th China Post-graduate Mathematical Contest.
- *2022.03*: &nbsp;🎉🎉 Two papers are accepted by IEEE CSCWD 2022.
- *2022.03*: &nbsp;🎉🎉 Our paper addressed [Unsupervised Image Anomaly Detection](https://www.sciencedirect.com/science/article/pii/S0950705122004038) is accepted by Knowledge-based Systems.


# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">TSMC</div><img src='./images/TSMC.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## BiaS: Incorporating Biased Knowledge to Boost Unsupervised Image Anomaly Localization

**Yunkang Cao**, Xiaohao Xu, Chen Sun, Liang Gao, and Weiming Shen*.

IEEE Transactions on Systems, Man, and Cybernetics: Systems.

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv</div><img src='./images/generic-ad.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Towards Generic Anomaly Detection and Understanding: Large-scale Visual-linguistic Model (GPT-4V) Takes the Lead

**Yunkang Cao**, Xiaohao Xu, Chen Sun, Xiaonan Huang, Weiming Shen*.

<div class="extra-links">
    <a class="_blank" href="https://arxiv.org/abs/2311.02782" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="https://github.com/caoyunkang/GPT4V-for-Generic-Anomaly-Detection">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">KBS</div><img src='./images/MaskedTeacher.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## A Masked Reverse Knowledge Distillation Method Incorporating Global and Local Information for Image Anomaly Detection

Yuxin Jiang, **Yunkang Cao**, Weiming Shen*

Knowledge-based Systems

<div class="extra-links">
    <a class="_blank" href="https://www.sciencedirect.com/science/article/pii/S0950705123007323" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
</div>

</div>
</div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv</div><img src='./images/SAA.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Segment Any Anomaly without Training via Hybrid Prompt Regularization

**Yunkang Cao**, Xiaohao Xu, Chen Sun, Yuqi Cheng, Zongwei Du, Liang Gao, and Weiming Shen*

<div class="extra-links">
    <a class="_blank" href="http://arxiv.org/abs/2305.10724" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="https://github.com/caoyunkang/Segment-Any-Anomaly">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">PR</div><img src='./images/CPMF.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Complementary Pseudo Multimodal Feature for Point Cloud Anomaly Detection

**Yunkang Cao**, Xiaohao Xu, Weiming Shen*

Pattern Recognition, Under Review

<div class="extra-links">
    <a class="_blank" href="https://arxiv.org/ftp/arxiv/papers/2303/2303.13194.pdf" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="https://github.com/caoyunkang/CPMF">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>

</div>
</div>




<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CASE 2023</div><img src='./images/CASE2023.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## High-Resolution Image Anomaly Detection via Spatiotemporal Consistency Incorporated Knowledge Distillation

**Yunkang Cao**, Yiheng Zhang, Weiming Shen*

IEEE International Conference on Automation Science and Engineering 2023 (IEEE CASE 2023)
<div class="extra-links">
    <a class="_blank" href="https://ieeexplore.ieee.org/abstract/document/10260338" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">TII</div><img src='./images/TII-CDO-2023-01.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Collaborative Discrepancy Optimization for Reliable Image Anomaly Localization 

**Yunkang Cao**, Xiaohao Xu, Zhaoge Liu, Weiming Shen*

IEEE Transactions on Industrial Informatics

<div class="extra-links">
    <a class="_blank" href="https://ieeexplore.ieee.org/document/10034849" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="https://github.com/caoyunkang/CDO">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">KBS</div><img src='./images/KBS-2022-3.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Informative Knowledge Distillation for image anomaly detection

**Yunkang Cao**, Qian Wan, Weiming Shen* and Liang Gao

Knowledge-based Systems

<div class="extra-links">
    <a class="_blank" href="https://www.sciencedirect.com/science/article/pii/S0950705122004038" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="https://github.com/caoyunkang/IKD">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>
</div>
</div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">KBS</div><img src='./images/KBS-2022-8.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## GON: End-to-end Optimization Framework for Constraint Graph Optimization Problems

Chuan Liu, Jingwei Wang, **Yunkang Cao**, Min Liu, Weiming Shen*

Knowledge-based Systems

<div class="extra-links">
    <a class="_blank" href="https://www.sciencedirect.com/science/article/pii/S0950705122008590" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
</div>
</div>
</div>



<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CSCWD 2022</div><img src='./images/CSCWD2022-1.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Semi-supervised Knowledge Distillation for Tiny Defect Detection

**Yunkang Cao**, Yanan Song, Xiaohao Xu, Shuya Li, Yuhao Yu, Yiheng Zhang, Weiming Shen*

IEEE International Conference on Computer Supported Cooperative Work in Design 2022 (IEEE CSCWD 2022)

<div class="extra-links">
    <a class="_blank" href="https://ieeexplore.ieee.org/document/9776026" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
</div>
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CASE 2022</div><img src='./images/CASE2022.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Position Encoding Enhanced Feature Mapping for Image Anomaly Detection

Qian Wan, **Yunkang Cao**, Liang Gao, Weiming Shen, Xinyu Li*

IEEE International Conference on Automation Science and Engineering 2022 (IEEE CASE 2022)

<div class="extra-links">
    <a class="_blank" href="https://www.researchgate.net/publication/361254312_Position_Encoding_Enhanced_Feature_Mapping_for_Image_Anomaly_Detection" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
    <a class="_blank" href="https://github.com/caoyunkang/PFM-and-PEFM-for-Image-Anomaly-Detection-and-Segmentation">
        <i class="ai ai-open-access ai-1x" aria-hidden="true"></i> Code
    </a>
</div>
</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CSCWD 2022</div><img src='./images/CSCWD2022-2.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## An Outlier-Aware Method for UWB Indoor Positioning in NLoS Situations

Chuan Liu, **Yunkang Cao**, Chen Sun, Weiming Shen*, Xinyu Li and Liang Gao

IEEE International Conference on Computer Supported Cooperative Work in Design 2022 (IEEE CSCWD 2022)

<div class="extra-links">
    <a class="_blank" href="https://ieeexplore.ieee.org/document/9776125" >
        <i class="fas fa-newspaper" aria-hidden="true"></i> Paper
    </a>
</div>
</div>
</div>

# 💻 Projects

<div class='paper-box'><div class='paper-box-image'><div><img src='./images/RobotDet.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

## Multi-View Industrial Inspection with Robot Arms

Robot assisted Industrial inspection for workpieces with curved and reflective surfaces (e.g. [VR glasses](../images/VR.png), Car's steering wheel covers)
</div>
</div>

# 🥇 Selected Awards
- **2nd place** in [CVPR VAND Zero-shot Anomaly Detection Challenge](https://sites.google.com/view/vand-cvpr23/challenge)
- First-class Scholarship for Postgraduates, HUST, 2020.09, 2021.09, 2022.09
- Student Award for Research and Innovation, 2022.05
- **Mathematical Modeling Stars Nomination (TOP 2)** in the 18th China Post-graduate Mathematical Contest, 2022.05
- Merit Postgraduate student, HUST, 2021.09
- Excellent Graduates, HUST, 2019.06
- National Scholarship (**the highest scholarship for B.E**), 2017.09, 2019.09

# 💬 Invited Talks
- *2023.11*, "Overview of Image Anomaly Detection—Review, Applications, and Future Prospects", Talk with Professor [Kevin Xu's](https://kevinkaixu.net/) group at the National University of Defense Technology.


# 📖 Educations
- ### *2020.09 - present, Huazhong University of Science and Technology*
  State Key Laboratory of Digital Manufacturing Equipment and Technology                               
  ***Ph.D. Candidate*** in Mechanical Engineering &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **Advisor**: Weiming Shen
 
- ### *2016.09 - 2020.06, Huazhong University of Science and Technology*
  ***B.S.*** in Mechanical Design, Manufacture & Automation &nbsp;&nbsp;&nbsp; 
  
<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=300&t=tt&d=QltdrDBXR7cYztdXsLCBfSeruYl8EMVZ7i3zpSoGzP4&co=2d78ad&cmo=3acc3a&cmn=ff5353&ct=ffffff'></script>  
<!-- Thesis: pass -->

<!-- # 💬 Invited Talks
- *2021.06*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.03*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  \| [\[video\]](https://github.com/)

# 💻 Internships
- *2019.05 - 2020.02*, [Lorem](https://github.com/), China. -->