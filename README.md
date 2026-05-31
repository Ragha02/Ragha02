<div align="center">

```
╔══════════════════════════════════════════════════════╗
║   building autonomous systems · one commit at a time  ║
╚══════════════════════════════════════════════════════╝
```

# Raghu Sree Nandan

**AI Engineer · Full-Stack Developer**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/anarajula-rsn)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/kl2200031212)
[![Mail](https://img.shields.io/badge/sreen02@outlook.com-0078d4?style=flat-square&logo=microsoftoutlook&logoColor=white)](mailto:sreen02@outlook.com)

</div>

---

```python
class RaghuSreeNandan:
    location   = "Hyderabad, IN 🇮🇳"
    focus      = ["Agentic AI", "Full-Stack Engineering", "Data Engineering"]
    currently  = "Building autonomous AI systems + learning cloud ops"
    ask_me     = "AI agents · RAG · system design · full-stack architecture"
    fun_fact   = "Hackathon winner who debugs with cold coffee ☕"
```

---

## ⚡ Stack

<table>
<tr>
<td valign="top" width="50%">

**Languages**
`Python` `Java` `TypeScript` `JavaScript` `C`

**Frontend**
`React` `Next.js` `Angular` `Vue` `Tailwind CSS`

**Backend**
`Node.js` `Express` `Django` `Flask` `Spring`

</td>
<td valign="top" width="50%">

**AI & Data**
`PyTorch` `scikit-learn` `Pandas`

**Databases**
`PostgreSQL` `MongoDB` `MySQL` `Firebase`

**Infra & Tools**
`AWS` `Docker` `Git`

</td>
</tr>
</table>

---

## 📊 GitHub Activity

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=ragha02&show_icons=true&hide_border=true&theme=default&hide_title=true&count_private=true" />
&nbsp;&nbsp;
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs?username=ragha02&layout=compact&hide_border=true&theme=default" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=ragha02&hide_border=true&date_format=M%20j%5B%2C%20Y%5D" height="140" />

</div>

---

## 🎯 Currently

```
📌  Deep-diving into agentic AI & autonomous system design
📌  Exploring data engineering pipelines & cloud ops on AWS
📌  Open to interesting problems — reach out
```

---

## 🏅 Highlights

```
◆  Hackathon winner
◆  AWS Certified
◆  Java Certified
```

---

<div align="center">

*If the problem is interesting, I'm probably already thinking about it.*

</div>

name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"   # runs daily at midnight UTC
  workflow_dispatch:        # allows manual trigger from Actions tab
  push:
    branches:
      - main

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10

    steps:
      - name: Generate contribution snake (light + dark)
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ragha02
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push output to the output branch
        uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
