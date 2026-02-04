# Unit Overview – Teacher Reference  
## SE12 Programming for the Web (Stage 6 Software Engineering)

This document provides a **teacher‑focused overview** of the unit, aligned with the NSW Stage 6 Software Engineering syllabus.  
It mirrors the student version but includes:

- teaching intent  
- pedagogical notes  
- common misconceptions  
- suggested demonstrations  
- differentiation strategies  
- assessment alignment  

---

## 🎯 Purpose of the Unit

**Programming for the Web** introduces students to the design and development of **interactive**, **data‑driven**, and **secure** web applications.  
Students learn to integrate:

- **Front‑end development** (HTML, CSS, JavaScript)  
- **Back‑end logic** (Node.js + Express)  
- **Database management** (SQLite + SQL)  
- **Progressive Web App (PWA)** concepts  
- **Testing and documentation** practices  

The unit culminates in a **catalogue‑style PWA** that demonstrates full‑stack capability.

---

## 🧩 Key Syllabus Outcomes (Teacher Interpretation)

### **1. Design and Structure**  
Students must demonstrate understanding of:

- UI/UX principles  
- responsive layout  
- accessibility considerations  
- semantic HTML  

**Teacher Notes:**  
- Students often jump straight into styling; emphasise structure first.  
- Demonstrate how poor structure affects screen readers and Lighthouse scores.  

---

### **2. Backend & Data Management**  
Students must:

- design a simple relational schema  
- write SQL queries (SELECT, INSERT, UPDATE, DELETE)  
- connect Express routes to database operations  
- return JSON to the front‑end  

**Teacher Notes:**  
- Many students struggle with async behaviour in Node.js.  
- Provide a simple “query → callback → JSON response” demonstration early.  

---

### **3. Programming Methodology**  
Students must:

- write maintainable, modular code  
- use version control (Git + GitHub)  
- understand libraries and dependencies  
- follow consistent naming and formatting conventions  

**Teacher Notes:**  
- Encourage frequent commits with meaningful messages.  
- Model folder structure early to avoid student repo chaos.  

---

### **4. Testing and Debugging**  
Students must:

- test routes, SQL queries, and UI behaviour  
- use browser dev tools  
- identify and fix errors  
- validate PWA installability  

**Teacher Notes:**  
- Students often test only the UI; explicitly teach API testing.  
- Recommend VS Code REST Client or Postman for route testing.  

---

### **5. Documentation**  
Students must produce:

- technical documentation  
- explanation of design choices  
- testing evidence  
- database schema description  

**Teacher Notes:**  
- Provide exemplars of concise, professional documentation.  
- Encourage students to document as they go, not at the end.  

---

## 🧭 Suggested Unit Sequence (High‑Level)

1. **Introduction to Web Architecture**  
2. **Front‑end fundamentals (HTML/CSS/JS)**  
3. **Server‑side development with Express**  
4. **Database creation + SQL queries**  
5. **Connecting server routes to SQL**  
6. **Rendering JSON data in the front‑end**  
7. **PWA concepts (manifest + service worker)**  
8. **Testing, debugging, and optimisation**  
9. **Documentation + final submission**  

**Teacher Notes:**  
- This sequence aligns with cognitive load principles: front‑end → backend → integration → enhancement.  
- Avoid introducing PWAs too early; students need a working app first.  

---

## ⚠️ Common Misconceptions

- “A PWA is just a website with a manifest.”  
- “SQL is only for big databases.”  
- “Express automatically sanitises input.”  
- “Service workers update instantly.”  
- “JSON and JavaScript objects are the same thing.”  

**Teacher Strategy:**  
Use short, targeted demonstrations to correct these early.

---

## 🎓 Differentiation Strategies

### For high‑ability students:
- Introduce optional features (search, filtering, sorting).  
- Encourage modularisation and reusable components.  
- Allow exploration of advanced SQL (JOINs, constraints).  

### For students needing support:
- Provide partially completed starter files.  
- Use visual schema diagrams before writing SQL.  
- Pair programming for debugging sessions.  

---

## 📝 Assessment Alignment

The assignment assesses:

- **Design** (UI/UX, structure, accessibility)  
- **Backend logic** (Express routes, SQL queries)  
- **Data handling** (JSON, schema design)  
- **Testing** (functional + PWA criteria)  
- **Documentation** (clarity, accuracy, completeness)  

**Teacher Notes:**  
- Ensure students understand that **functionality alone is not enough** for high‑band achievement.  
- Emphasise efficiency
