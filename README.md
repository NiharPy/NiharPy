<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&duration=3200&pause=900&color=6EE7B7&center=true&vCenter=true&width=760&height=45&lines=Co-Founder+%26+Engineer+%40+NOKVO+AI;Voice+AI+agents+that+answer+in+under+a+second;104%2C000+lines+of+Python.+Shipped+solo." alt="Neelala Harish Nihar Kumar" />

### Neelala Harish Nihar Kumar

**Backend & AI systems engineer.** Hyderabad, India 🇮🇳

I build production AI infrastructure — real-time voice agents, multi-tenant LLM pooling, agentic pipelines that ship code and forms unattended. I write the backend, the migrations, the IaC and the tests.

<a href="https://www.linkedin.com/in/nihar-neelala/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:Niharkumar1407@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://github.com/NiharPy?tab=repositories"><img src="https://img.shields.io/badge/Projects-181717?style=for-the-badge&logo=github&logoColor=white" alt="Projects" /></a>
<img src="https://komarev.com/ghpvc/?username=NiharPy&style=for-the-badge&color=6EE7B7&label=PROFILE+VIEWS" alt="Profile views" />

</div>

---

## `whoami`

```python
class Nihar:
    role        = "Co-Founder & Engineer @ NOKVO AI LLP"
    education   = "B.Tech CSE, GITAM — Class of 2027"
    focus       = ["real-time voice AI", "agent architecture", "distributed backends"]
    stack       = ["Python", "FastAPI", "PostgreSQL", "Redis", "Azure", "LangGraph"]
    speaks      = ["English", "Telugu", "Hindi"]           # and so do my agents
    currently   = "shipping NOKVO to production"

    def philosophy(self):
        return "fail-open for background work, fail-closed for money"
```

---

## 🔊 Flagship — [NOKVO](https://github.com/NiharPy/NOKVO)

> **Multi-tenant voice AI calling platform.** Agents that answer inbound calls and run outbound campaigns in English, Hindi and Telugu. Built and shipped solo.

<div align="center">

| | | | |
|:---:|:---:|:---:|:---:|
| **< 1s** | **273** | **104K** | **1,466** |
| end-of-speech → first audio | REST + WebSocket endpoints | lines of Python | automated tests |
| **52** | **55** | **3** | **82** |
| PostgreSQL tables | Alembic migrations | languages, live | failure modes mapped |

</div>

**What's actually hard about it:**

- 🧠 **Shared LLM pool** — killed per-tenant Azure OpenAI provisioning; idle reserved capacity now **zero**, budgeted with atomic Lua decrements over 60s / 200K-token windows in Redis
- ⚡ **Cache-warm routing** — each call anchors to a home deployment via `blake2b` hashing, keeping Azure's prompt cache hot across turns and rerouting rate-limited models in milliseconds
- 📞 **Zero-touch telephony** — Indian DID lifecycle fully automated (compliance filing → approval polling → rental → rotation), with Redis single-flight locks so replicas never double-buy paid numbers
- 🔁 **8 idempotent background loops** — scheduler, number polling, HMAC-signed CRM webhooks, lead sync — coordinated across replicas with Redis + PostgreSQL advisory locks
- 💳 **Razorpay billing** — subscriptions, prepaid minute bundles, credits wallet, 4 metered per-call cost centres, fail-closed webhook signature verification
- 🚀 **Ship pipeline** — Azure Container Apps, Bicep IaC, Key Vault managed identity, GitHub Actions OIDC CI/CD

<sub>`Python` `FastAPI` `PostgreSQL` `Redis` `Azure OpenAI` `Bicep` `Docker` `Vue 3` `Plivo` `Sarvam AI` `Razorpay` `OpenTelemetry` `LangSmith`</sub>

---

## 🛠 Selected Work

<table>
<tr>
<td width="50%" valign="top">

### [Agentic Google Form Generator](https://github.com/NiharPy/Agentic-GoogleForm-Generator)
`Feb 2026`

Natural-language prompt → a finished Google Form, built end to end **unattended**.

- 6-node **LangGraph** workflow splitting planner and executor
- Executor polls plans from Postgres over a **database-driven A2A protocol**
- 10 FastAPI routes, 7 tables, spanning **Azure + GCP**
- Google **OAuth 2.0** — forms land in *your* Drive, not a service account's
- RAG memory scoped per conversation, not globally

<sub>`FastAPI` `LangGraph` `PostgreSQL` `Qdrant` `A2A` `Google Forms API`</sub>

</td>
<td width="50%" valign="top">

### [Hydie — Agentic Backend Builder](https://github.com/NiharPy/Hydie)
`Jan – Feb 2026`

Natural-language prompt → working back-end code, scaffold through applied schema changes.

- 20-node **LangGraph** workflow delegating codegen to GPT-4o
- **17,000** lines across 109 modules, 30 endpoints, 23 tables
- Live schema scanned + embedded into **Qdrant** so generation stays grounded
- Every write gated behind an **MCP** confirmation node
- Import from GitHub via OAuth, or scaffold from zero

<sub>`FastAPI` `LangGraph` `Azure AI Foundry` `Qdrant` `MCP` `Key Vault`</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Needles](https://github.com/NiharPy/needles-v1)
`Dec 2024 – Aug 2025` · [demo ↗](https://drive.google.com/file/d/1QwREHyGly7MY-paOWP8kWdpl_0AdAGl2/view?usp=sharing)

Tailoring marketplace — concept to prototype in 9 months, leading a 2-person team.

- 28 Express routes over 24 MongoDB models, **7,100** lines of JS
- **Search by photo or description** via vector embeddings — no catalogue browsing
- RBAC across customer / tailor / admin on one shared backend
- 2 clients on one API: React Native + Vue.js
- Analytics split into a standalone Flask service

<sub>`Node.js` `Express` `MongoDB` `Qdrant` `React Native` `Vue.js` `Flask`</sub>

</td>
<td width="50%" valign="top">

### Beyond the code

**🏆 Leadership**
- Team Lead — Final-Year Capstone, GITAM `2026 –`
- Finance Head — E-Sports Club, GITAM `2025 – 26`
- Team Lead — Smart India Hackathon `2025`

**📜 Credentials**
- Microsoft Certified: **Azure AI Fundamentals (AI-900)**
- IELTS Academic — **Overall 7.0**

**📈 Go-to-market**
- Pitched NOKVO to marketing heads at **15 real-estate companies** — validated demand, isolated price as the blocker

</td>
</tr>
</table>

---

## ⚙️ Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

**Backend & APIs**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socketdotio&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth_2.0-EB5424?style=flat-square&logo=auth0&logoColor=white)

**AI & Agents**

![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangSmith](https://img.shields.io/badge/LangSmith-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=anthropic&logoColor=white)

**Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Alembic](https://img.shields.io/badge/Alembic-6BA81E?style=flat-square&logo=alembic&logoColor=white)

**Cloud & DevOps**

![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Bicep](https://img.shields.io/badge/Bicep_IaC-0078D4?style=flat-square&logo=icinga&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

**Frontend**

![Vue](https://img.shields.io/badge/Vue_3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)

---

## 📊 Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=NiharPy&show_icons=true&hide_border=true&theme=tokyonight&bg_color=00000000&title_color=6EE7B7&icon_color=6EE7B7&include_all_commits=true&count_private=true" alt="GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=NiharPy&layout=compact&hide_border=true&theme=tokyonight&bg_color=00000000&title_color=6EE7B7&langs_count=8" alt="Top languages" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=NiharPy&theme=tokyo-night&hide_border=true&bg_color=00000000&color=6EE7B7&line=6EE7B7&point=ffffff&area=true" alt="Activity graph" width="98%" />

</div>

---

<div align="center">

### Building something that needs to talk, think, or scale?

**[📬 Niharkumar1407@gmail.com](mailto:Niharkumar1407@gmail.com)** &nbsp;·&nbsp; **[💼 LinkedIn](https://www.linkedin.com/in/nihar-neelala/)**

<sub><i>fail-open for background work, fail-closed for money.</i></sub>

</div>
