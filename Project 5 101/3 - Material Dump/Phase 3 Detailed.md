# Phase 3 – Tech Blueprint (Overkill, No Flowcharts)

## **🎯 Objective**

We’re building a tech setup so stable that no matter how beginner the devs are, they can’t accidentally nuke the repo or block progress.  
By the end of this phase:

- The **stack** is final and justified.
- The **architecture** is described in words so everyone understands data flow.
- Team roles are laser-defined.
- Git workflow is strict enough to prevent merge hell.
- Daily dev process is locked.

---

## **1. Tech Stack (Locked & Justified)**

| Layer            | Choice                                                                             | Why This Choice Rocks                                                                         | Backup Option        |
| ---------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | -------------------- |
| **Frontend**     | **React.js + Tailwind CSS**                                                        | Rapid component-based dev, huge community, Tailwind for instant styling without CSS headaches | Vue.js + Vuetify     |
| **Backend**      | **Node.js + Express.js**                                                           | Minimal boilerplate, fast iteration, runs anywhere, beginner-friendly                         | Python + FastAPI     |
| **Database**     | **PostgreSQL via Supabase**                                                        | SQL familiarity, hosted service, built-in authentication, free tier                           | Firebase Firestore   |
| **Auth**         | Supabase Auth                                                                      | Secure, integrated with DB, supports OAuth and email/password instantly                       | Firebase Auth        |
| **File Storage** | Supabase Storage                                                                   | Integrated with Supabase auth & DB                                                            | AWS S3 (if advanced) |
| **Hosting**      | Frontend: Vercel                                                                   | One-click deploy, auto CI/CD from GitHub                                                      | Netlify              |
|                  | Backend: Render                                                                    | Free tier, quick Node deployment, no config headaches                                         | Railway              |
| **Collab Tools** | GitHub (code), Figma (UI/UX), Postman (API testing), Notion/Trello (task tracking) | Jira (if needed)                                                                              |                      |

💡 **Rule for tools:** If it takes >30 mins to set up or learn, we skip it.

---

## **2. Architecture (Text-Only Explanation)**

Our system will work like this:

- **Frontend** (React + Tailwind) will handle all user interaction — forms, buttons, displays, visualizations. It will never directly touch the database.
- **Backend** (Node + Express) will be the “traffic cop,” receiving requests from the frontend, validating inputs, running business logic, and querying the database.
- **Database** (PostgreSQL/Supabase) stores all persistent data — user accounts, uploaded files, search results, logs.
- **Auth Service** (Supabase Auth) ensures only verified users can access features, keeping roles (user/admin) separate.
- **File Storage** (Supabase Storage) handles uploaded documents/media, linked to user accounts.
- **External APIs** (if needed) will be fetched only by the backend to avoid exposing keys.
- The **data flow** will always be → **Frontend → Backend → Database/API → Backend → Frontend**. No shortcuts.

---

## **3. Team Roles (Zero Overlap)**

|Role|Responsibilities|Tools|
|---|---|---|
|**Frontend Lead**|Builds all UI pages/components, integrates API calls, styles with Tailwind, handles responsive design|React, Tailwind, Axios|
|**Backend Lead**|Creates API routes, handles DB queries, sets up middleware, manages data validation|Node, Express, Supabase|
|**UI/UX Designer**|Creates wireframes, prototypes, style guide, ensures user flow is intuitive|Figma|
|**DevOps/Tester**|Sets up hosting, manages environment variables, configures CI/CD, runs integration tests|Vercel, Render, GitHub Actions|
|**Documentation Lead**|Writes README, API reference, user manual, and demo guide|Markdown, Notion|

💡 **Golden Rule:** No two people work on the same file unless they’re pair programming.

---

## **4. Git & Branching Strategy**

We’ll use **GitHub Flow with an integration branch**:

- `main` → Stable, production-ready code for demos.
- `dev` → Integration branch where all tested features go before merging to `main`.
- `feature/<feature-name>` → Each feature/task gets its own branch.
    - Example: `feature/auth-system`, `feature/file-upload`, `feature/data-visualization`

**Rules:**

1. Always pull the latest `dev` before starting a feature.
2. Commit small changes with descriptive messages.
3. No direct commits to `main` or `dev`.
4. At least **one code review** before merging to `dev`.
5. Merge to `main` only after MVP milestone testing.

---

## **5. Development Workflow**

**Daily Flow:**

1. **Morning standup** (10 min): What was done yesterday, what’s next, blockers.
2. Pick tasks from Notion/Trello — every task must have:
    - A short title
    - Owner
    - Due date
    - Subtasks
3. Work in short cycles — commit every 1–2 hours.
4. Push code daily to avoid losing progress.
5. End-of-day mini sync (optional) for merging PRs.

**Testing Before Merge:**

- **Backend:** Test all endpoints with Postman (happy + edge cases).
- **Frontend:** Click through UI, check forms, buttons, and error messages.
- **Integration:** Run through the core user flow at least once after merging to `dev`.

**Safety Practices:**

- `.env` file for all secrets (never committed).
- Use **mock APIs/data** if real API isn’t ready yet.
- Keep a **demo-ready branch** at all times so a crash doesn’t kill our pitch.

---

✅ **Phase 3 Overkill (No Flowcharts) Summary:**

- Beginner-proof stack with instant deploy capability.
- Clear text-based architecture description.
- Roles assigned to avoid collisions.
- Strict Git rules to prevent repo disasters.
- Daily workflow to keep progress consistent and transparent.
