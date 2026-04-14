---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi👋, I am Tongcheng, currently a master’s student in the [NICS-EFC Lab](https://nicsefc.ee.tsinghua.edu.cn/) ([EffAlg](https://nics-effalg.com/)) at the Department of Electronic Engineering, Tsinghua University. I’m now advised by [Professor Wang Yu](https://nicsefc.ee.tsinghua.edu.cn/people/YuWang), [Professor Ding Wenbo](https://ssr-group.net/), and [Dr. Ning Xuefei](https://nics-effalg.com/ningxuefei/). I received my Bachelor’s degree from the Beijing Institute of Technology in 2024. My research focuses on efficient visual generation, and recently, I’ve also become interested in agent system. I warmly welcome opportunities for collaboration or discussion—feel free to reach me out!

---

<h2 id="experience">Experience</h2>

**Kling Team, Kuaishou Technology** — Algorithm Research Intern  
Feb 2026 – Present  
Mentor: [Xin Tao](https://www.xtao.website/)

**Infinigence AI** — Algorithm Research Intern  
Aug 2023 – Jul 2025  
Mentor: [Xuefei Ning](https://nics-effalg.com/ningxuefei/)

---

<h2 id="publications">Publications</h2>

\* indicates equal contribution

{% assign pubs = site.publications | sort: ‘date’ | reverse %}
{% for pub in pubs %}
**[{{ pub.venue }}] [{{ pub.title }}]({{ pub.paperurl }})**  
{{ pub.excerpt }}  
{{ pub.citation }}

{% endfor %}

Please review my [Google Scholar profile](https://scholar.google.com/citations?user=tA7BRgQAAAAJ&hl=en) to view more.

