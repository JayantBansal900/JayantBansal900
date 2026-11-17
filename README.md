<!-- ============================== HEADER ============================== -->
<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:7aa2f7&height=220&section=header&text=Jayant%20Bansal&fontSize=62&fontColor=ffffff&fontAlignY=36&desc=Full-Stack%20Developer%20%E2%80%A2%20Backend%20%E2%80%A2%20AI%20Apps&descSize=20&descAlignY=58&animation=fadeIn" alt="Jayant Bansal"/>
</p>

<p align="center">
  <a href="https://github.com/JayantBansal900">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=800&color=7AA2F7&center=true&vCenter=true&width=620&lines=Building+scalable+backends+with+Spring+Boot;Microservices+%E2%80%A2+Kafka+%E2%80%A2+Redis+%E2%80%A2+Docker;Full-stack+apps+with+MERN+%2B+TypeScript;AI+apps+with+RAG%2C+FAISS+%26+Gemini;Always+shipping+something+new+%F0%9F%9A%80" alt="Typing intro"/>
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=JayantBansal900&label=Profile%20views&color=7aa2f7&style=flat-square" alt="Profile views"/>
  <a href="https://github.com/JayantBansal900?tab=followers"><img src="https://img.shields.io/github/followers/JayantBansal900?label=Followers&style=flat-square&color=bb9af7&logo=github" alt="Followers"/></a>
  <a href="https://github.com/JayantBansal900?tab=repositories"><img src="https://img.shields.io/badge/Projects-10%2B-9ece6a?style=flat-square&logo=github" alt="Projects"/></a>
  <img src="https://img.shields.io/badge/Open%20to-Opportunities-f7768e?style=flat-square" alt="Open to opportunities"/>
</p>

<!-- ============================== ABOUT ============================== -->
## 🧑‍💻 About me

<img align="right" width="360" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=JayantBansal900&theme=tokyonight" alt="Profile summary" />

I'm a **full-stack developer** who enjoys turning ideas into complete, deployed products, from the database and API all the way to the UI.

- ⚙️ **Backend first:** Java, Spring Boot, microservices, event-driven systems with Kafka
- 🌐 **Full-stack:** MERN, NestJS, React + TypeScript, Tailwind
- 🤖 **Applied AI:** RAG pipelines, semantic search (FAISS), LLM apps with Gemini, ML clustering
- 🔭 Currently building **[QuickKart](https://github.com/JayantBansal900/QuickKart)**, a Spring Boot microservice e-commerce platform
- 🎯 Looking for **SDE internships and full-time roles**
- 💬 Ask me about **Spring Boot, MERN, system design, or RAG**

<br clear="right"/>

```js
const jayant = {
  role: "Full-Stack Developer",
  backend: ["Java", "Spring Boot", "Node.js", "Express", "NestJS"],
  frontend: ["React", "TypeScript", "Tailwind CSS", "Vite"],
  data: ["PostgreSQL", "MongoDB", "Redis", "Kafka"],
  ai: ["RAG", "FAISS", "Gemini", "scikit-learn"],
  devops: ["Docker", "GitHub Actions", "Vercel", "Render"],
  currentFocus: "Distributed systems & production-grade backends",
};
```

<!-- ============================== TECH STACK ============================== -->
## 🧰 Tech stack

<p align="center"><b>Languages</b><br/><br/>
  <img src="https://skillicons.dev/icons?i=java,js,ts,py,html,css&theme=dark" alt="Languages"/>
</p>
<p align="center"><b>Backend & Frontend</b><br/><br/>
  <img src="https://skillicons.dev/icons?i=spring,nodejs,express,nestjs,fastapi,flask,react,tailwind,vite&theme=dark" alt="Frameworks"/>
</p>
<p align="center"><b>Databases, Messaging & DevOps</b><br/><br/>
  <img src="https://skillicons.dev/icons?i=postgres,mongodb,redis,kafka,docker,githubactions,vercel,maven&theme=dark" alt="Data and DevOps"/>
</p>
<p align="center"><b>AI / ML & Tools</b><br/><br/>
  <img src="https://skillicons.dev/icons?i=sklearn,opencv,git,github,vscode,idea,postman,linux&theme=dark" alt="AI and tools"/>
</p>

<!-- ============================== FEATURED ============================== -->
## 🚀 Featured projects

### 🛒 [QuickKart](https://github.com/JayantBansal900/QuickKart): microservice e-commerce platform

![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.5-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![React](https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

A React storefront and admin panel on top of Spring Boot services behind an API gateway, with PostgreSQL, Redis and Kafka.

```text
 Browser ─▶ nginx + React ─▶ API Gateway :8080  (routing · CORS · correlation id)
                                 │
          ┌──────────────────────┼───────────────────────┐
          ▼                      ▼                       ▼
   Product service         Order service            Monolith
   catalog · search        cart · checkout          auth · admin · email
   ⇅ Redis cache           outbox relay ──▶ Kafka ──▶ consumer ──▶ SMTP
          └──────────────── PostgreSQL ──────────────────┘
```

- 🔒 **No overselling:** checkout locks product rows (`SELECT … FOR UPDATE`) and checks stock in one transaction
- 🔁 **No double orders:** idempotency keys + cart fingerprints; a repeated checkout returns the same order
- 📬 **No lost events:** a **transactional outbox** writes the event with the order, and a relay publishes it to Kafka
- ♻️ **No duplicate emails:** idempotent consumer, retries and a dead-letter topic
- ⚡ **Fast catalog:** Redis-cached search at **687 req/s, p95 ≈ 50 ms** (load-tested)
- 🛡️ **Security:** JWT revoked on password reset, HMAC-hashed OTPs, per-email and per-IP rate limiting
- ✅ **CI:** GitHub Actions with Testcontainers and an embedded Kafka

<br/>

### 📊 [Segmentra](https://github.com/JayantBansal900/customer-segmentation): customer segmentation platform · [**Live demo**](https://segmentra.vercel.app)

<a href="https://segmentra.vercel.app"><img src="https://raw.githubusercontent.com/JayantBansal900/customer-segmentation/main/docs/screenshots/home.jpg" alt="Segmentra screenshot" width="100%"/></a>

Upload transaction data and get explorable customer segments: **RFM features + KMeans clustering**, silhouette and PCA model diagnostics, per-customer drill-down, and CSV exports, all in a responsive React UI.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

<br/>

### More things I've built

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>✈️ <a href="https://github.com/JayantBansal900/AI-trip-planner">PushpakUdaan</a></h4>
      AI trip planner that generates day-by-day itineraries, budget breakdowns and hotel picks with <b>Google Gemini</b>.<br/><br/>
      <img src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white"/>
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
      <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
    </td>
    <td width="50%" valign="top">
      <h4>🏛️ <a href="https://github.com/JayantBansal900/ai-scheme-advisor">AI Scheme Advisor</a></h4>
      Finds the right government schemes from plain-language questions using <b>ML + FAISS semantic search + RAG</b>.<br/><br/>
      <img src="https://img.shields.io/badge/RAG-FAISS-0467DF?style=flat-square"/>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
      <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🧺 <a href="https://github.com/JayantBansal900/mini-laundry-order-management-system">Laundry Order System</a> · <a href="https://mini-laundry-order-management-syste-seven.vercel.app">Live</a></h4>
      <img src="https://raw.githubusercontent.com/JayantBansal900/mini-laundry-order-management-system/main/screenshots/dashboard.png" width="100%" alt="Laundry dashboard"/><br/>
      MERN order management: create orders, track status, dashboard analytics.<br/><br/>
      <img src="https://img.shields.io/badge/MERN-47A248?style=flat-square&logo=mongodb&logoColor=white"/>
    </td>
    <td width="50%" valign="top">
      <h4>🤖 <a href="https://github.com/JayantBansal900/ai-agent-education-system">AI Agent Education System</a></h4>
      <img src="https://raw.githubusercontent.com/JayantBansal900/ai-agent-education-system/main/frontend/Demo.png" width="100%" alt="AI agent demo"/><br/>
      Multi-agent pipeline: a <b>generator</b> writes content, a <b>reviewer</b> scores it, and a refinement loop improves it.<br/><br/>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🏘️ <a href="https://github.com/JayantBansal900/LocalLink">LocalLink</a></h4>
      Connects citizens, local service providers and municipal officers, with civic-issue reporting, escalation and role-based dashboards.<br/><br/>
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"/>
      <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white"/>
    </td>
    <td width="50%" valign="top">
      <h4>💳 <a href="https://github.com/JayantBansal900/saas-frontend">SaaS Subscription App</a> · <a href="https://saas-frontend-orcin.vercel.app">Live</a></h4>
      Subscription SaaS with JWT auth, plans, admin dashboard and Stripe (NestJS backend + React 19 frontend).<br/><br/>
      <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"/>
      <img src="https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB"/>
    </td>
  </tr>
</table>

<details>
<summary><b>📂 Even more projects</b></summary>
<br/>

| Project | Description | Stack |
|---|---|---|
| [ecommerce-mern](https://github.com/JayantBansal900/ecommerce-mern) | E-commerce with JWT auth, Razorpay payments and role-based access | MERN |
| [url-shortener-api](https://github.com/JayantBansal900/url-shortener-api) | URL shortener REST API | Node.js · Express · MongoDB |
| [luffy-stretch](https://github.com/JayantBansal900/luffy-stretch) | Real-time face-stretch effect controlled by hand pinch gestures | Python · MediaPipe · OpenCV |
| [review-analytics-dashboard](https://github.com/JayantBansal900/review-analytics-dashboard) | Sentiment dashboard for e-commerce reviews | HTML · CSS · JS |
| [Recipe-App](https://github.com/JayantBansal900/Recipe-App) · [Live](https://jayantbansal900.github.io/Recipe-App/) | Search and filter recipes with TheMealDB API | JavaScript |

</details>

<!-- ============================== STATS ============================== -->
## 📈 GitHub analytics

<p align="center">
  <img height="170" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=JayantBansal900&theme=tokyonight" alt="Stats"/>
  <img height="170" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=JayantBansal900&theme=tokyonight" alt="Top languages"/>
</p>
<p align="center">
  <img height="170" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=JayantBansal900&theme=tokyonight" alt="Repos per language"/>
  <img height="170" src="https://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=JayantBansal900&theme=tokyonight&utcOffset=5.5" alt="Productive time"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=JayantBansal900&theme=tokyonight&hide_border=true&border_radius=10" alt="Streak"/>
</p>
<p align="center">
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=JayantBansal900&theme=tokyo-night&hide_border=true&area=true" alt="Contribution graph"/>
</p>

<!-- ============================== SNAKE ============================== -->
## 🐍 Contribution snake

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/JayantBansal900/JayantBansal900/output/github-contribution-grid-snake-dark.svg"/>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/JayantBansal900/JayantBansal900/output/github-contribution-grid-snake.svg"/>
    <img alt="Contribution snake" src="https://raw.githubusercontent.com/JayantBansal900/JayantBansal900/output/github-contribution-grid-snake-dark.svg"/>
  </picture>
</p>

<!-- ============================== CONNECT ============================== -->
## 🤝 Let's connect

<p align="center">
  <a href="https://github.com/JayantBansal900"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></a>
  <!-- Add your links here, e.g.:
  <a href="https://www.linkedin.com/in/YOUR-ID"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  -->
</p>

<p align="center"><i>⭐ If you like a project, a star means a lot. Thanks for visiting!</i></p>

<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7aa2f7,50:203a43,100:0f2027&height=120&section=footer" alt="footer"/>
</p>
