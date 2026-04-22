---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi👋, I am Tongcheng, currently a master’s student in the [NICS-EFC Lab](https://nicsefc.ee.tsinghua.edu.cn/) ([EffAlg](https://nics-effalg.com/)) at the Department of Electronic Engineering, Tsinghua University. I’m now advised by [Professor Yu Wang](https://nicsefc.ee.tsinghua.edu.cn/people/YuWang), [Professor Wenbo Ding](https://ssr-group.net/), and [Dr. Xuefei Ning](https://nics-effalg.com/ningxuefei/). I received my Bachelor’s degree from the Beijing Institute of Technology in 2024. I warmly welcome opportunities for collaboration or discussion—feel free to reach me out!

**Research Interests:** My primary research interest lies in efficient visual generation, specifically post-training model compression for visual diffusion models. I leverage techniques such as quantization, sparse attention, and linear attention to develop hardware-aware paradigms that enhance deployment efficiency across cloud and edge platforms. Recently, I have focused on integrating efficient architectures into the pre-training stage to improve training efficiency. Additionally, I am interested in the foundational capabilities of Vision-Language Models (VLMs) and emerging inference paradigms like Test-Time Training (TTT).

<h2 id="internship" style="border-bottom: none;">Internship</h2>

**Kling Team, Kuaishou Technology** — Algorithm Research Intern  
Feb 2026 – Present  
Mentor: [Xin Tao](https://www.xtao.website/)

**Infinigence AI** — Algorithm Research Intern  
Aug 2023 – Jul 2025  
Mentor: [Xuefei Ning](https://nics-effalg.com/ningxuefei/)

<h2 id="awards" style="border-bottom: none;">Awards</h2>

- Comprehensive Excellence Scholarship of Tsinghua University, 2024–2025
- Beijing Outstanding Graduate, 2024
- National Scholarship, Ministry of Education of China, 2022–2023
- National Scholarship, Ministry of Education of China, 2021–2022
- National Scholarship, Ministry of Education of China, 2020–2021

<h2 id="publications" style="border-bottom: none;">Publications</h2>

\* indicates equal contribution

{% assign pubs = site.publications | sort: ‘date’ | reverse %}
{% for pub in pubs %}
**[{{ pub.venue }}] [{{ pub.title }}]({{ pub.paperurl }})**  
{{ pub.excerpt }}  
{{ pub.citation }}

{% endfor %}

Please review my [Google Scholar profile](https://scholar.google.com/citations?user=tA7BRgQAAAAJ&hl=en) to view more.

