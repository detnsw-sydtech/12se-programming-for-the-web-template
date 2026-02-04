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

