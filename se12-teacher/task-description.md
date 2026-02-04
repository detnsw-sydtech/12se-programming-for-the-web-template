# Task Description – Teacher Reference  
## SE12 Programming for the Web (Stage 6 Software Engineering)

This document provides the **teacher‑annotated version** of the assignment brief.  
It mirrors the student version but includes:

- teaching intent  
- clarification of requirements  
- common misconceptions  
- guidance for introducing the task  
- differentiation notes  
- assessment alignment  

Use this version when presenting the task, planning lessons, and supporting students.

---

# 📘 Assignment Overview

Students will design and develop a **catalogue‑style Progressive Web Application (PWA)** that:

- displays structured data from a **SQLite database**  
- retrieves data through an **Express server**  
- presents information through a **clean, accessible UI**  
- includes **PWA features** such as a manifest and service worker  
- demonstrates **testing**, **debugging**, and **documentation** skills  

This task assesses the full stack of web development skills taught in the unit.

---

# 🎯 Learning Intent (Teacher Notes)

This assignment is designed to:

- consolidate front‑end and back‑end skills  
- introduce students to real‑world web architecture  
- build confidence with SQL and server‑side logic  
- reinforce version control and documentation practices  
- prepare students for senior‑level software engineering tasks  

**Teacher Tip:**  
Emphasise that this is not a “website project” — it is a **software engineering task** requiring structure, logic, and documentation.

---

# 🧩 Core Requirements (Teacher Clarifications Included)

## **1. Front‑End Interface (HTML/CSS/JS)**  
Students must create:

- a clean, accessible UI  
- responsive layout  
- a page that fetches and displays JSON data  
- basic interactivity (e.g., buttons, navigation, filtering if desired)

**Common Misconception:**  
Students often think “responsive” means “looks okay on a laptop.”  
Model mobile‑first design early.

---

## **2. Backend Server (Node.js + Express)**  
Students must:

- create an Express server  
- serve static files  
- create at least one API route returning JSON  
- handle errors safely  

**Teacher Note:**  
Encourage students to test routes using REST Client or Postman before connecting the front‑end.

---

## **3. Database (SQLite + SQL)**  
Students must:

- design a simple schema  
- create a SQLite database  
- write SQL queries to retrieve data  
- connect SQL results to Express routes  

**Teacher Note:**  
Students often forget to handle SQL errors.  
Model a safe pattern:

```js
db.all("SELECT * FROM items", [], (err, rows) => {
  if (err) return res.status(500).json({ error: err.message });
  res.json(rows);
});
```

## 4. Progressive Web App Features

Students must include:

- `manifest.json`
- app icons
- a basic service worker
- offline caching of essential files
- installability

**Teacher Note:**  
Keep PWA requirements simple. Students do **not** need advanced caching strategies.

---

## 5. Testing and Debugging

Students must:

- test UI behaviour
- test API routes
- test SQL queries
- test PWA installability
- document issues and fixes

**Teacher Tip:**  
Encourage students to screenshot Lighthouse results for documentation.

---

## 6. Documentation

Students must produce:

- a technical overview
- explanation of design choices
- database schema description
- testing evidence
- version control history

**Teacher Note:**  
Documentation is often left to the end — encourage incremental writing.

---

## Submission Requirements

Students must submit:

- their GitHub Classroom repository
- all source code
- SQLite database file
- documentation folder or Markdown file
- working PWA accessible via `localhost`

**Teacher Note:**  
You may choose to require a short video walkthrough for students who struggle with written documentation.

---

## Assessment Alignment (Teacher Interpretation)

This task assesses:

- **Design** (UI/UX, structure, accessibility)
- **Backend logic** (Express routes, SQL queries)
- **Data handling** (JSON, schema design)
- **Testing** (functional + PWA criteria)
- **Documentation** (clarity, accuracy, completeness)

High‑band work demonstrates:

- efficiency
- structure
- security awareness
- professional documentation
- consistent version control

---

## Common Student Pitfalls

- Hard‑coding JSON instead of using SQL
- Forgetting to export the database file
- Incorrect file paths in service workers
- Manifest not linked correctly
- SQL queries returning empty arrays
- Using `fetch()` incorrectly (missing `await` or `.then`)
- Not testing routes before connecting the UI

**Teacher Strategy:**  
Run a mid‑project checkpoint where students must demonstrate:

- working SQL query  
- working Express route  
- working fetch request  

This prevents last‑minute collapse.

---

## Differentiation Notes

### For high‑ability students:
- Add search or filtering
- Add sorting
- Add multiple database tables
- Add more advanced caching strategies

### For students needing support:
- Provide a starter Express server
- Provide a partially completed database
- Provide a UI skeleton
- Use pair programming for debugging

---

## Introducing the Task (Teacher Script)

A recommended introduction:

> “In this assignment, you’re going to build a small but complete web application — not just a website. You’ll design the interface, build the server, create the database, and connect everything together. This is the same architecture used in real software engineering teams.”

This framing helps students understand the professional relevance.

---

## Teacher‑Only Notes

- This file is **not** included in student repositories.
- You may adapt the brief for differentiation or accessibility needs.
- Keep the student version clean and free of teacher commentary.

