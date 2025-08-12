## Understanding the Problem Statement – NCO Semantic Search

### **What’s the Core Issue?**

Right now, **finding the right occupation code in NCO-2015** is like looking for a needle in a haystack made of government PDFs.  
People:

- Scroll through giant documents
- Search by exact keywords (no typo tolerance, no “close match” smarts)
- Need to know the NCO hierarchy inside-out just to find basic jobs

This makes the process **slow, error-prone, and exhausting**.

---

### **Why Is This a Problem?**

- Wrong codes → Bad data → Bad policies    
- Takes too long for people in the field (survey enumerators, officers)
- Scaling is a nightmare — India’s workforce is huge and diverse
- Not everyone searches in perfect English — they use Hindi/regional languages or voice

---

### **What’s the Goal?**

**Build an AI-powered search tool** where someone can type or say a job title (in English, Hindi, or other languages) and get:

- The correct NCO occupation code(s)
- Ranked results with a **confidence score**
- Synonym/context awareness (e.g., “tailor” should find “Sewing Machine Operator”)
- Easy interface for both field users and admins

---

### **Who Will Use It? (Actors)**

1. **Survey Enumerators** – Field staff collecting job data
2. **Employment Officers** – Government staff managing occupational records
3. **Admin Staff** – People maintaining/updating the NCO database
4. **System Itself** – Backend services for NLP, semantic search, indexing

---

### **Triggers**

- User enters text like _“mechanic for scooters”_
- User speaks the query in Hindi
- Admin uploads new/updated occupation data
- Search fails → fallback suggestions triggered

---

### **Desired Outcomes**

- **Primary Outcome**: User gets the correct code in seconds, not minutes
- **Secondary Outcomes**:
    
    - Search understands intent, not just exact words
    - Handles multiple languages and voice
    - Can be maintained easily via an admin dashboard


---

### **Data / APIs Needed**

- **NCO-2015 dataset** (in machine-readable form: CSV, JSON, etc.)
- **Pre-trained NLP models** (e.g., BERT, IndicBERT, Sentence Transformers)
- **Vector database or FAISS** for storing embeddings
- **Optional**: Speech-to-text API (Google, Azure, Vosk) for voice queries
- **Optional**: Translation API for multilingual handling

---

### **Clarification Questions for Mentors**

1. Can we use **external APIs** (Google Translate, Azure STT) or must it be fully offline?
2. Is there a **pre-cleaned NCO-2015 dataset**, or do we have to extract from PDFs?
3. How critical is **multilingual support** for the MVP — must it be in v1 or can it be phase 2?
4. Any restrictions on **cloud hosting** or must it be on-premise?
5. What’s the **expected scale** (number of concurrent users)?
6. How should the **confidence score** be calculated and presented?
7. Any UI/UX accessibility requirements (e.g., offline mode)?
