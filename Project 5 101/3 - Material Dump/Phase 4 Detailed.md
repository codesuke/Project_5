# Phase 4 – MVP Plan (Overkill)

## 🎯 **Objective**

The MVP must be **fully functional by Week 5** — no excuses — so the last 3 weeks are for polish, wow-factor features, bug fixes, and demo prep.  
We’re building **in parallel**, not in a slow linear sequence.

---

## **1. Week-by-Week Timeline**

|Week|Goal|Deliverables|Parallel Streams|
|---|---|---|---|
|**Week 1**|Kickoff & Scaffolding|- GitHub repo set up with `main` + `dev` + branches- Frontend React/Tailwind skeleton- Backend Node/Express skeleton- Database & Supabase project created- Auth system basic setup|- Frontend: Build header, footer, layout- Backend: Hello World API route- DevOps: Hosting connected to `dev` branch|
|**Week 2**|Core System Foundations|- Authentication flow (sign up/login/logout)- Database tables for users/data- File upload API (backend only)|- Frontend: Login/register pages- Backend: API for auth & upload- Testing: Postman tests for each endpoint|
|**Week 3**|Core Data Handling|- Upload connected to DB- Search API built- Display basic search results in frontend|- Backend: Search endpoints- Frontend: Search page UI + call API- DevOps: Basic logging/monitoring|
|**Week 4**|Visualization Layer|- Backend returns aggregated data for charts- Frontend renders charts/tables|- UI/UX: Style dashboard- Backend: Optimize DB queries- Testing: Verify data consistency|
|**Week 5**|**MVP Freeze**|- Full end-to-end flow works:Auth → Upload → Search → Visualization- Deployed version running|- Documentation: README + API docs- Demo-ready stable branch created|
|**Week 6**|Nice-to-Have Features|- Implement OC1 (Advanced Search Filters)- Add error handling & UI polish|- Frontend: Loading states, error messages- Backend: Input validation, API error handling|
|**Week 7**|Wow Factor + Polish|- Add OC4 (Multi-format export)- Add micro-interactions in UI- Prepare final dataset for judging|- Stress testing & performance tuning|
|**Week 8**|Demo Prep|- Script final demo- Record fallback demo video- Prepare slides- Full dry-run|- QA: Test every feature end-to-end- Create backup database & deployment|

---

## **2. Milestone Checkpoints**

We don’t wait for “later” to discover something’s broken.  
At each checkpoint:

- **Functional test** (user flow works)
    
- **Code quality check** (no commented-out junk, linted)
    
- **Deployment check** (live version matches local)
    

|Milestone|Deadline|What’s Tested|
|---|---|---|
|**M1 – Scaffold Done**|End of Week 1|Repo, hosting, skeleton apps|
|**M2 – Auth Working**|Mid-Week 2|Login/register flow works live|
|**M3 – Upload + DB**|End of Week 3|File upload saves to DB/storage|
|**M4 – Search Live**|Mid-Week 4|Queries return correct results|
|**M5 – MVP Freeze**|End of Week 5|Full flow live & stable|

---

## **3. Parallel Work Streams (So We Don’t Bottleneck)**

- **Stream 1 – Frontend:** Build pages with dummy data, integrate APIs when backend is ready.
    
- **Stream 2 – Backend:** Build API routes with mock responses, connect DB later.
    
- **Stream 3 – UI/UX:** Work in Figma from Day 1, keep updating designs.
    
- **Stream 4 – Testing/DevOps:** Deploy early, test every merge, keep `dev` live at all times.
    

💡 **Rule:** If you’re blocked waiting for another team, you **switch to another feature or testing** — no idle time.

---

## **4. Demo-Readiness Strategy**

We prep for the demo **as early as Week 5**, not the night before:

- Keep a **demo branch** that’s always working.
    
- Record a **backup video demo** in Week 7 in case the live app dies.
    
- Demo flow: Problem → Solution → Live demo → Impact → Wow feature.
    

---

✅ **Phase 4 Output:**

- MVP done by Week 5 guaranteed.
    
- Risk of “last week coding all night” eliminated.
    
- Parallel work to keep beginners productive.
    
- Demo prep baked into the schedule.
    

