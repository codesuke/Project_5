# **Team Workflow & Management Plan**

### **1. Roles & Responsibilities (Development Tracks)**

We lock **1 person = 1 primary module**, but they also have a backup/support task.

| Person                              | Primary Module                              | Backup Task                             |
| ----------------------------------- | ------------------------------------------- | --------------------------------------- |
| **Person 1 (Lead Dev)**             | Backend Architecture + AI Chat + OCR        | Code reviews + final merges             |
| **Person 2 (Frontend Lead)**        | Page layouts + Chat UI                      | Dashboard frontend support              |
| **Person 3 (Auth Specialist)**      | Auth API + DB models                        | Data persistence for other modules      |
| **Person 4 (Dashboard Specialist)** | Analytics backend + Chart.js visualizations | OCR result integration                  |
| **Person 5 (QA + Enhancer)**        | Weekly testing + bug tracking               | Small UI features + presentation assets |

---

### **2. Development Workflow (No Khichdi Rules)**

#### **a. Branching Strategy (GitHub)**

- `main` → **Only stable, tested code** (you control merges here).
    
- `dev` → Shared integration branch (everyone pushes here after testing).
    
- `feature/<module>` → One branch per feature (example: `feature/auth`, `feature/chat`).
    

**Flow:**

1. Person pulls from `main`.
    
2. Creates/works on `feature/...` branch.
    
3. Tests locally.
    
4. Makes a Pull Request (PR) → PR reviewed by _you or QA_.
    
5. PR merged into `dev`.
    
6. After team testing → `dev` merged into `main`.
    

---

#### **b. Commit Rules**

- **Atomic commits** → Small, logical changes (not “added stuff lol”).
    
- Commit message format:
    
    ```
    feat(auth): add JWT login endpoint
    fix(chat): handle empty input crash
    style(ui): improve dashboard color scheme
    ```
    
- **NEVER** commit directly to `main`.
    

---

#### **c. Parallel Dev Strategy**

To avoid conflicts:

- Frontend team uses **mock JSON APIs** until backend is ready.
    
- Backend team tests APIs in **Postman** before handing to frontend.
    
- Data structures (API responses) are **documented early** in a shared Notion/Google Doc.
    

---

### **3. Project Management Tools**

**GitHub Projects (Kanban Board)** → Columns:

- **Backlog** (Not started yet)
    
- **In Progress** (Assigned tasks)
    
- **Testing** (QA reviewing)
    
- **Done** (Approved & merged to main)
    

Each task card includes:

- Description
    
- Owner
    
- Deadline
    
- Related branch/PR link
    

---

### **4. Communication Rules**

- **Daily 15-min standup** (Discord/Meet): Everyone says what they did yesterday, what they’re doing today, blockers.
    
- **Mid-week progress review** → Check if anyone’s falling behind.
    
- If stuck for **>1 hour**, **ask for help immediately** (don’t waste time silently).
    

---

### **5. Integration & Testing Cycles**

- **Every Friday** → Merge all `feature/...` into `dev`, run full integration tests.
    
- **Person 5 (QA)** → Logs bugs in GitHub Issues with clear steps to reproduce.
    
- Only after **two people** verify → Merge into `main`.
    

---

### **6. Deployment Workflow**

- **Frontend:** Auto-deploy from `main` → Netlify
    
- **Backend:** Auto-deploy from `main` → Render/Vercel
    
- QA tests staging build before demo days.
    

---

💡 **Why this avoids khichdi:**

- Everyone works in **isolated branches**.
    
- API contracts are frozen early → no random changes mid-dev.
    
- Weekly merges mean bugs are caught before they pile up.
    
- You’re the **merge gatekeeper** — nothing touches `main` without your green light.
    

---
