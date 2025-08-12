# Phase 3 – Tech Blueprint (Overkill Mode)

## **1. Tech Stack – Optimized for Speed + Stability**

We’re not experimenting with fancy untested stuff. We’re picking **battle-tested tools** so we can move fast without debugging frameworks all weekend.

|Layer|Choice|Reason|
|---|---|---|
|**Frontend**|**React + Vite**|Fast dev server, hot reload, easy to split components, works for beginners|
|**UI Library**|**TailwindCSS**|No CSS hell, quick prototypes|
|**Backend API**|**FastAPI (Python)**|Async support, beginner-friendly, integrates with ML easily|
|**Search/NLP**|**Sentence Transformers (all-MiniLM-L6-v2)**|Lightweight, fast, good semantic quality|
|**Vector DB**|**FAISS** (local)|No external dependency risk, blazing fast search|
|**Data Store**|**SQLite** (for structured data)|Lightweight, zero-config|
|**Voice Input** (optional later)|**Vosk** (offline) or Google STT|Works offline for MVP if needed|
|**Multilingual** (optional later)|**IndicBERT + IndicTrans2**|Native support for Indian languages|
|**Deployment**|**Docker** + Railway/Render (cloud)|Containerized, zero “works on my machine” drama|
|**Version Control**|**GitHub**|Free CI/CD, easy PR workflow|

---

## **2. System Architecture**

### **Flow Overview**

1. **Data Ingestion Pipeline**
    
    - Admin uploads CSV/JSON of NCO data → ingestion script cleans + normalizes → generate embeddings → store in FAISS + SQLite.
        
2. **Query Handling**
    
    - User sends query (text or later voice) → preprocessing (lowercase, normalize, remove stopwords) → embeddings generated → FAISS similarity search → results with confidence scores → map to NCO hierarchy → send to frontend.
        
3. **Frontend**
    
    - Search bar → result cards with code, title, sector, confidence.
        
    - Minimal but judge-friendly UI with emphasis on **speed**.
        

---

### **Architecture Diagram (Text Form)**

```
[User Browser] 
    ↓ (search query)
[React + Tailwind UI] 
    ↓ REST API request (JSON)
[FastAPI Backend]
    ├── [Preprocessing Module]
    ├── [Embedding Generator - Sentence Transformers]
    ├── [Vector DB - FAISS] → returns top matches
    └── [SQLite DB] → fetch hierarchical metadata
    ↓
[JSON Response with results + confidence]
    ↓
[Frontend Renders Ranked List]
```

---

## **3. Branching Strategy – Chaos Prevention**

We’re running a **feature-branch model** with strict PR rules.

|Branch|Purpose|
|---|---|
|`main`|Always deploy-ready, protected branch|
|`dev`|Integration branch, merges from feature branches|
|`feature/*`|One branch per feature (e.g., `feature/frontend-search`)|
|`hotfix/*`|Urgent bug fixes from `main`|

**Rules:**

- No direct commits to `main`.
    
- PR → Code Review → Merge to `dev` → Tested → Merge to `main`.
    
- Beginners get “safe” tasks with **mentored PR reviews**.
    

---

## **4. Development Workflow – No Merge Wars**

1. **Task assigned** → Create feature branch (`feature/<name>`).
    
2. Commit often, push daily.
    
3. Pull latest `dev` before pushing to avoid conflicts.
    
4. Test locally before PR.
    
5. One person merges PR after review.
    

---

## **5. Team Role Allocation**

We split by skill and dependencies to avoid idle waiting.

|Role|Person|Main Tasks|
|---|---|---|
|**Backend Lead**|Strongest Python dev|FastAPI setup, NLP pipeline, FAISS integration|
|**Frontend Lead**|React/Tailwind expert|Search UI, result display|
|**Data Engineer**|Someone patient|Parse NCO-2015 dataset, create JSON/CSV|
|**ML/NLP Engineer**|Good with Python + ML libs|Embedding model integration, synonym handling|
|**Beginner Dev 1**|Learner|Write basic API routes, handle UI forms|
|**Beginner Dev 2**|Learner|Implement result card components|
|**QA / Tester**|Detail-oriented|Test MVP features, record bugs, manage demo data|
|**Project Manager**|Me + You|Oversee progress, unblock, keep repo clean|

---

## **6. Testing Workflow**

- **Unit tests** for backend functions (search, data parsing).
    
- **Smoke test** every morning on dev branch.
    
- **Manual functional test** before merging to main.
    
- Use **Postman** for API endpoint testing.
    
- Use **sample queries** like:
    
    - "tailor"
        
    - "mechanic for bikes"
        
    - misspelled: "mechnic"
        
    - contextual: "garment stitcher"
        

---

## **7. Beginner-Friendly Safety Nets**

- Pre-configured `.devcontainer` or Docker so no one spends hours on setup.
    
- Starter scripts for running backend (`run_backend.sh`) and frontend (`run_frontend.sh`).
    
- `README.md` with **copy-paste commands**.
    
- A **data subset** for local testing (no heavy downloads needed).
    

---

✅ **Phase 3 Deliverable:**  
We now have the **stack locked**, **architecture mapped**, **roles assigned**, **workflow enforced**, and **merge chaos prevention plan** ready. Everyone knows exactly what they’re doing and where their code lives.
