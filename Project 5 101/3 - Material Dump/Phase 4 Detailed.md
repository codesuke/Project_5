# Phase 4 – MVP Plan

## **1. MVP Scope (Locked from Phase 2)**

We only build what’s essential for the demo:

- ✅ **English text search** (job title/description → NCO code)
- ✅ **Semantic search via embeddings**
- ✅ **Synonym handling**
- ✅ **Ranked results + confidence scores**
- ✅ **Typos & fuzzy matching**
- ✅ **Data ingestion pipeline**
- ✅ **Hierarchical NCO display**
- ✅ **Basic, clean UI**    

Everything else (voice, multilingual, dashboards, advanced filters) is **post-MVP/wow-phase**.

---

## **2. Development Timeline (2-Month Hackathon)**

| Week       | Goal                        | Tasks                                                                                                         | Owner(s)                   |
| ---------- | --------------------------- | ------------------------------------------------------------------------------------------------------------- | -------------------------- |
| **Week 1** | **Kickoff + Setup**         | Repo creation, branching rules, Docker dev env, assign roles, import NCO dataset sample                       | All                        |
| **Week 2** | **Data Ingestion Pipeline** | Parse dataset, clean, normalize, store in SQLite, generate embeddings (Sentence Transformers), index in FAISS | Data Eng + ML Eng          |
| **Week 3** | **Backend Search API**      | Build FastAPI endpoints: `/search` (semantic), `/ingest` (admin)                                              | Backend Lead               |
| **Week 4** | **Frontend Search UI**      | React + Tailwind search bar, result cards, loading states                                                     | Frontend Lead + Beginner 1 |
| **Week 5** | **Synonym + Fuzzy Match**   | Integrate synonyms dict & fuzzy search fallback                                                               | ML Eng + Backend Lead      |
| **Week 6** | **End-to-End Integration**  | Frontend → Backend → FAISS → SQLite → Frontend results                                                        | All                        |
| **Week 7** | **Testing & Bug Fixes**     | Unit tests, functional tests, fix UI bugs, performance tuning                                                 | QA + All                   |
| **Week 8** | **Demo-Readiness**          | Seed with test queries, add styling polish, prepare demo script                                               | Frontend Lead + PMs        |

---

## **3. Parallel Work Streams**

To avoid idle time:

- **Stream 1:** Data pipeline (Data Eng + ML Eng) → starts immediately with dataset extraction.
- **Stream 2:** Frontend scaffolding (Frontend Lead + Beginner Devs) → can work with mock API while backend is in progress.    
- **Stream 3:** Backend API (Backend Lead) → can test with fake embeddings until real pipeline ready.


---

## **4. Demo-Readiness Checkpoints**

We do **three hard checkpoints** to make sure we’re not blindsided:

1. **Checkpoint Alpha (Week 4)** – Frontend + mock backend connected.    
2. **Checkpoint Beta (Week 6)** – Full end-to-end working with real data.
3. **Checkpoint Gamma (Week 8)** – Fully tested, styled, and demo script rehearsed.    

---

## **5. Repo Management & Conflict Avoidance**

- Use **GitHub Projects** for Kanban board: Backlog → In Progress → Done.
- Assign tasks clearly so no one touches the same file without coordination.
- PR review mandatory before merge to `dev`.
- Freeze `dev` one week before demo — only bug fixes allowed.    

---

## **6. Testing Workflow**

- **Daily Smoke Test:** Run standard set of queries every morning.
- **Unit Tests:** For search logic, synonym matching, and fuzzy matching.
- **Manual UI Test:** Check for rendering errors, broken buttons, slow responses.
- Keep a **test dataset** small enough to run searches instantly during demos.    

---

## **7. Emergency Backup Plan**

If embeddings or FAISS integration breaks near deadline:

- Fallback to **keyword search** + synonyms + fuzzy matching.
- Still gives decent search and keeps project functional for judges.    

---

✅ **Phase 4 Deliverable:**  
We now have a **timeboxed, dependency-aware plan** with parallel work streams, early integration, and judge-focused checkpoints. We will be MVP-ready **at least a week before demo day**.
