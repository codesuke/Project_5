# **Phase 1 – Extraction**

## **1. Problem in One Sentence**

We need to build an **AI-powered semantic search tool** that lets users quickly find the right NCO occupation code from NCO-2015 using **natural language queries**, with multilingual and voice support, plus an admin interface for data updates.

---

## **2. Core Use Cases (Must-Have)**

|#|Use Case|Actor|Trigger|Outcome|
|---|---|---|---|---|
|1|Search by job title in English|Enumerator / Officer|User types "tailor"|Returns top matching codes with confidence scores|
|2|Search by detailed job description|Enumerator / Officer|User types "repairs scooter engines"|Returns relevant occupation codes|
|3|Handle synonyms/context|System|User types "sewing worker"|Finds "Sewing Machine Operator"|
|4|Show ranked results|System|After search query|Top N results sorted by relevance|
|5|Handle typos & ambiguous queries|System|User types "mechnic"|Shows corrected search or close matches|
|6|Data ingestion & indexing|Admin|Uploads NCO dataset|Data processed and embeddings generated|
|7|Admin updates database|Admin|Adds new occupation|Search updated automatically|
|8|Display hierarchical structure|System|Search result found|Show code with sector/division/sub-group info|
|9|Confidence score display|System|After search|User sees “confidence: 0.92”|
|10|Basic UI|Enumerator / Officer|Open app|Search box, result list, and selection option|

---

## **3. Optional / Wow-Factor Use Cases**

|#|Feature|Actor|Outcome|
|---|---|---|---|
|1|Multilingual text search|User|Search in Hindi/regional language|
|2|Voice input search|User|Speak job title, get result|
|3|Offline mode|User|Search works without internet|
|4|Synonym bank editor|Admin|Update/add synonym mappings|
|5|Usage dashboard|Admin|See query stats, top searched jobs|
|6|Advanced filters|User|Filter by sector, skill level, location relevance|
|7|Contextual suggestions|System|Suggest related roles|

---

## **4. Actors – Role Mapping**

|Actor|Responsibility|
|---|---|
|Enumerator|Query system for codes during surveys|
|Employment Officer|Lookup codes for official records|
|Admin|Upload/update dataset, manage synonyms, view logs|
|System|Process NLP queries, return ranked results, manage embeddings|

---

## **5. Triggers**

- **User Action**: Typing job title/description
- **User Action**: Speaking into mic
- **Admin Action**: Uploading new dataset
- **System Event**: New model version deployed
- **Error Handling Trigger**: Query returns no results

---

## **6. Outcomes**

- **Direct**: Fast, accurate occupation code lookup    
- **Indirect**: Reduced training time, improved classification accuracy, higher survey efficiency

---

## **7. Required Data & APIs**

|Need|Example / Option|
|---|---|
|NCO-2015 structured dataset|CSV, JSON, or extracted from PDF|
|NLP embedding model|BERT, IndicBERT, Sentence Transformers|
|Vector store|FAISS, Pinecone, Weaviate|
|Voice recognition|Google Speech-to-Text, Vosk|
|Translation|IndicTrans2, Google Translate|
|Web framework|Flask/FastAPI (backend), React/Vue (frontend)|

---

## **8. Clarification Questions for Mentors**

1. Can we store embeddings in **cloud DBs** like Pinecone, or must it be offline?
2. Is voice/multilingual a **must for MVP** or later?
3. Are there **UI constraints** (mobile-only, web, kiosk)?
4. Any **security/compliance** requirements for storing queries?
5. What’s the **max dataset size** we need to handle?
6. Should the **confidence score threshold** be configurable?    
