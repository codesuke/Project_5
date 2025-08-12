# Phase 2 – Deep Analysis

## **1. Impact vs. Effort Analysis**

Here’s a quick prioritization so beginners don’t drown and we still deliver something impressive.

|Feature|Impact|Effort|Notes / Risks|Decision|
|---|---|---|---|---|
|English text search|High|Low|Simple input, embedding search|✅ Must-have|
|Semantic understanding via embeddings|High|Medium|Pre-trained models are available; just integrate|✅ Must-have|
|Synonym/context handling|High|Medium|Can start with static mapping, expand later|✅ Must-have|
|Ranked results + confidence score|High|Low|Easy once embeddings work|✅ Must-have|
|Data ingestion & indexing|High|Medium|One-time script + periodic updates|✅ Must-have|
|Typos & fuzzy matching|Medium|Low|Use string similarity fallback|✅ Must-have|
|Hierarchical code display|Medium|Low|Display from dataset structure|✅ Must-have|
|Multilingual search|High|Medium-High|Requires translation or multilingual model|🔄 Later phase if time|
|Voice input|Medium|Medium|Speech-to-text integration|🔄 Later phase if time|
|Admin panel for updates|Medium|Medium-High|Build after core search is stable|🔄 Later phase|
|Usage dashboard|Low|Medium|Not essential for MVP|❌ Drop for hackathon|
|Advanced filters|Low|Medium|Feature creep risk|❌ Drop for hackathon|
|Contextual suggestions|Medium|Medium|Can be phase 2 after MVP|🔄 Later|

---

## **2. Kill / Postpone Risky Features**

**Kill for Hackathon:**

- Usage dashboard (low judge value vs. time sink)
    
- Complex advanced filters (overkill for MVP)
    

**Postpone to Post-MVP/Wow phase:**

- Multilingual
    
- Voice input
    
- Contextual suggestions
    
- Full-featured admin panel
    

---

## **3. Dependencies Mapping**

|Feature|Dependencies|
|---|---|
|Semantic search|NCO dataset cleaned + embeddings + vector DB|
|Synonym handling|Pre-built synonym dictionary + integration into search pipeline|
|Typos handling|String similarity / fuzzy matching library|
|Data ingestion|File parsing + normalizing + storing in DB/vector DB|
|Hierarchical display|NCO dataset structure preserved|
|Multilingual search|Translation model or multilingual embeddings|
|Voice input|Speech-to-text API + search integration|

---

## **4. Definition of Done (DoD) – For MVP**

For each must-have feature, here’s how we’ll know it’s done and judge-ready:

|Feature|DoD|
|---|---|
|English text search|User can type any job title/description and get correct NCO codes|
|Semantic search|Queries like "garment stitcher" return "Sewing Machine Operator"|
|Synonym handling|“Tailor” and “Sewing machine operator” both lead to same code|
|Ranked results|Top N results sorted by confidence|
|Data ingestion|One-click ingestion of CSV/JSON updates search instantly|
|Typos handling|Misspelling like “mechnic” still finds “Mechanic”|
|Hierarchical display|Each result shows full NCO path|
|UI|Search box, results list, basic styling|

---

## **5. Risk Mitigation**

- **Data parsing delays?** → Start with a pre-cleaned subset of NCO data to develop search first.
- **Model performance bad?** → Keep a fallback to simple keyword search.
- **Merge conflicts?** → Lock branching strategy early (covered in Phase 3).
- **Time loss due to team skill gaps?** → Assign “critical path” tasks to strongest devs, safe tasks to beginners.


---

✅ **Phase 2 Deliverable:**  
We now have **locked MVP scope**, **killed scope creep**, and **set clear done criteria**. No one can say “let’s add this one cool feature” without knowing it will hurt the finish line.

