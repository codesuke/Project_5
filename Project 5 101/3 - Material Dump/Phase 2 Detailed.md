# Phase 2 – Deep Analysis (Finalized)

### **1. Impact vs. Effort Matrix**

**Legend:**
- **Impact:** 1 (low) → 5 (high) — how much value it brings to solving the problem & impressing judges.
- **Effort:** 1 (low) → 5 (high) — how hard/time-consuming it is to implement.

|ID|Feature|Impact|Effort|Priority|Notes|
|---|---|---|---|---|---|
|UC1|User Registration & Authentication|5|2|**P1**|Must-have for controlled access|
|UC2|Data Upload & Storage|5|3|**P1**|Core to platform functionality|
|UC3|Data Search & Retrieval|5|3|**P1**|Directly tied to usability|
|UC4|Data Visualization|4|3|**P1**|Increases clarity & appeal in demo|
|UC5|Admin Data Management|3|2|P2|Needed for maintainability, can be built after MVP|
|OC1|Advanced Search Filters|4|3|P2|Adds polish, but MVP can work without it|
|OC2|Real-time Collaboration|3|5|**Kill for MVP**|High effort, not core|
|OC3|Predictive Analytics|4|5|**Kill for MVP**|Nice but risky under time constraints|
|OC4|Multi-format Export|3|3|P3|Post-MVP bonus feature|

---

### **2. Dependencies**

|Feature|Depends On|
|---|---|
|UC2 Data Upload & Storage|UC1 Authentication|
|UC3 Data Search & Retrieval|UC2 Data Upload & Storage|
|UC4 Data Visualization|UC3 Data Search & Retrieval|
|OC1 Advanced Search|UC3 Data Search & Retrieval|
|OC3 Predictive Analytics|UC2, UC3, OC1|
|OC4 Export Reports|UC4 Visualization|

---

### **3. Kill/Delay Risky Features**

- **Kill for MVP:**
    
    - OC2 Real-time Collaboration (high effort, sync complexity)
    - OC3 Predictive Analytics (needs significant ML dev time)
- **Delay for Post-MVP:**
    
    - OC1 Advanced Search Filters
    - OC4 Multi-format Export

---

### **4. Definition of Done (DoD) for Each Feature**

|Feature|DoD|
|---|---|
|UC1 Authentication|User can sign up/login/logout securely, tested with 3 test accounts|
|UC2 Data Upload|User can upload files, system stores & validates them, confirmed by DB entry|
|UC3 Search & Retrieval|User can enter keyword/query and get relevant results in <2 seconds|
|UC4 Visualization|User can generate chart/table from stored data with correct values|
|UC5 Admin Management|Admin can update/delete records & changes are reflected in real time|

---

✅ **Phase 2 Output:**

- Clear priorities (P1 = build now, P2 = after MVP, Kill = ignore)
- Dependencies mapped to avoid bottlenecks
- Risky features removed from MVP
- Each feature has a concrete “done” state to prevent scope creep
