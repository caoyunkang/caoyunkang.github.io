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
  <p class="role-line cn lang-zh"><i class="fas fa-user-graduate" aria-hidden="true"></i> 助理教授 · 副研究员 · 博士生导师 · 机器人工程系副主任</p>
  <div class="profile-meta">
    <span class="lang-en"><i class="fas fa-university" aria-hidden="true"></i> School of Artificial Intelligence and Robotics, Hunan University</span>
    <span class="lang-zh"><i class="fas fa-university" aria-hidden="true"></i> 湖南大学人工智能与机器人学院</span>
    <span><i class="fas fa-envelope" aria-hidden="true"></i> <a href="mailto:caoyunkang0207@gmail.com">caoyunkang0207@gmail.com</a></span>
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
  <a href="#about"><i class="fas fa-id-card" aria-hidden="true"></i><span class="lang-en">About</span><span class="lang-zh">个人简介</span></a>
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
    "#about-me": { zh: "首页", en: "Home" },
    "#openings": { zh: "招生", en: "Openings" },
    "#research": { zh: "研究方向", en: "Research" },
    "#works": { zh: "代表成果", en: "Works" },
    "#publications": { zh: "代表论文", en: "Publications" },
    "#service": { zh: "学术服务", en: "Service" },
    "/files/CV_Yunkang_CAO.pdf": { zh: "简历", en: "CV" }
  };

  function getMainNavLabels(link) {
    var href = link.getAttribute("href");
    if (mainNavLabels[href]) {
      return mainNavLabels[href];
    }

    try {
      var url = new URL(href, window.location.href);
      if (url.pathname === "/files/CV_Yunkang_CAO.pdf") {
        return mainNavLabels["/files/CV_Yunkang_CAO.pdf"];
      }
      if (url.origin === window.location.origin && url.hash && (url.pathname === "/" || url.pathname === window.location.pathname)) {
        return mainNavLabels[url.hash];
      }
    } catch (error) {
      return null;
    }

    return null;
  }

  function updateMainNav(lang) {
    document.querySelectorAll(".masthead a[href], .greedy-nav a[href]").forEach(function (link) {
      var labels = getMainNavLabels(link);
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

    document.querySelectorAll(".masthead a[href^='#'], .quick-nav a[href^='#']").forEach(function (link) {
      link.addEventListener("click", function (event) {
        var hash = link.getAttribute("href");
        var target = hash ? document.querySelector(hash) : null;
        if (!target) {
          return;
        }

        event.preventDefault();
        target.scrollIntoView({ block: "start" });
        if (window.history && window.history.replaceState) {
          window.history.replaceState({}, "", window.location.pathname + window.location.search + hash);
        } else {
          window.location.hash = hash;
        }
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

# <i class="fas fa-id-card section-icon" aria-hidden="true"></i><span class="lang-en">About</span><span class="lang-zh">个人简介</span>

I am an Assistant Professor and Ph.D. supervisor at the [School of Artificial Intelligence and Robotics, Hunan University (HNU)](http://robotics.hnu.edu.cn/), an Associate Research Fellow at the National Engineering Research Center of Robot Visual Perception and Control Technology, and Deputy Director of the Department of Robotics Engineering. I am a core member of the research team led by [Yaonan Wang (王耀南院士)](https://robotics.hnu.edu.cn/info/1176/3098.htm) and [Hui Zhang (张辉院长)](https://robotics.hnu.edu.cn/info/1176/2966.htm).
{: .lang-en}

曹云康，湖南大学人工智能与机器人学院助理教授、博士生导师，机器人视觉感知与控制技术国家工程研究中心副研究员，机器人工程系副主任，王耀南院士、张辉院长团队核心成员。
{: .lang-zh}

I received my Ph.D. in Mechanical Engineering from [Huazhong University of Science and Technology](http://english.hust.edu.cn/), where I was advised by [Prof. Weiming Shen](https://scholar.google.com.hk/citations?user=FuSHsx4AAAAJ&hl=en&oi=sra). From 2023 to 2024, I was a visiting Ph.D. researcher at [Politecnico di Milano](https://www.polimi.it/) under the supervision of [Prof. Giacomo Boracchi](https://boracchi.faculty.polimi.it/).
{: .lang-en}

2025 年获华中科技大学机械工程博士学位，师从[沈卫明教授](https://scholar.google.com.hk/citations?user=FuSHsx4AAAAJ&hl=en&oi=sra)。博士期间于 2023 至 2024 年赴[米兰理工大学](https://www.polimi.it/)访学，合作导师为 [Giacomo Boracchi 教授](https://boracchi.faculty.polimi.it/)。
{: .lang-zh}

My research centers on industrial inspection and covers four connected directions: anomaly generation, anomaly detection, anomaly understanding, and embodied perception. I study how inspection systems can learn from limited defect data, detect and explain anomalies in open environments, and guide robots to gather evidence through active observation. The goal is to develop practical methods that connect perception, reasoning, and action in industrial settings.
{: .lang-en}

主要研究工业场景中的异常生成、异常检测、异常理解和具身感知。针对缺陷数据少、生产环境变化大等问题，研究可控缺陷生成、开放场景异常检测和多模态异常推理，并将相关方法用于机器人主动巡检。代表性工作包括 Anomagic、INP-Former、IAD-R1 等。
{: .lang-zh}

<div class="metrics-grid">
  <div class="metric-item"><i class="fas fa-file-alt" aria-hidden="true"></i><strong>60+</strong><span class="lang-en">Publications</span><span class="lang-zh">论文</span></div>
  <div class="metric-item"><i class="fas fa-quote-right" aria-hidden="true"></i><strong>2100+</strong><span class="lang-en">Citations</span><span class="lang-zh">引用</span></div>
  <div class="metric-item"><i class="fas fa-chart-line" aria-hidden="true"></i><strong>21</strong><span class="lang-en">H-index</span><span class="lang-zh">H 指数</span></div>
  <div class="metric-item"><i class="fas fa-user-edit" aria-hidden="true"></i><strong>17</strong><span class="lang-en">First or Corresponding</span><span class="lang-zh">一作或通讯</span></div>
</div>


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

# <i class="fas fa-user-plus section-icon" aria-hidden="true"></i><span class="lang-en">Openings and Mentoring</span><span class="lang-zh">招生与培养</span>

<div class="opening-highlight">
<p class="lang-en"><i class="fas fa-bullhorn" aria-hidden="true"></i>The 2027 Ph.D. quota is full. I am currently recruiting master's students and research assistants. Applicants from artificial intelligence, automation, computer science, mechanical engineering, and related fields are welcome. Master's students may join through recommendation-based admission, the national entrance examination, or transfer admission.</p>
<p class="lang-zh"><i class="fas fa-bullhorn" aria-hidden="true"></i>2027 年博士研究生招生名额已满。目前主要招收硕士研究生和科研助理，欢迎人工智能、自动化、计算机、机械等相关专业的同学联系。硕士招生包括推免、统考和调剂。</p>
</div>

I work directly with students on topic selection, research design, and paper writing. New members begin with a concrete research problem and learn how to complete a full project, including literature review, experiment design, implementation, and manuscript preparation. Undergraduate students are encouraged to start research early. Research assistant positions may be remote or on site, and a commitment of about one year is recommended for those seeking sustained research experience or preparing for further study.
{: .lang-en}

我会直接参与选题、研究设计和论文指导。新同学入组后，通常先从一个具体课题做起，学习查阅文献、设计实验、实现算法和撰写论文。课题安排会结合个人基础和后续规划。本科生可提前进组；科研助理可线上或线下参与，建议连续投入一年左右，完成一个完整的研究项目。
{: .lang-zh}

I advised Yuhuan Du, an undergraduate from the 2023 cohort, on *OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection*. He is the first author, and I am the corresponding author. The paper received the Best Student Paper Award at ICAIS & ISAS 2026. Another student paper received the Best Student Paper Award at IEEE CSCWD 2025.
{: .lang-en}

2023 级本科生杜禹寰以第一作者完成论文 *OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection*，获 ICAIS & ISAS 2026 Best Student Paper Award，本人为通讯作者。另有一篇学生论文获 IEEE CSCWD 2025 Best Student Paper Award。
{: .lang-zh}

The group collaborates with the University of Oxford, Politecnico di Milano, Tsinghua University, Huazhong University of Science and Technology, Huawei, Tencent Youtu Lab, CATL, and SEER Robotics. Students have access to computing resources, robotic platforms, research projects, paper-writing support, and academic or industrial collaboration opportunities.
{: .lang-en}

课题组与牛津大学、米兰理工大学、清华大学、华中科技大学等高校保持合作，也与华为、腾讯优图、宁德时代、视比特机器人等企业开展联合研究。学生可使用团队的计算资源和机器人实验平台，并参与学术交流和企业合作项目。
{: .lang-zh}

**Contact**: Please send your CV to [caoyunkang0207@gmail.com](mailto:caoyunkang0207@gmail.com). Use the subject line "Master's Application / Research Assistant Application - Name - University - Major - Expected Start Date."
{: .lang-en}

申请时请将个人简历发送至 [caoyunkang0207@gmail.com](mailto:caoyunkang0207@gmail.com)，邮件标题请注明“硕士申请 / 科研助理申请 - 姓名 - 学校 - 专业 - 预计参与时间”。
{: .lang-zh}

-----

<span class='anchor' id='research'></span>

# <i class="fas fa-microscope section-icon" aria-hidden="true"></i><span class="lang-en">Research Directions</span><span class="lang-zh">研究方向</span>

The group studies four connected problems in industrial inspection: anomaly generation, anomaly detection, anomaly understanding, and embodied perception. Our work examines how inspection systems can learn from limited defect data, operate in open industrial environments, explain their findings, and guide robots to collect additional evidence and respond to anomalies.
{: .lang-en}

我的研究主要包括以下四个方向，均面向工业检测，具体关注缺陷样本不足、未知异常识别、异常原因分析和机器人自主巡检等问题。
{: .lang-zh}

## <i class="fas fa-magic section-icon" aria-hidden="true"></i><span class="lang-en">1. Anomaly Generation</span><span class="lang-zh">1. 异常生成</span>

We study physics-informed generation of realistic industrial defects. Our work combines generative models with physical priors and explores foundation-model agents that can plan the generation process, assess sample quality, and refine results iteratively. The generated data support detector training, benchmarking, and long-tail anomaly analysis when real defects are scarce.
{: .lang-en}

真实缺陷通常数量少、类型有限，采集和标注成本也较高。本方向研究引入物理先验的缺陷生成方法，使合成样本在外观和成因上更接近真实缺陷；同时探索大模型智能体在生成方案设计、样本筛选和自动迭代中的应用。生成数据主要用于检测模型训练、评测集构建和长尾异常分析。
{: .lang-zh}

## <i class="fas fa-search section-icon" aria-hidden="true"></i><span class="lang-en">2. Anomaly Detection</span><span class="lang-zh">2. 异常检测</span>

We develop unsupervised, few-shot, zero-shot, and unified anomaly detection methods for industrial images, point clouds, 3D geometry, and multi-view data. The research covers foundation models, vision-language models, normal prototype modeling, fine-grained localization, and generalization across products, defect types, and production sites.
{: .lang-en}

研究无监督、少样本、零样本和统一异常检测，数据形式包括 2D 图像、点云、3D 几何和多视角图像。重点关注正常原型建模、视觉语言模型、细粒度定位和跨产品泛化，希望模型在更换产线、产品或缺陷类型后仍能稳定使用。代表性成果包括首届 CVPR VAND 挑战赛全球亚军方法 Segment Any Anomaly，以及被多支获奖队伍采用的 INP-Former。
{: .lang-zh}

## <i class="fas fa-brain section-icon" aria-hidden="true"></i><span class="lang-en">3. Anomaly Understanding</span><span class="lang-zh">3. 异常理解</span>

We study multimodal anomaly understanding with foundation models. The research covers anomaly description, attribute recognition, cause analysis, visual question answering, risk assessment, and recovery suggestions. Representative work includes IAD-R1, which applies reinforcement learning to industrial anomaly reasoning.
{: .lang-en}

传统异常检测通常只给出分数和热力图，难以直接回答异常是什么、为什么出现以及如何处理。本方向研究基于多模态大模型的异常描述、属性识别、原因分析、视觉问答、风险评估和恢复建议。代表性成果 IAD-R1 将强化学习用于工业异常推理。
{: .lang-zh}

## <i class="fas fa-robot section-icon" aria-hidden="true"></i><span class="lang-en">4. Embodied Perception</span><span class="lang-zh">4. 具身感知</span>

We integrate anomaly detection and understanding into robots and unmanned inspection systems. Robots actively select viewpoints, plan observation paths, gather multimodal evidence, and revisit suspicious regions. This allows them to discover, verify, and understand anomalies in open industrial environments and provide evidence for subsequent decisions and recovery actions.
{: .lang-en}

具身感知面向机器人巡检。我们将异常检测和异常理解模型部署到机器人上，让机器人根据当前观测主动调整视角和路线，必要时返回疑似区域复查。这样，机器人可以在开放工业环境中完成异常发现、确认和解释，并将结果用于后续处置。
{: .lang-zh}

-----

<span class='anchor' id='works'></span>

# <i class="fas fa-layer-group section-icon" aria-hidden="true"></i><span class="lang-en">Representative Works</span><span class="lang-zh">代表性成果</span>

The following works illustrate the current research line from anomaly generation and detection to understanding and embodied inspection.
{: .lang-en}

以下列出几项与研究方向对应的代表性工作。
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
      <p class="lang-zh">利用视觉和文本提示控制缺陷的位置与形态，在没有真实异常样本的情况下生成训练数据。</p>
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
      <p class="lang-zh">面向 3D 工业检测，将缺陷合成、模型训练和在线推理组织为一套完整流程。</p>
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
      <p class="lang-zh">从单张图像中提取正常原型，用于跨类别的通用异常检测。该方法被 CVPR VAND 多支获奖队伍采用。</p>
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
      <p class="lang-zh">针对视角和光照变化，构建多视角、多光照工业异常检测数据集，用于评估模型在复杂成像条件下的稳定性。</p>
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
      <p class="lang-zh">通过后训练提升视觉语言模型的异常推理能力，使其能够判断和定位异常，并说明判断原因。</p>
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
      <p class="lang-zh">结合 3D 点云和多视角 2D 特征，改进点云异常检测与细粒度定位。</p>
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

- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.07*: Congratulations to Wenzhuo Sun. His project, *"Zero-shot Industrial Anomaly Detection Based on Active Embodied Vision and a Digital Twin,"* supervised by me, has been approved under the National Undergraduate Innovation Training Program in a key support area.</span><span class="lang-zh">*2026.07*: 恭喜孙文卓同学！由其负责、本人指导的项目《基于主动具身视觉与数字孪生的零样本工业异常检测关键技术研究》获国家级大学生创新训练计划重点支持领域项目立项。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.06*: I was elected Deputy Director of the Department of Robotics Engineering, School of Artificial Intelligence and Robotics, Hunan University.</span><span class="lang-zh">*2026.06*: 当选湖南大学人工智能与机器人学院机器人工程系副主任。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.05*: Congratulations to Yuhuan Du. His first-author paper, *"OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection,"* received the Best Student Paper Award at ICAIS & ISAS 2026. I am the corresponding author.</span><span class="lang-zh">*2026.05*: 恭喜杜禹寰！由其担任第一作者的论文《OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection》获 ICAIS & ISAS 2026 Best Student Paper Award，本人为通讯作者。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.05*: Our paper *"Cross-source Medical Anomaly Detection via Prompt-guided Diffusion Representations"* has been accepted by **Pattern Recognition**.</span><span class="lang-zh">*2026.05*: 论文 *"Cross-source Medical Anomaly Detection via Prompt-guided Diffusion Representations"* 被 Pattern Recognition 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.04*: The *Pattern Recognition* Special Issue on *Foundation Models for Anomaly Detection, Reasoning, and Recovery* officially closed for submissions, receiving more than 230 manuscripts.</span><span class="lang-zh">*2026.04*: Pattern Recognition 特刊 *"Foundation Models for Anomaly Detection, Reasoning, and Recovery"* 正式截止投稿，累计收到 230 余篇稿件。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.03*: Our paper *"Visual Anomaly Detection under Complex View-Illumination Interplay: A Large-Scale Benchmark"* has been accepted by **Pattern Recognition**.</span><span class="lang-zh">*2026.03*: 论文 *"Visual Anomaly Detection under Complex View-Illumination Interplay: A Large-Scale Benchmark"* 被 Pattern Recognition 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2026.01*: Our survey paper *"A Comprehensive Survey for Real-World Industrial Defect Detection"* has been accepted by **Journal of Manufacturing Systems (JMS)**.</span><span class="lang-zh">*2026.01*: 综述论文 *"A Comprehensive Survey for Real-World Industrial Defect Detection"* 被 Journal of Manufacturing Systems 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.12*: Our paper on [Zero-shot 3D Anomaly Detection](https://arxiv.org/pdf/2409.13162) has been accepted by **IEEE TSMC**.</span><span class="lang-zh">*2025.12*: 零样本 3D 异常检测论文被 IEEE TSMC 录用。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.11*: Three papers on high-resolution point cloud anomaly detection, zero-shot anomaly generation, and foundation models for anomaly detection have been accepted by **AAAI 2026**, including two oral presentations.</span><span class="lang-zh">*2025.11*: 课题组 3 篇论文获 AAAI 2026 录用，分别围绕高分辨率点云异常检测、零样本异常生成和异常检测基础模型展开，其中 2 篇入选 Oral。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.09*: I serve as the Executive Guest Editor for the *Pattern Recognition* Special Issue on *Foundation Models for Anomaly Detection, Reasoning, and Recovery*.</span><span class="lang-zh">*2025.09*: 担任 Pattern Recognition 特刊 *"Foundation Models for Anomaly Detection, Reasoning, and Recovery"* 执行客座编辑。</span>
- <i class="far fa-calendar-alt news-icon" aria-hidden="true"></i><span class="lang-en">*2025.05*: Congratulations to Xiaohao Xu. The paper *"Customizing Visual-Language Foundation Models for Multi-Modal Anomaly Detection and Reasoning,"* co-first-authored by Xiaohao Xu and me, received the Best Student Paper Award at **IEEE CSCWD 2025**.</span><span class="lang-zh">*2025.05*: 恭喜徐晓豪！我与徐晓豪共同作为第一作者完成的论文《Customizing Visual-Language Foundation Models for Multi-Modal Anomaly Detection and Reasoning》获 IEEE CSCWD 2025 Best Student Paper Award。</span>
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
  <li><span class="lang-en">Yuhuan Du et al. <i>OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection</i>, Best Student Paper Award, ICAIS & ISAS, 2026. Yuhuan Du is the student first author; Yunkang Cao is the corresponding author.</span><span class="lang-zh">杜禹寰等，<i>OmniPose-AD: Canonical Normal Rendering for Unaligned 3D Anomaly Detection</i>，ICAIS & ISAS 2026 Best Student Paper Award。杜禹寰为学生第一作者，曹云康为通讯作者。</span></li>
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
