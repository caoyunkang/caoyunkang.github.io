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

<div class="profile-lead">
  <p class="role-line lang-en"><i class="fas fa-user-graduate" aria-hidden="true"></i> Assistant Professor / Associate Research Fellow / Ph.D. Supervisor / Deputy Director of the Department of Robotics Engineering</p>
  <p class="role-line cn lang-zh"><i class="fas fa-user-graduate" aria-hidden="true"></i> 助理教授 / 副研究员 / 博士生导师 / 机器人工程系副主任</p>
  <div class="profile-meta">
    <span class="lang-en"><i class="fas fa-university" aria-hidden="true"></i> School of Artificial Intelligence and Robotics, Hunan University</span>
    <span class="lang-zh"><i class="fas fa-university" aria-hidden="true"></i> 湖南大学人工智能与机器人学院</span>
    <span><i class="fas fa-envelope" aria-hidden="true"></i> <a href="mailto:caoyunkang0207@gmail.com">caoyunkang0207@gmail.com</a></span>
    <span class="lang-en"><i class="fas fa-map-marker-alt" aria-hidden="true"></i> Room C1-310, Taizihu Campus, Hunan University</span>
    <span class="lang-zh"><i class="fas fa-map-marker-alt" aria-hidden="true"></i> 湖南大学桃子湖校区人工智能与机器人学院 C1-310</span>
  </div>
  <div class="profile-links">
    <a href="https://scholar.google.com/citations?user=aLJ8_G4AAAAJ&hl=zh-CN"><i class="ai ai-google-scholar" aria-hidden="true"></i> Google Scholar</a>
    <a href="https://github.com/caoyunkang"><i class="fab fa-github" aria-hidden="true"></i> GitHub</a>
  </div>
</div>

<div class="language-toggle" role="group" aria-label="Language selector">
  <button type="button" data-lang-switch="zh">中文</button>
  <button type="button" data-lang-switch="en">English</button>
</div>

<nav class="quick-nav" aria-label="Quick links">
  <a href="#about"><i class="fas fa-id-card" aria-hidden="true"></i><span class="lang-en">About</span><span class="lang-zh">基本情况</span></a>
  <a href="#openings"><i class="fas fa-user-plus" aria-hidden="true"></i><span class="lang-en">Openings</span><span class="lang-zh">招生</span></a>
  <a href="#research"><i class="fas fa-microscope" aria-hidden="true"></i><span class="lang-en">Research</span><span class="lang-zh">研究方向</span></a>
  <a href="#works"><i class="fas fa-layer-group" aria-hidden="true"></i><span class="lang-en">Works</span><span class="lang-zh">代表成果</span></a>
  <a href="#projects"><i class="fas fa-tasks" aria-hidden="true"></i><span class="lang-en">Projects</span><span class="lang-zh">科研项目</span></a>
  <a href="#teaching"><i class="fas fa-chalkboard-teacher" aria-hidden="true"></i><span class="lang-en">Teaching</span><span class="lang-zh">课程</span></a>
  <a href="#publications"><i class="fas fa-book-open" aria-hidden="true"></i><span class="lang-en">Publications</span><span class="lang-zh">代表论文</span></a>
  <a href="#service"><i class="fas fa-hands-helping" aria-hidden="true"></i><span class="lang-en">Service</span><span class="lang-zh">学术服务</span></a>
</nav>

<script>
(function () {
  var params = new URLSearchParams(window.location.search);
  var initialLang = params.get("lang") === "en" ? "en" : "zh";
  var root = document.documentElement;
  var mainNavLabels = {
    "/#about-me": { zh: "首页", en: "About" },
    "../files/CV_Yunkang_CAO.pdf": { zh: "简历", en: "CV" },
    "/#openings": { zh: "招生", en: "Openings" },
    "/#research": { zh: "研究方向", en: "Research" },
    "/#works": { zh: "代表成果", en: "Works" },
    "/#publications": { zh: "代表论文", en: "Publications" },
    "/#service": { zh: "学术服务", en: "Service" }
  };

  function updateMainNav(lang) {
    document.querySelectorAll(".masthead a[href], .greedy-nav a[href]").forEach(function (link) {
      var labels = mainNavLabels[link.getAttribute("href")];
      if (labels) {
        link.textContent = labels[lang];
      }
    });
  }

  function setLanguage(lang, updateUrl) {
    var nextLang = lang === "en" ? "en" : "zh";
    root.setAttribute("data-lang", nextLang);
    root.setAttribute("lang", nextLang === "en" ? "en" : "zh-CN");
    updateMainNav(nextLang);

    document.querySelectorAll("[data-lang-switch]").forEach(function (button) {
      var isActive = button.getAttribute("data-lang-switch") === nextLang;
      button.classList.toggle("is-active", isActive);
      button.setAttribute("aria-pressed", isActive ? "true" : "false");
    });

    if (updateUrl && window.history && window.history.replaceState) {
      var url = new URL(window.location.href);
      if (nextLang === "en") {
        url.searchParams.set("lang", "en");
      } else {
        url.searchParams.delete("lang");
      }
      window.history.replaceState({}, "", url.pathname + url.search + url.hash);
    }
  }

  root.setAttribute("data-lang", initialLang);
  root.setAttribute("lang", initialLang === "en" ? "en" : "zh-CN");

  document.addEventListener("DOMContentLoaded", function () {
    setLanguage(initialLang, false);
    document.querySelectorAll("[data-lang-switch]").forEach(function (button) {
      button.addEventListener("click", function () {
        setLanguage(button.getAttribute("data-lang-switch"), true);
      });
    });
  });
})();
</script>

<style>
html:not([data-lang="en"]) .lang-en {
  display: none !important;
}

html[data-lang="en"] .lang-zh {
  display: none !important;
}

.profile-lead {
  border-left: 4px solid #365f91;
  margin: 0.8rem 0 1rem;
  padding: 0.1rem 0 0.1rem 1rem;
}

.role-line {
  font-weight: 700;
  margin: 0 0 0.3rem;
}

.role-line i,
.profile-meta i,
.profile-links i,
.quick-nav i,
.section-icon {
  color: #365f91;
  margin-right: 0.35rem;
}

.role-line.cn {
  color: #38485c;
}

.profile-meta {
  display: grid;
  gap: 0.25rem;
  margin: 0.75rem 0;
}

.profile-meta span {
  align-items: baseline;
  display: flex;
  line-height: 1.55;
}

.profile-meta i {
  flex: 0 0 1.15rem;
  text-align: center;
}

.profile-links,
.quick-nav {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
}

.language-toggle {
  display: flex;
  gap: 0.35rem;
  justify-content: flex-end;
  margin: 0.85rem 0 0.7rem;
}

.language-toggle button {
  background: #fff;
  border: 1px solid #d8e1ed;
  border-radius: 999px;
  color: #365f91;
  cursor: pointer;
  font-size: 0.86rem;
  font-weight: 700;
  line-height: 1;
  padding: 0.42rem 0.75rem;
}

.language-toggle button.is-active {
  background: #365f91;
  border-color: #365f91;
  color: #fff;
}

.profile-links a,
.quick-nav a {
  align-items: center;
  border: 1px solid #d8e1ed;
  border-radius: 6px;
  display: inline-flex;
  line-height: 1.2;
  padding: 0.36rem 0.55rem;
  text-decoration: none;
}

.profile-links a:hover,
.quick-nav a:hover {
  background: #f4f7fb;
}

.section-icon {
  display: inline-block;
  width: 1.2rem;
}

.opening-highlight {
  background: #fff7f5;
  border: 1px solid #efcbc4;
  border-left: 4px solid #b02418;
  border-radius: 8px;
  color: #8f1d14;
  font-weight: 700;
  margin: 0.8rem 0 1rem;
  padding: 0.72rem 0.9rem;
}

.opening-highlight p {
  margin: 0 0 0.35rem;
}

.opening-highlight p:last-child {
  margin-bottom: 0;
}

.opening-highlight i,
.news-icon,
.work-kicker i {
  color: #365f91;
  margin-right: 0.35rem;
}

.opening-highlight i {
  color: #b02418;
}

.metrics-grid {
  display: grid;
  gap: 0.7rem;
  grid-template-columns: repeat(auto-fit, minmax(135px, 1fr));
  margin: 1rem 0;
}

.metric-item {
  border: 1px solid #d8e1ed;
  border-radius: 8px;
  padding: 0.65rem 0.75rem;
}

.metric-item i {
  color: #365f91;
  margin-right: 0.35rem;
}

.metric-item strong {
  color: #22364f;
  display: inline-block;
  font-size: 1.18rem;
  margin-right: 0.2rem;
}

.metric-item span {
  color: #526171;
  display: block;
  font-size: 0.86rem;
  margin-top: 0.15rem;
}

.works-grid {
  display: grid;
  gap: 14px;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  margin: 1rem 0 1.6rem;
}

.work-card {
  background: #fff;
  border: 1px solid #d9e1ec;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.work-card img {
  background: #f7f9fc;
  border-bottom: 1px solid #e4eaf2;
  height: 210px;
  object-fit: contain;
  width: 100%;
}

.work-body {
  display: flex;
  flex: 1;
  flex-direction: column;
  padding: 12px 14px 14px;
}

.work-kicker {
  color: #365f91;
  font-size: 0.82rem;
  font-weight: 700;
  margin: 0 0 6px;
}

.work-body h3 {
  font-size: 1.05rem;
  margin: 0 0 8px;
}

.work-body p {
  line-height: 1.55;
  margin: 0 0 8px;
}

.work-links {
  font-weight: 700;
  margin-top: auto;
}

@media (max-width: 560px) {
  .work-card img {
    height: 180px;
  }
}
</style>

-----

<span class='anchor' id='about'></span>

# <i class="fas fa-id-card section-icon" aria-hidden="true"></i><span class="lang-en">About</span><span class="lang-zh">基本情况</span>

I am an Assistant Professor and Ph.D. supervisor at the [School of Artificial Intelligence and Robotics, Hunan University (HNU)](http://robotics.hnu.edu.cn/), an Associate Research Fellow at the National Engineering Research Center of Robot Visual Perception and Control Technology, and Deputy Director of the Department of Robotics Engineering. I am a core member of the research team led by [Yaonan Wang (王耀南院士)](https://robotics.hnu.edu.cn/info/1176/3098.htm) and [Hui Zhang (张辉院长)](https://robotics.hnu.edu.cn/info/1176/2966.htm).
{: .lang-en}

曹云康，博士，湖南大学人工智能与机器人学院助理教授、博士生导师，机器人视觉感知与控制技术国家工程研究中心副研究员，兼任机器人工程系副主任，王耀南院士、张辉院长团队核心成员。
{: .lang-zh}

My research focuses on industrial visual inspection, multimodal foundation models, and robotic embodied perception. I aim to move industrial inspection systems from defect detection toward anomaly understanding, cause analysis, active inspection, and autonomous recovery. The long-term goal is to build deployable perception and reasoning systems for intelligent manufacturing, intelligent breeding, and other real-world industrial scenarios.
{: .lang-en}

本人主要从事工业视觉检测、多模态基础模型与机器人具身感知研究，重点关注工业检测系统如何从“发现缺陷”走向“理解异常、分析成因、主动巡检和自主恢复”。相关研究面向智能制造、智能育种等实际场景，致力于发展可部署、可解释、可闭环运行的工业感知与推理技术。
{: .lang-zh}

My work is organized around four connected directions: anomaly generation, anomaly detection, anomaly understanding, and embodied perception for industrial inspection. Representative outcomes include Anomagic for anomaly generation, IAD-R1 for industrial anomaly reasoning, and INP-Former for universal visual anomaly detection. INP-Former was adopted as a core method by four of the top five teams in the CVPR VAND Challenge.
{: .lang-en}

研究工作围绕异常生成、异常检测、异常理解与具身感知四条主线展开，已形成异常生成方法 Anomagic、工业异常推理模型 IAD-R1，以及面向通用视觉异常检测的 INP-Former 等代表性成果。其中，INP-Former 被 CVPR VAND 挑战赛前五名中的四支队伍采用为核心方法。
{: .lang-zh}

I have published more than 60 papers in journals and conferences including IEEE TCYB, IEEE TII, IEEE TSMC, Pattern Recognition, CVPR, ECCV, AAAI, IJCAI, and ICCV Workshop. My work has received over 2,100 Google Scholar citations with an H-index of 21. I have published 17 papers as first or corresponding author, and two papers have been selected as ESI Highly Cited Papers.
{: .lang-en}

近年来在 IEEE TCYB、IEEE TII、IEEE TSMC、Pattern Recognition 等国际期刊及 CVPR、ECCV、AAAI、IJCAI、ICCV Workshop 等会议发表论文 60 余篇，Google Scholar 引用 2100 余次，H 指数 21；其中以第一作者或通讯作者发表论文 17 篇，2 篇入选 ESI 高被引论文。
{: .lang-zh}

<div class="metrics-grid">
  <div class="metric-item"><i class="fas fa-file-alt" aria-hidden="true"></i><strong>60+</strong><span class="lang-en">Publications</span><span class="lang-zh">论文</span></div>
  <div class="metric-item"><i class="fas fa-quote-right" aria-hidden="true"></i><strong>2100+</strong><span class="lang-en">Citations</span><span class="lang-zh">引用</span></div>
  <div class="metric-item"><i class="fas fa-chart-line" aria-hidden="true"></i><strong>21</strong><span class="lang-en">H-index</span><span class="lang-zh">H 指数</span></div>
  <div class="metric-item"><i class="fas fa-user-edit" aria-hidden="true"></i><strong>17</strong><span class="lang-en">First or Corresponding</span><span class="lang-zh">一作或通讯</span></div>
</div>

In technology transfer, I have led or participated in projects supported by Yuelushan Laboratory, central university research funds, key laboratory open funds, and industrial partners. The developed defect generation and multimodal open-set detection algorithms have been integrated into the SEER Robotics Xiangyun algorithm platform and deployed in core manufacturing scenarios through industry collaborations.
{: .lang-en}

在应用转化方面，主持岳麓山实验室种业专项、中央高校基本科研基金、教育部重点实验室开放基金及多项企业委托项目，并作为核心成员参与国家自然科学基金重大项目“跨物种多感官多粒度仿生感知”。相关缺陷生成与多模态开集检测算法已集成到视比特机器人翔云算法平台，并用于多项行业合作中的核心制造环节。
{: .lang-zh}

I serve on the editorial board of *Pattern Recognition* and lead the Special Issue on "Foundation Models for Anomaly Detection, Reasoning, and Recovery." I also review for more than twenty journals and conferences, including TPAMI, IJCV, CVPR, and NeurIPS. I have organized or co-organized workshops, special sessions, and forums on industrial inspection, anomaly detection, foundation models, and embodied perception.
{: .lang-en}

在学术服务方面，担任中科院一区期刊 Pattern Recognition 编委，牵头组织“面向缺陷检测、推理与修复的基础模型”专题特刊；长期担任 TPAMI、IJCV、CVPR、NeurIPS 等二十余个期刊与会议审稿人，并围绕工业检测、异常检测、基础模型与具身感知等主题组织国际研讨会和专题论坛。
{: .lang-zh}

-----

<span class='anchor' id='experience'></span>

# <i class="fas fa-graduation-cap section-icon" aria-hidden="true"></i><span class="lang-en">Education and Experience</span><span class="lang-zh">学习与工作经历</span>

<ul>
  <li><span class="lang-en"><strong>2025.05 - Present</strong>, Assistant Professor / Associate Research Fellow, School of Artificial Intelligence and Robotics, Hunan University.</span><span class="lang-zh"><strong>2025.05 至今</strong>，湖南大学，人工智能与机器人学院，助理教授 / 副研究员。</span></li>
  <li><span class="lang-en"><strong>2020.09 - 2025.06</strong>, Ph.D. in Mechanical Engineering, Huazhong University of Science and Technology. Advisor: <a href="https://scholar.google.com.hk/citations?user=FuSHsx4AAAAJ&hl=en&oi=sra">Prof. Weiming Shen</a>.</span><span class="lang-zh"><strong>2020.09 - 2025.06</strong>，华中科技大学，机械工程，博士，导师：沈卫明教授。</span></li>
  <li><span class="lang-en"><strong>2023.10 - 2024.10</strong>, Visiting Ph.D. Researcher, Politecnico di Milano. Host: <a href="https://boracchi.faculty.polimi.it/">Prof. Giacomo Boracchi</a>.</span><span class="lang-zh"><strong>2023.10 - 2024.10</strong>，米兰理工大学，计算机科学，访问博士，导师：Giacomo Boracchi。</span></li>
  <li><span class="lang-en"><strong>2016.09 - 2020.06</strong>, B.E. in Mechanical Design, Manufacturing and Automation, Huazhong University of Science and Technology.</span><span class="lang-zh"><strong>2016.09 - 2020.06</strong>，华中科技大学，机械设计制造及其自动化，学士。</span></li>
</ul>

-----

<span class='anchor' id='openings'></span>

# <i class="fas fa-user-plus section-icon" aria-hidden="true"></i><span class="lang-en">Openings and Mentoring</span><span class="lang-zh">招生与培养理念</span>

<div class="opening-highlight">
<p class="lang-en"><i class="fas fa-bullhorn" aria-hidden="true"></i>Openings: I am recruiting master's students, research assistants, and visiting students. Strong undergraduates are welcome to join early for research training.</p>
<p class="lang-zh"><i class="fas fa-bullhorn" aria-hidden="true"></i>招生：长期招收硕士研究生、研究助理和访问学生。也欢迎数理基础扎实、愿意认真做科研的本科生提前进组学习。欢迎对人工智能、计算机视觉、具身智能、机器人、工业视觉检测和多模态大模型感兴趣的同学联系。</p>
</div>

I value careful problem formulation, solid implementation, and steady research training. New members will receive close guidance throughout their first project, from reading papers and designing experiments to writing code, preparing manuscripts, and responding to reviewers.
{: .lang-en}

课题组注重把问题凝练、代码实现、实验复现和论文写作打通。新成员入组后，将围绕第一个课题接受系统训练，包括文献阅读、实验设计、代码实现、论文撰写、投稿修改和学术交流，逐步培养独立开展研究的能力。
{: .lang-zh}

I have advised students in national-level undergraduate innovation training projects and key-area support projects. Student work has received Best Student Paper Awards at CSCWD 2025 and ICAIS & ISAS 2026.
{: .lang-en}

目前已指导学生获批国家级大学生创新训练项目和重点领域支持项目，并获得 IEEE CSCWD 2025 Best Student Paper Award、ICAIS & ISAS 2026 Best Student Paper Award。
{: .lang-zh}

The group maintains collaborations with the University of Oxford, Politecnico di Milano, Tsinghua University, Huazhong University of Science and Technology, Huawei, Tencent Youtu Lab, CATL, SEER Robotics, and other academic and industrial partners. Students will have opportunities to work on real industrial scenarios, participate in technology transfer, and attend leading conferences such as CVPR, ICCV, AAAI, and IJCAI.
{: .lang-en}

课题组与牛津大学、米兰理工大学、清华大学、华中科技大学等国内外高校保持合作，并与华为、腾讯优图、宁德时代、视比特机器人等企业建立合作关系。学生有机会参与真实工业项目，接触技术转化和工程落地过程，也鼓励参加 CVPR、ICCV、AAAI、IJCAI 等国际会议，拓展学术视野。
{: .lang-zh}

**Contact**: Please send your CV to [caoyunkang0207@gmail.com](mailto:caoyunkang0207@gmail.com). Please briefly describe your research interests, prior experience, technical skills, and future research thoughts in the email.
{: .lang-en}

联系时请先阅读“研究方向介绍”和代表性成果，并在邮件中简要说明研究兴趣、过往经历、技能基础及未来科研思考，便于后续沟通。
{: .lang-zh}

-----

<span class='anchor' id='research'></span>

# <i class="fas fa-microscope section-icon" aria-hidden="true"></i><span class="lang-en">Research Directions</span><span class="lang-zh">研究方向</span>

The group studies four connected problems in industrial inspection: anomaly generation, anomaly detection, anomaly understanding, and embodied perception. The aim is to build systems that learn from limited defect data, generalize across open industrial environments, and connect perception with robotic inspection and recovery.
{: .lang-en}

课题组围绕工业检测中的异常生成、异常检测、异常理解和具身感知开展研究。我们关注缺陷样本少、场景开放、工况变化大等实际问题，希望在这些约束下建立易训练、泛化能力强、便于部署的检测系统，并将其接入机器人主动巡检和异常恢复流程。
{: .lang-zh}

## <i class="fas fa-magic section-icon" aria-hidden="true"></i><span class="lang-en">1. Anomaly Generation</span><span class="lang-zh">1. 异常生成</span>

We build controllable anomaly generation methods for industrial inspection, including diffusion-based synthesis, multimodal prompt-driven generation, and defect transfer. The goal is to create realistic and diverse defects for detector training, benchmarking, and failure-case analysis when real anomaly data are scarce.
{: .lang-en}

针对工业现场缺陷样本少、异常形态难以穷举的问题，研究生成式模型、扩散模型和多模态提示驱动的异常生成方法，按需生成真实、多样、可控制的缺陷样本，用于检测模型训练、评测集构建和长尾异常分析，降低工业检测对真实缺陷数据的依赖。
{: .lang-zh}

## <i class="fas fa-search section-icon" aria-hidden="true"></i><span class="lang-en">2. Anomaly Detection</span><span class="lang-zh">2. 异常检测</span>

We develop unsupervised, few-shot, and zero-shot anomaly detection methods for industrial images, point clouds, 3D geometry, and multi-view inspection. The focus is on foundation models, vision-language models, normal prototype modeling, high-resolution localization, and robust generalization across products, defect types, and production sites.
{: .lang-en}

研究在正常样本有限、甚至没有目标域样本时发现未知异常的方法，覆盖 2D 图像、点云、3D 几何和多视角检测。重点关注基础模型、视觉语言模型、正常原型建模、高分辨率细粒度定位和跨产品泛化，使模型面对新产线、新类别和新缺陷时仍能稳定工作。代表性成果包括首届 CVPR VAND 挑战赛全球亚军方法 Segment Any Anomaly，以及被多支获奖队伍采用的 INP-Former。
{: .lang-zh}

## <i class="fas fa-brain section-icon" aria-hidden="true"></i><span class="lang-en">3. Anomaly Understanding</span><span class="lang-zh">3. 异常理解</span>

We study multimodal anomaly understanding with large models. Beyond anomaly scores and heatmaps, the goal is to describe anomaly appearance, identify semantic attributes, infer possible causes, and provide information that engineers can verify and act on.
{: .lang-en}

异常理解关注检测结果之后的“为什么”和“怎么办”。在多模态大模型基础上，研究异常描述、属性识别、成因线索推断、处置建议和检测报告生成，使系统不只输出分数或热力图，还能说明异常现象和可能原因，帮助工程人员复核与决策。
{: .lang-zh}

## <i class="fas fa-robot section-icon" aria-hidden="true"></i><span class="lang-en">4. Embodied Perception</span><span class="lang-zh">4. 具身感知</span>

We integrate anomaly detection and anomaly understanding into robots and unmanned inspection systems. The aim is to let robots actively plan viewpoints and paths, gather multi-view and multimodal evidence, re-check suspicious regions, discover anomalies in open industrial sites, and support localization, recording, alerts, and recovery.
{: .lang-en}

具身感知强调把检测、理解能力与机器人主动行动结合起来。我们将异常检测和异常理解能力集成到机器人与无人巡检系统中，使其能够围绕检测任务主动规划视角和路径，采集多视角、多模态信息，在开放工业现场发现异常、复核疑似区域，并为定位、记录、报警和自主恢复提供依据。
{: .lang-zh}

-----

<span class='anchor' id='works'></span>

# <i class="fas fa-layer-group section-icon" aria-hidden="true"></i><span class="lang-en">Representative Works</span><span class="lang-zh">代表性成果</span>

The following works illustrate the current research line from anomaly generation and detection to understanding and embodied inspection.
{: .lang-en}

这里展示几项代表性成果，呈现课题组从异常生成、异常检测到异常理解和机器人主动巡检的研究脉络。
{: .lang-zh}

<div class="works-grid">
  <article class="work-card">
    <a href="https://github.com/yuxin-jiang/Anomagic" target="_blank" rel="noopener">
      <img src="/images/works/anomagic.webp" alt="Anomagic framework">
    </a>
    <div class="work-body">
      <p class="work-kicker"><i class="fas fa-magic" aria-hidden="true"></i><span class="lang-en">Anomaly Generation</span><span class="lang-zh">异常生成</span></p>
      <h3>Anomagic</h3>
      <p class="lang-en">Crossmodal prompt-driven zero-shot anomaly generation for controllable defect synthesis.</p>
      <p class="lang-zh">面向零样本异常生成，用视觉和文本提示共同控制缺陷合成，为检测、分割和推理模型提供可合成的异常样本。</p>
      <p class="work-links"><a href="https://github.com/yuxin-jiang/Anomagic" target="_blank" rel="noopener">Repository</a></p>
    </div>
  </article>

  <article class="work-card">
    <a href="https://github.com/hustCYQ/Synthesis4AD" target="_blank" rel="noopener">
      <img src="/images/works/synthesis4ad.webp" alt="Synthesis4AD system pipeline">
    </a>
    <div class="work-body">
      <p class="work-kicker"><i class="fas fa-cubes" aria-hidden="true"></i><span class="lang-en">Anomaly Generation</span><span class="lang-zh">3D 缺陷合成</span></p>
      <h3>Synthesis4AD</h3>
      <p class="lang-en">A practical pipeline for 3D anomaly synthesis, model training, and online inference in industrial inspection.</p>
      <p class="lang-zh">围绕 3D 缺陷合成、检测模型训练和在线推理构建流程，把“合成数据”接入可部署的工业检测系统。</p>
      <p class="work-links"><a href="https://github.com/hustCYQ/Synthesis4AD" target="_blank" rel="noopener">Repository</a></p>
    </div>
  </article>

  <article class="work-card">
    <a href="https://github.com/luow23/INP-Former" target="_blank" rel="noopener">
      <img src="/images/works/inp-former.webp" alt="INP-Former framework">
    </a>
    <div class="work-body">
      <p class="work-kicker"><i class="fas fa-search" aria-hidden="true"></i><span class="lang-en">Anomaly Detection</span><span class="lang-zh">通用异常检测</span></p>
      <h3>INP-Former</h3>
      <p class="lang-en">Intrinsic normal prototypes extracted from a single image for universal anomaly detection.</p>
      <p class="lang-zh">从单张图像中挖掘内在正常原型，用于跨类别、跨场景的通用异常检测，并被 CVPR VAND 多支获奖队伍采用。</p>
      <p class="work-links"><a href="https://github.com/luow23/INP-Former" target="_blank" rel="noopener">Repository</a></p>
    </div>
  </article>

  <article class="work-card">
    <a href="https://hustcyq.github.io/M2AD/" target="_blank" rel="noopener">
      <img src="/images/works/m2ad.webp" alt="M2AD dataset examples">
    </a>
    <div class="work-body">
      <p class="work-kicker"><i class="fas fa-database" aria-hidden="true"></i><span class="lang-en">Benchmark</span><span class="lang-zh">多视角多光照检测</span></p>
      <h3>M2AD</h3>
      <p class="lang-en">A large-scale benchmark for visual anomaly detection under coupled view and illumination changes.</p>
      <p class="lang-zh">面向真实部署中常见的视角和光照变化，构建多视角、多光照工业异常检测数据集，用于检验模型在复杂成像条件下的鲁棒性。</p>
      <p class="work-links"><a href="https://hustcyq.github.io/M2AD/" target="_blank" rel="noopener"><span class="lang-en">Project Page</span><span class="lang-zh">项目主页</span></a></p>
    </div>
  </article>

  <article class="work-card">
    <a href="https://github.com/Yanhui-Lee/IAD-R1" target="_blank" rel="noopener">
      <img src="/images/works/iad-r1.webp" alt="IAD-R1 overview">
    </a>
    <div class="work-body">
      <p class="work-kicker"><i class="fas fa-brain" aria-hidden="true"></i><span class="lang-en">Anomaly Understanding</span><span class="lang-zh">异常理解</span></p>
      <h3>IAD-R1</h3>
      <p class="lang-en">A post-training framework for industrial anomaly reasoning with vision-language models.</p>
      <p class="lang-zh">面向工业异常理解，对视觉语言模型进行后训练，使模型能够判断异常、定位异常，并给出更贴近工程复核需求的解释。</p>
      <p class="work-links"><a href="https://github.com/Yanhui-Lee/IAD-R1" target="_blank" rel="noopener">Repository</a></p>
    </div>
  </article>

  <article class="work-card">
    <a href="https://github.com/caoyunkang/CPMF" target="_blank" rel="noopener">
      <img src="/images/works/cpmf.webp" alt="CPMF framework">
    </a>
    <div class="work-body">
      <p class="work-kicker"><i class="fas fa-cube" aria-hidden="true"></i><span class="lang-en">3D Anomaly Detection</span><span class="lang-zh">点云异常检测</span></p>
      <h3>CPMF</h3>
      <p class="lang-en">Complementary pseudo multimodal features for point cloud anomaly detection.</p>
      <p class="lang-zh">融合 3D 点云与多视角 2D 表征，提升点云异常检测中的细粒度定位和跨模态信息利用能力。</p>
      <p class="work-links"><a href="https://github.com/caoyunkang/CPMF" target="_blank" rel="noopener">Repository</a></p>
    </div>
  </article>
</div>

-----

<span class='anchor' id='projects'></span>

# <i class="fas fa-tasks section-icon" aria-hidden="true"></i><span class="lang-en">Selected Research Projects</span><span class="lang-zh">部分科研项目</span>

<ol>
  <li><span class="lang-en">National Natural Science Foundation of China, Major Program Topic, <strong>Cross-species Multi-sensory and Multi-granularity Bionic Perception</strong>, 62595801, 2026/01 - 2030/12, ongoing, participant.</span><span class="lang-zh">国家自然科学基金委员会重大项目课题，<strong>跨物种多感官多粒度仿生感知</strong>，62595801，2026/01 - 2030/12，在研，参与。</span></li>
  <li><span class="lang-en">Yuelushan Laboratory Seed Industry Special Project, <strong>Key Technologies and Applications for Crop Holographic Phenotype Acquisition and Analysis</strong>, YLS-20026-ZY01003, 2026/03 - 2028/03, ongoing, sub-project leader.</span><span class="lang-zh">岳麓山实验室种业专项，“人工智能+生物育种”技术攻关项目，<strong>作物全息表型采集与解析关键技术及应用</strong>，YLS-20026-ZY01003，2026/03 - 2028/03，在研，子课题负责人。</span></li>
  <li><span class="lang-en">Fuyao University of Science and Technology, School of Intelligent Manufacturing and Future Technology Open Fund, <strong>Semi-supervised Industrial Image Anomaly Detection via Defect Generation</strong>, FIMFYUST-2025B05, 2025/07 - 2027/07, ongoing, principal investigator.</span><span class="lang-zh">福耀科技大学智造与未来技术学院开放基金，<strong>基于缺陷生成的半监督工业图像异常检测算法研究</strong>，FIMFYUST-2025B05，2025/07 - 2027/07，在研，主持。</span></li>
  <li><span class="lang-en">Zhejiang University Hangzhou International Innovation Center entrusted project, <strong>AI Defect Sample Generation Algorithm Development</strong>, 2026/01 - 2026/12, ongoing, principal investigator.</span><span class="lang-zh">浙江大学杭州国际科创中心委托项目，<strong>AI 缺陷样本生成算法开发</strong>，2026/01 - 2026/12，在研，主持。</span></li>
  <li><span class="lang-en">Fundamental Research Funds for the Central Universities, <strong>Foundation-model-driven Anomaly Detection, Reasoning, and Recovery</strong>, 2025/10 - 2030/10, ongoing, principal investigator.</span><span class="lang-zh">中央高校基本科研基金项目，<strong>基于基础模型驱动的异常检测、推理与修复技术研究</strong>，2025/10 - 2030/10，在研，主持。</span></li>
</ol>

-----

<span class='anchor' id='teaching'></span>

# <i class="fas fa-chalkboard-teacher section-icon" aria-hidden="true"></i><span class="lang-en">Teaching</span><span class="lang-zh">开设课程</span>

## <i class="fas fa-user-graduate section-icon" aria-hidden="true"></i><span class="lang-en">Undergraduate Courses</span><span class="lang-zh">本科生课程</span>

- <span class="lang-en">Mathematical Foundations of Artificial Intelligence, 32 hours</span><span class="lang-zh">人工智能中的数学基础，32 学时</span>
- <span class="lang-en">Circuit Experiments, 32 hours</span><span class="lang-zh">电路实验，32 学时</span>
- <span class="lang-en">Electronic Technology Practice II, 32 hours</span><span class="lang-zh">电子技术实践 II，32 学时</span>

## <i class="fas fa-graduation-cap section-icon" aria-hidden="true"></i><span class="lang-en">Graduate Courses</span><span class="lang-zh">研究生课程</span>

- <span class="lang-en">Philosophy and Ethics in Artificial Intelligence, 32 hours</span><span class="lang-zh">人工智能中的哲学与伦理，32 学时</span>
- <span class="lang-en">Robotics for the Future, 32 hours</span><span class="lang-zh">面向未来的机器人，32 学时</span>

-----

<span class='anchor' id='news'></span>

# <i class="far fa-calendar-alt section-icon" aria-hidden="true"></i><span class="lang-en">News</span><span class="lang-zh">最新动态</span>

- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.06*: I was elected Deputy Director of the Department of Robotics Engineering, School of Artificial Intelligence and Robotics, Hunan University.</span><span class="lang-zh">*2026.06*: 当选湖南大学人工智能与机器人学院机器人工程系副主任。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.05*: Our paper *"Cross-source Medical Anomaly Detection via Prompt-guided Diffusion Representations"* has been accepted by **Pattern Recognition**.</span><span class="lang-zh">*2026.05*: 论文 *"Cross-source Medical Anomaly Detection via Prompt-guided Diffusion Representations"* 被 Pattern Recognition 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.04*: The *Pattern Recognition* Special Issue on *Foundation Models for Anomaly Detection, Reasoning, and Recovery* officially closed for submissions, receiving more than 230 manuscripts.</span><span class="lang-zh">*2026.04*: Pattern Recognition 特刊 *"Foundation Models for Anomaly Detection, Reasoning, and Recovery"* 正式截止投稿，累计收到 230 余篇稿件。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.03*: Our paper *"Visual Anomaly Detection under Complex View-Illumination Interplay: A Large-Scale Benchmark"* has been accepted by **Pattern Recognition**.</span><span class="lang-zh">*2026.03*: 论文 *"Visual Anomaly Detection under Complex View-Illumination Interplay: A Large-Scale Benchmark"* 被 Pattern Recognition 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.01*: Our survey paper *"A Comprehensive Survey for Real-World Industrial Defect Detection"* has been accepted by **Journal of Manufacturing Systems (JMS)**.</span><span class="lang-zh">*2026.01*: 综述论文 *"A Comprehensive Survey for Real-World Industrial Defect Detection"* 被 Journal of Manufacturing Systems 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.12*: Our paper on [Zero-shot 3D Anomaly Detection](https://arxiv.org/pdf/2409.13162) has been accepted by **IEEE TSMC**.</span><span class="lang-zh">*2025.12*: 零样本 3D 异常检测论文被 IEEE TSMC 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.11*: Three papers have been accepted by **AAAI 2026**, including two oral presentations.</span><span class="lang-zh">*2025.11*: 3 篇论文被 AAAI 2026 录用，其中 2 篇为 Oral。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.09*: I serve as the Executive Guest Editor for the *Pattern Recognition* Special Issue on *Foundation Models for Anomaly Detection, Reasoning, and Recovery*.</span><span class="lang-zh">*2025.09*: 担任 Pattern Recognition 特刊 *"Foundation Models for Anomaly Detection, Reasoning, and Recovery"* 执行客座编辑。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.05*: Our student paper received the Best Student Paper Award at **CSCWD 2025**.</span><span class="lang-zh">*2025.05*: 指导学生论文获 CSCWD 2025 Best Student Paper Award。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.04*: We organized the CVPR 2025 pre-conference "Industrial Vision" special session, attracting more than 5,000 online viewers.</span><span class="lang-zh">*2025.04*: 组织 CVPR 2025 预会议“工业视觉”专场，线上观看人数超过 5000。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.03*: Two papers on unified anomaly detection and unseen anomaly generation have been accepted by **CVPR 2025**.</span><span class="lang-zh">*2025.03*: 关于统一异常检测和未见异常生成的 2 篇论文被 CVPR 2025 录用。</span>

-----

<span class='anchor' id='publications'></span>

# <i class="fas fa-book-open section-icon" aria-hidden="true"></i><span class="lang-en">Representative Publications</span><span class="lang-zh">代表性论文</span>

Note: \* indicates equal contribution. † indicates corresponding author.
{: .lang-en}

说明：\* 表示共同第一作者，† 表示通讯作者。完整列表请见 [Google Scholar](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ&view_op=list_works&sortby=pubdate).
{: .lang-zh}

[![Citations](https://img.shields.io/badge/Citations-2100%2B-007ec6?logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ)
[![H-index](https://img.shields.io/badge/H--index-21-2563eb?logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?hl=zh-CN&user=aLJ8_G4AAAAJ)
[![GitHub](https://img.shields.io/badge/GitHub-caoyunkang-181717?logo=github&logoColor=white)](https://github.com/caoyunkang)

## <i class="fas fa-magic section-icon" aria-hidden="true"></i><span class="lang-en">Anomaly Generation</span><span class="lang-zh">异常生成</span>

<ol>
  <li>Sun H, Cao Y（曹云康）, Dong H, et al. Unseen Visual Anomaly Generation. <i>IEEE/CVF Conference on Computer Vision and Pattern Recognition</i>, 2025. doi:10.1109/CVPR52734.2025.02375. CCF-A.</li>
  <li>Jiang Y, Luo W, Zhang H, Shen W, Cao Y†（曹云康）. Anomagic: Crossmodal Prompt-driven Zero-shot Anomaly Generation. <i>AAAI Conference on Artificial Intelligence</i>, 2026. doi:10.48550/arXiv.2511.10020. CCF-A.</li>
  <li>Cheng Y, Cao Y（曹云康）, Wang D, et al. Boosting global-local feature matching via anomaly synthesis for multi-class point cloud anomaly detection. <i>IEEE Transactions on Automation Science and Engineering</i>, 22: 12560-12571, 2025. doi:10.1109/TASE.2025.3544462. 中科院二区.</li>
  <li>Cao Y（曹云康）, Yao H, Cai Y, Zhang Y, Chen H, Zhang H, Shen W. Cross-source medical anomaly detection via prompt-guided diffusion representations. <i>Pattern Recognition</i>, 2026, 180(Part A): 113985. doi:10.1016/j.patcog.2026.113985.</li>
</ol>

## <i class="fas fa-search section-icon" aria-hidden="true"></i><span class="lang-en">Anomaly Detection</span><span class="lang-zh">异常检测</span>

<ol>
  <li>Cao Y（曹云康）, Zhang J, Frittoli L, et al. AdaCLIP: Adapting CLIP with Hybrid Learnable Prompts for Zero-Shot Anomaly Detection. <i>European Conference on Computer Vision</i>, 2025. doi:10.1007/978-3-031-72761-0_4. CCF-B.</li>
  <li>Luo W*, Cao Y*（曹云康）, Yao H, et al. Exploring Intrinsic Normal Prototypes within a Single Image for Universal Anomaly Detection. <i>IEEE/CVF Conference on Computer Vision and Pattern Recognition</i>, 2025. doi:10.1109/CVPR52734.2025.00932. CCF-A.</li>
  <li>Cao Y（曹云康）, Xu X, Cheng Y, et al. Personalizing Vision-Language Models with Hybrid Prompts for Zero-Shot Anomaly Detection. <i>IEEE Transactions on Cybernetics</i>, 55(4): 1917-1929, 2025. 中科院一区.</li>
  <li>Cao Y（曹云康）, Xu X, Liu Z, et al. Collaborative discrepancy optimization for reliable image anomaly localization. <i>IEEE Transactions on Industrial Informatics</i>, 19(11): 10674-10683, 2023. 中科院一区.</li>
  <li>Cao Y（曹云康）, Yao H, Luo W, et al. VarAD: Lightweight High-Resolution Image Anomaly Detection via Visual Autoregressive Modeling. <i>IEEE Transactions on Industrial Informatics</i>, 21(4): 3246-3255, 2025. 中科院一区，高被引论文.</li>
  <li>Cao Y（曹云康）, Xu X, Shen W. Complementary pseudo multimodal feature for point cloud anomaly detection. <i>Pattern Recognition</i>, 156: 110761, 2024. doi:10.1016/j.patcog.2024.110761. 中科院一区.</li>
  <li>Cheng Y*, Cao Y*（曹云康）, Xie G, et al. Towards zero-shot point cloud anomaly detection: A multi-view projection framework. <i>IEEE Transactions on Systems, Man, and Cybernetics: Systems</i>, 53(3): 1747-1760, 2026. doi:10.1109/TSMC.2025.3648581. 中科院一区.</li>
  <li>Cao Y（曹云康）, Cheng Y, Zhang Y, et al. Visual anomaly detection under complex view-illumination interplay: A large-scale benchmark. <i>Pattern Recognition</i>, 2026.</li>
</ol>

## <i class="fas fa-brain section-icon" aria-hidden="true"></i><span class="lang-en">Anomaly Understanding</span><span class="lang-zh">异常理解</span>

<ol>
  <li>Li Y, Cao Y（曹云康）, Liu C, et al. IAD-R1: Reinforcing Consistent Reasoning in Industrial Anomaly Detection. <i>AAAI Conference on Artificial Intelligence</i>, 2026. doi:10.48550/arXiv.2508.09178. CCF-A, Oral.</li>
  <li>Xu X, Cao Y（曹云康）, Zhang H, Sang N, Huang X. Customizing Visual-Language Foundation Models for Multi-Modal Anomaly Detection and Reasoning. <i>International Conference on Computer Supported Cooperative Work in Design</i>, 2025. CCF-C, Best Student Paper Award.</li>
  <li>Zhang Y, Cao Y（曹云康）, Xu X, et al. LogiCode: An LLM-Driven Framework for Logical Anomaly Detection. <i>IEEE Transactions on Automation Science and Engineering</i>, 22: 7712-7723, 2025. 中科院二区.</li>
  <li>Cai W, Huang W, Cao Y（曹云康）, et al. Towards VLM-based Hybrid Explainable Prompt Enhancement for Zero-Shot Industrial Anomaly Detection. <i>International Joint Conference on Artificial Intelligence</i>, 2025. CCF-A.</li>
</ol>

## <i class="fas fa-robot section-icon" aria-hidden="true"></i><span class="lang-en">Embodied Perception</span><span class="lang-zh">具身感知</span>

<ol>
  <li>Liu J*, Cao Y*（曹云康）, Chen Y*, Li C, Du Y, Zhang H. Towards Active Real-to-Twin Inspection: A New Paradigm for Zero-Shot Anomaly Detection. <i>The 16th IEEE International Conference on CYBER Technology in Automation, Control, and Intelligent Systems</i>, 2026. arXiv:2605.25407.</li>
  <li>Du Y, Zhang H, Cheng Y, Huang C, Cao Y†（曹云康）. OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection. <i>2026 Joint International Conference on Automation-Intelligence-Safety and International Symposium on Autonomous Systems</i>, 2026: 1-6. doi:10.1109/ICAISISAS68969.2026.11567774. Best Student Paper.</li>
  <li>Cheng Y, Sun Y, Zhang H, Shen W, Cao Y†（曹云康）. Towards high-resolution 3D anomaly detection: A scalable dataset and real-time framework for subtle industrial defects. <i>AAAI Conference on Artificial Intelligence</i>, 2026. doi:10.48550/arXiv.2507.07435. CCF-A, Oral.</li>
  <li>Zhang H, Liu H, Biekezati B, Cao Y（曹云康）, et al. FPF: A Focused Perception Framework for Small Defect Identification in Complex Power Scenarios. <i>IEEE Transactions on Industrial Informatics</i>, doi:10.1109/TII.2025.3649024, 2026. 中科院一区.</li>
</ol>

-----

<span class='anchor' id='patents'></span>

# <i class="fas fa-certificate section-icon" aria-hidden="true"></i><span class="lang-en">Selected Authorized Patents</span><span class="lang-zh">代表性授权专利</span>

<ol>
  <li>张辉，杜瑞，别克扎提·巴合提，陈厚权，邱宇，张恺宁，曹云康，王耀南. 一种基于霍奇分解与多模态融合的部件分割方法及系统：中国，ZL202511195689.2，2025年10月31日，授权。</li>
  <li>张辉，唐友源，杜瑞，别克扎提·巴合提，陈厚权，张恺宁，曹云康，邱宇，王耀南. 一种基于结构感知框架的架空电力线覆冰厚度检测方法和系统：中国，ZL202511195907.2，2025年10月31日，授权。</li>
  <li>沈卫明，程育奇，曹云康，张以恒，孙依晗，谭宇翔，张雨昕. 一种复杂零件缺陷数据标注方法、缺陷检测方法及多视角多光照数据采集装置：中国，ZL202510060769.0，2025年12月2日，授权。</li>
  <li>沈卫明，程育奇，曹云康. 一种考虑原型分数校正的点云异常检测方法及设备：中国，ZL202510040267.1，2026年2月17日，授权。</li>
  <li>沈卫明，程育奇，曹云康. 一种点云数据局部异常生成方法及系统：中国，ZL202410633098.8，2025年2月11日，授权。</li>
  <li>沈卫明，程育奇，曹云康. 一种考虑多层级特征的多类别点云异常检测方法及系统：中国，ZL202410622146.3，2025年2月11日，授权。</li>
  <li>沈卫明，程育奇，曹云康. 一种考虑提示学习的零样本点云异常检测方法及系统：中国，ZL202410359413.2，2024年11月5日，授权。</li>
  <li>沈卫明，姜雨欣，曹云康. 基于原型学习引导的判别分割网络的小样本缺陷检测方法：中国，ZL202311254405.3，2025年11月4日，授权。</li>
  <li>沈卫明，刘照阁，徐晓豪，曹云康. 基于像素单点及多元配对的无监督异常检测方法：中国，ZL202310570510.1，2026年1月6日，授权。</li>
  <li>沈卫明，姜雨欣，曹云康. 一种工业缺陷检测方法及系统：中国，ZL202310570502.7，2025年11月21日，授权。</li>
</ol>

-----

<span class='anchor' id='awards'></span>

# <i class="fas fa-award section-icon" aria-hidden="true"></i><span class="lang-en">Awards</span><span class="lang-zh">科研获奖经历</span>

<ol>
  <li><span class="lang-en">Key Technologies and Applications of Multimodal Perception and Collaborative Optimization for Collaborative Intelligent Manufacturing, China Association of Inventions Invention Entrepreneurship Award, Project Award Second Prize, 3rd ranked, Dec. 2025.</span><span class="lang-zh">面向协同智能制造的多模态感知与协同优化关键技术及应用，中国发明协会发明创业奖项目奖二等奖，排名第三，2025年12月。</span></li>
  <li><span class="lang-en">Key Technologies and Applications of Multimodal Perception and Collaborative Optimization for Collaborative Intelligent Manufacturing, Gold Award of the 29th National Invention Exhibition, 3rd ranked, Oct. 2025.</span><span class="lang-zh">面向协同智能制造的多模态感知与协同优化关键技术及应用，第二十九届全国发明展览会金奖，排名第三，2025年10月。</span></li>
  <li><span class="lang-en">Yunkang Cao, Xiaohao Xu, Chen Sun, Yuqi Cheng, Liang Gao, Weiming Shen. Runner-up, CVPR Visual Anomaly and Novelty Detection Challenge, Jun. 2023.</span><span class="lang-zh">Yunkang Cao, Xiaohao Xu, Chen Sun, Yuqi Cheng, Liang Gao, Weiming Shen. CVPR Visual Anomaly and Novelty Detection Challenge，全球亚军，2023年6月。</span></li>
  <li><span class="lang-en">Xiaohao Xu, Yunkang Cao, Huaxin Zhang, Nong Sang, Xiaonan Huang. Best Student Paper Award, IEEE Computer Supported Cooperative Work in Design, May 2025.</span><span class="lang-zh">Xiaohao Xu, Yunkang Cao, Huaxin Zhang, Nong Sang, Xiaonan Huang. IEEE Computer Supported Cooperative Work in Design，Best Student Paper Award，2025年5月。</span></li>
  <li><span class="lang-en">Du Y, Zhang H, Cheng Y, Huang C, Cao Y. Best Student Paper Award, ICAIS & ISAS, 2026.</span><span class="lang-zh">Du Y, Zhang H, Cheng Y, Huang C, Cao Y. ICAIS & ISAS，Best Student Paper Award，2026年。</span></li>
  <li><span class="lang-en">Yunkang Cao, National Scholarship for Ph.D. Students, Nov. 2024.</span><span class="lang-zh">曹云康，博士研究生国家奖学金，2024年11月。</span></li>
</ol>

-----

<span class='anchor' id='service'></span>

# <i class="fas fa-hands-helping section-icon" aria-hidden="true"></i><span class="lang-en">Academic Service</span><span class="lang-zh">学术服务</span>

## <i class="fas fa-edit section-icon" aria-hidden="true"></i><span class="lang-en">Editorial and Reviewing Service</span><span class="lang-zh">编委与审稿服务</span>

- <span class="lang-en">Editorial Board Member, *Pattern Recognition*.</span><span class="lang-zh">*Pattern Recognition* 编委。</span>
- <span class="lang-en">Lead organizer of the Special Issue on "Foundation Models for Anomaly Detection, Reasoning, and Recovery."</span><span class="lang-zh">牵头组织“面向缺陷检测、推理与修复的基础模型”专题特刊。</span>
- <span class="lang-en">Special Session Chair, IEEE CSCWD 2025.</span><span class="lang-zh">IEEE CSCWD 2025 专题主席。</span>
- <span class="lang-en">Reviewer for TPAMI, IJCV, CVPR, ICCV, NeurIPS, AAAI, IJCAI, *Pattern Recognition*, IEEE TCYB, IEEE TII, and other journals and conferences.</span><span class="lang-zh">担任 TPAMI、IJCV、CVPR、ICCV、NeurIPS、AAAI、IJCAI、Pattern Recognition、IEEE TCYB、IEEE TII 等期刊与会议审稿人。</span>

## <i class="fas fa-users section-icon" aria-hidden="true"></i><span class="lang-en">Workshop and Forum Organization</span><span class="lang-zh">研讨会与论坛组织</span>

<ol>
  <li><span class="lang-en">CVPR 2024-2026, Visual Anomaly and Novelty Detection Workshop (VAND).</span><span class="lang-zh">CVPR 2024-2026，视觉异常与新颖性检测研讨会 VAND。</span></li>
  <li><span class="lang-en">IJCAI 2024, Anomaly Detection with Foundation Models Workshop (ADFM).</span><span class="lang-zh">IJCAI 2024，基于基础模型的异常检测研讨会 ADFM。</span></li>
  <li><span class="lang-en">ICCV 2025, Anomaly Detection with Foundation Models Workshop (ADFM).</span><span class="lang-zh">ICCV 2025，基于基础模型的异常检测研讨会 ADFM。</span></li>
  <li><span class="lang-en">CVPR 2026, Anomaly Detection with Foundation Models Workshop (ADFM).</span><span class="lang-zh">CVPR 2026，基于基础模型的异常检测研讨会 ADFM。</span></li>
  <li><span class="lang-en">IEEE CASE, Special Session on Industrial Foundation Models and Applications in Smart Manufacturing.</span><span class="lang-zh">IEEE CASE，“智能制造中的工业大模型及其应用”专题。</span></li>
  <li><span class="lang-en">CSIG Donghu Forum, CVPR 2025 pre-conference "Industrial Vision" special session.</span><span class="lang-zh">CSIG “东湖论坛”前沿论文分享会 CVPR 2025 预会议“工业视觉”专场。</span></li>
  <li><span class="lang-en">YAC 2026, Special Session on Industrial Vision Intelligent Measurement and Inspection, Special Session Chair, Changsha.</span><span class="lang-zh">YAC 2026，“工业视觉智能测量与检测”专题，专题主席，长沙。</span></li>
  <li><span class="lang-en">The 3rd International Conference on 3D Vision, Perception and Applications, Robot Intelligent Inspection Forum, Forum Secretary, Suzhou.</span><span class="lang-zh">第三届国际 3D 视觉感知与应用大会，“机器人智能检测”分会，论坛秘书，苏州。</span></li>
  <li><span class="lang-en">CSIG Frontier Forum on Embodied Intelligent Perception and Inspection, Organizing Committee Chair, Guilin.</span><span class="lang-zh">CSIG 具身智能感知与检测前沿论坛，组织委员会主席，桂林。</span></li>
</ol>

<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=300&t=tt&d=QltdrDBXR7cYztdXsLCBfSeruYl8EMVZ7i3zpSoGzP4&co=2d78ad&cmo=3acc3a&cmn=ff5353&ct=ffffff'></script>
