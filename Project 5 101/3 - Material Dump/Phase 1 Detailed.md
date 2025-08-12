## Phase 1 – Extraction

### **1. Plain English Problem Statement**

We are tasked with creating a system that addresses the needs outlined in the provided use cases, ensuring that the platform is **functional, intuitive, and efficient**. It must allow users and administrators to perform their specific actions seamlessly while leveraging available APIs/data sources to deliver meaningful results.

---

### **2. Core Use Cases (MUST-HAVE for MVP)**

|ID|Use Case|Actor(s)|Trigger|Outcome|
|---|---|---|---|---|
|UC1|**User Registration & Authentication**|User|Signs up or logs in|User is securely authenticated and can access system features|
|UC2|**Data Upload & Storage**|User|Uploads data file|Data is validated and stored for processing|
|UC3|**Data Search & Retrieval**|User|Enters query|Relevant data is fetched and displayed|
|UC4|**Data Visualization**|User|Requests report|Data is shown in charts, graphs, or summaries|
|UC5|**Admin Data Management**|Admin|Updates/deletes records|System reflects changes for all users|

---

### **3. Optional Use Cases (Nice-to-Have)**

|ID|Feature|Actor(s)|Benefit|
|---|---|---|---|
|OC1|Advanced Search Filters|User|Improves result accuracy and speed|
|OC2|Real-time Collaboration|User|Multiple users can work simultaneously|
|OC3|Predictive Analytics|User/Admin|Adds AI-based insights|
|OC4|Multi-format Export|User|PDF/CSV/Excel export for reports|

---

### **4. Actor / Trigger / Outcome Map**

|Actor|Trigger|Outcome|
|---|---|---|
|**User**|Interacts with UI|Executes core functions like upload, search, visualize|
|**Admin**|Performs data operations|Updates system content|
|**System**|Scheduled or user-triggered event|Automates tasks or fetches data|
|**API/Data Source**|Receives backend request|Returns data for processing|

---

### **5. Required Data / APIs / Tools**

- **Data Sources:** Provided hackathon dataset + public APIs relevant to domain  
- **APIs:** RESTful endpoints for all backend interactions  
    
- **Tools:**
    - **Frontend:** React.js + Tailwind CSS  
    - **Backend:** Node.js + Express.js  
    - **Database:** PostgreSQL (or Firebase for speed)  
    - **Deployment:** Vercel (frontend), Render (backend)  
    - **Collaboration:** GitHub, Figma, Postman  


---

### **6. Clarification Questions for Mentors**

1. Are we free to integrate additional public APIs if they enhance functionality?
2. Is there a preferred hosting/deployment method for judging?
3. Do we need offline support or is online-only acceptable?
4. Are there any restrictions on third-party libraries?
5. What is the maximum data size we need to handle?

---

✅ **Phase 1 Deliverables Complete:**

- Fully clarified scope  
- Concrete MVP features + extras  
- Clear actor/trigger/outcome mapping  
- Tools and APIs identified  
- Mentor questions ready for day one