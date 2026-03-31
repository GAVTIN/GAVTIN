## Hi there, I'm Gaurav Sinha 👋

<p align="left">
  <a href="https://x.com/TheDevWhoShips" target="_blank">
    <img src="https://img.shields.io/badge/@TheDevWhoShips-000000?style=flat&logo=x&logoColor=white" alt="X / Twitter" />
  </a>
  <a href="https://www.linkedin.com/in/gaurav-sinha-b9156941/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:gavtin2807@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-EA4335?style=flat&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <img src="https://komarev.com/ghpvc/?username=GAVTIN&color=16a34a&style=flat&label=Profile+views" alt="Profile views" />
</p>

> **Senior Frontend Engineer & Tech Lead** · 11+ years · BFSI/Fintech · React · Node.js · AI-augmented development  
> *Currently on a public journey from frontend specialist → fullstack AI-first engineer* → **[@TheDevWhoShips](https://x.com/TheDevWhoShips)**

---

- 🔭 &nbsp;Building **[FinSight](#-finsight--financial-health--alert-aggregator)** — a production-grade full-stack fintech dashboard
- 🌱 &nbsp;Completing the **Airtribe AI-First Backend Developer** course — documenting every session publicly
- 💼 &nbsp;Deep expertise in **React · TypeScript · Redux Toolkit** across BFSI/investment banking products
- 🤖 &nbsp;Integrating AI tooling into daily dev workflow — **GitHub Copilot · Cursor AI · OpenAI API · LLMs**
- ✍️ &nbsp;Running a 19-part Twitter series on frontend → fullstack engineering at **[@TheDevWhoShips](https://x.com/TheDevWhoShips)**
- 👯 &nbsp;Open to collaborating on **fintech products · developer tooling · AI-first web apps**
- 💬 &nbsp;Ask me about **React architecture · Redux Toolkit · micro-frontends · async JS · REST API design**
- 📫 &nbsp;Reach me at **gavtin2807@gmail.com** or DM on [X / Twitter](https://x.com/TheDevWhoShips)
- 📍 &nbsp;**Thane, Maharashtra** — open to Mumbai/Thane hybrid · pan-India remote · international remote
- ⚡ &nbsp;Fun fact: I explained `Promise.allSettled` vs `Promise.all` by building a live fintech app that fetches stock prices from 3 APIs simultaneously

---

## 🚀 Featured Projects

---

### 💹 FinSight — Financial Health & Alert Aggregator

> *A production-style full-stack BFSI dashboard — built as a capstone for the Airtribe AI-First Backend course*

[![Node.js](https://img.shields.io/badge/Node.js-20-339933?style=flat&logo=node.js&logoColor=white)](https://nodejs.org)
[![Express](https://img.shields.io/badge/Express-4-000000?style=flat&logo=express&logoColor=white)](https://expressjs.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev)
[![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=flat&logo=redux&logoColor=white)](https://redux-toolkit.js.org)
[![MongoDB](https://img.shields.io/badge/MongoDB_Atlas-47A248?style=flat&logo=mongodb&logoColor=white)](https://mongodb.com)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)

**What it does**
- 📊 Calculates a real-time **Financial Health Score (0–100)** across diversification, risk balance, and performance
- ⚡ Fetches live prices from **3 independent data sources in parallel** using `Promise.allSettled` — prices are returned even when individual sources fail
- 🔔 Runs a **cron-scheduled alert engine** every 15 minutes that dispatches email, SMS, and webhook notifications when thresholds are breached
- 🔐 Full **JWT auth** with access token + refresh token rotation and Axios interceptor-based silent refresh
- 🛡 **Role-based access** — admin dashboard shows all users, portfolios, health scores, and alert rules with RTK Query per-user caching (5-minute cache, manual refresh)

**Key engineering decisions worth reading**

| Decision | Why |
|---|---|
| `Promise.allSettled` for market data | Partial prices beat no prices — one source down shouldn't block the whole feed |
| `Promise.all` for notifications | All channels must succeed or we need to know which failed |
| Closure-based rate limiter | No external library — demonstrates the pattern directly in production middleware |
| RTK Query with `keepUnusedDataFor` | Admin revisiting a user gets instant cached response; no redundant API call |
| Layered architecture | Routes → Controllers → Services → Models — services have zero Express imports |

**🔗 [View Repository](https://github.com/GAVTIN/finsight)** &nbsp;·&nbsp; **🌐 [Live Demo](https://finsight.vercel.app)**

---

### 🏨 Smart Host Allocator — Room Occupancy Optimizer

> *A revenue-maximising hotel room allocation engine built in React + TypeScript*

[![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)](https://vitejs.dev)

**What it does**
- 🏷 Intelligently **allocates hotel rooms** to incoming guests to maximise occupancy and revenue
- 🧮 Implements a **greedy allocation algorithm** — matches guest requirements to available rooms by price, capacity, and room type
- 📱 Clean, component-driven UI with TypeScript for full type safety across the allocation logic
- 🔄 Reactive state updates — room availability and revenue figures update instantly as allocations are made

**🔗 [View Repository](https://github.com/GAVTIN/smart-host-allocator)**

---

### 📈 TradeSpex — Portfolio & Stock Management Dashboard

> *A role-based trading dashboard with portfolio views, per-stock modals, and admin/client separation*

[![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)](https://vitejs.dev)
[![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=flat&logo=redux&logoColor=white)](https://redux-toolkit.js.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)](https://typescriptlang.org)

**What it does**
- 🔐 **JWT-based authentication** with separate admin and client role dashboards
- 📊 **Portfolio data views** — holdings, allocation breakdown, P&L at a glance
- 🪟 **Per-stock modals** — detailed stock information, price history, and position management
- 🧩 Component-driven architecture with Redux Toolkit for predictable, cache-aware state management
- ⚡ Built on **Vite** for near-instant HMR and optimised production builds

**🔗 [View Repository](https://github.com/GAVTIN/tradespex)**

---

## 🛠 Full Tech Stack

**Frontend**

![React](https://img.shields.io/badge/React_18-61DAFB?style=flat&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-764ABC?style=flat&logo=redux&logoColor=white)
![RTK Query](https://img.shields.io/badge/RTK_Query-764ABC?style=flat&logo=redux&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router_v6-CA4245?style=flat&logo=reactrouter&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js_20-339933?style=flat&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express_4-000000?style=flat&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=flat&logo=mongoose&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![node-cron](https://img.shields.io/badge/node--cron-339933?style=flat&logo=node.js&logoColor=white)

**AI & Developer Tooling**

![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat&logo=openai&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/GitHub_Copilot-000000?style=flat&logo=github&logoColor=white)
![Cursor AI](https://img.shields.io/badge/Cursor_AI-000000?style=flat&logoColor=white)

**Testing & Quality**

![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat&logo=cypress&logoColor=white)
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=flat&logo=eslint&logoColor=white)

**DevOps & Deployment**

![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat&logo=railway&logoColor=white)
![MongoDB Atlas](https://img.shields.io/badge/MongoDB_Atlas-47A248?style=flat&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![PM2](https://img.shields.io/badge/PM2-2B037A?style=flat&logoColor=white)

---

## 📊 GitHub Stats

<p align="left">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=GAVTIN&show_icons=true&theme=default&hide_border=true&count_private=true&bg_color=ffffff&title_color=16a34a&icon_color=16a34a&text_color=374151" alt="Gaurav's GitHub stats" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=GAVTIN&layout=compact&hide_border=true&bg_color=ffffff&title_color=16a34a&text_color=374151&langs_count=8" alt="Top languages" />
</p>

---

## 🧠 Currently Learning

```
Airtribe AI-First Backend Developer Course (Cohort 19)
├── ✅ JavaScript fundamentals — execution context, closures, this, Event Loop
├── ✅ Node.js runtime — libuv, async I/O, non-blocking model
├── ✅ Express.js — REST APIs, middleware chain, layered architecture
├── ✅ Async JS — callbacks → Promises → async/await → Promise combinators
├── ✅ MongoDB + Mongoose — schemas, virtuals, Atlas deployment
├── 🔄 Authentication — JWT, bcrypt, refresh token rotation
├── ⏳ System Design — HLD vs LLD, DB scaling, sharding
└── ⏳ AI Integration — LLM APIs, prompt engineering, AI-first backends
```

---

## ✍️ Latest from @TheDevWhoShips

> *Documenting the frontend → fullstack journey publicly — one post at a time*

- 🧵 **19-part series:** My journey from Senior Frontend Engineer to AI-First Fullstack Developer
- 💡 Sharing real patterns from production BFSI systems — micro-frontends, RTK Query caching, JWT interceptors
- 🤖 Writing about AI-augmented development — how Copilot, Cursor, and LLMs change how senior engineers work
- 🏗 Building in public — architecture decisions, debugging sessions, and lessons from the Airtribe course

**Follow along → [x.com/TheDevWhoShips](https://x.com/TheDevWhoShips)**

---

## 🤝 Let's Connect

I'm actively looking for **Senior Frontend Engineer, Tech Lead, and Fullstack Engineer** roles — particularly in BFSI/fintech companies and product startups.

If you're building something interesting in fintech, developer tooling, or AI-first products — let's talk.

<p>
  <a href="https://x.com/TheDevWhoShips">
    <img src="https://img.shields.io/badge/Follow_on_X-000000?style=for-the-badge&logo=x&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://www.linkedin.com/in/gaurav-sinha-b9156941/">
    <img src="https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  &nbsp;
  <a href="mailto:gavtin2807@gmail.com">
    <img src="https://img.shields.io/badge/Send_an_Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <i>"Ship consistently. Learn publicly. Build things that matter."</i>
</p>
