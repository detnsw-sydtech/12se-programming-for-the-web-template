# 📘 **Programming for the Web – Unit Overview**  
### Software Engineering Stage 6 (Year 12)

---

## 🌐 **About This Unit**

**Programming for the Web** focuses on designing, developing, and testing **interactive**, **secure**, and **data‑driven** web applications. Students learn to build functional systems using **HTML**, **CSS**, **JavaScript**, and **SQL**, supported by modern development practices such as **version control**, **testing**, and **documentation**.

This repository provides the full student booklet, appendices, and teacher resources for delivering the unit.

---

## 🎯 **Key Outcome Descriptors**

### 🎨 **Design and Structure**  
Students demonstrate understanding of **User Interface (UI)** and **User Experience (UX)** principles, creating functional and accessible **HTML/CSS** layouts.

### 🗄️ **Backend & Data Management**  
Students organise, store, and retrieve data using **SQL**, designing and managing database interactions effectively.

### 🧠 **Programming Methodology**  
Students implement efficient, maintainable code, apply **version control**, and use **code libraries** appropriately.

### 🧪 **Testing and Debugging**  
Students test and debug web applications, identify issues, and ensure the system behaves as intended.

### 📄 **Documentation**  
Students produce clear, structured **technical documentation** explaining code structure, design decisions, and testing processes.

---

## 🏅 **Performance Bands (A–E)**  
Aligned with the **Teacher Support Resource** and **Syllabus Outcomes**.

---

### 🟩 **Band A – Outstanding Achievement**  
Students demonstrate **advanced mastery** of web development concepts.  
They:

- Develop **complex**, **robust**, and **well‑structured** web applications  
- Implement **secure backend data handling**  
- Produce **highly efficient**, **well‑documented** code  
- Use **version control**, **libraries**, and **best practices** extensively  
- Show strong independence and problem‑solving ability  

---

### 🟦 **Band B – High Achievement**  
Students demonstrate **strong proficiency** and consistent application of skills.  
They:

- Build **responsive**, **functional**, and **secure** applications  
- Apply SQL and backend logic effectively  
- Use version control appropriately  
- Provide clear documentation and testing evidence  

---

### 🟨 **Band C – Sound Achievement**  
Students demonstrate **competent understanding** of core concepts.  
They:

- Develop **functional** web applications using HTML, CSS, SQL, and basic JavaScript  
- Apply **basic programming methodologies**  
- Conduct testing and provide **basic documentation**  
- Show developing confidence with backend processes  

---

### 🟧 **Band D – Basic Achievement**  
Students demonstrate **partial understanding** of required concepts.  
They:

- Produce **simple**, functional code with limited styling  
- Show emerging understanding of **database interaction**  
- Require support to debug and structure their work  
- Provide minimal documentation  

---

### 🟥 **Band E – Developing Achievement**  
Students demonstrate **limited progress** toward outcomes.  
They:

- Produce **very simple** or incomplete code  
- Show minimal understanding of web structure or SQL  
- Require significant guidance to complete tasks  
- Provide little or no documentation  

---

## 📌 **Common Assessment Criteria**

### ✔️ **Accuracy**  
Correct use of **HTML tags**, **CSS properties**, **JavaScript syntax**, and **SQL statements**.

### ⚙️ **Functionality**  
The application behaves as intended, with no major errors or broken features.

### 🚀 **Efficiency**  
Code is **clean**, **readable**, and **optimised**, not just functional.

### 📝 **Documentation**  
Clear explanation of:

- Code structure  
- Design choices  
- Testing processes  
- Database schema  

---

## 📂 **Repository Structure**

```bash
SE12-student/      → Student booklet and appendices
SE12-teacher/      → Teacher-only resources, marking guides, solutions
public/            → Front-end assets (if included in template)
src/               → Server, database, and logic files
LICENSE            → MIT License
README.md           → This file
```

---

## 🚀 **Using This Template in GitHub Classroom**

This repository is designed to be used as a **template** for individual student assignments.  
When linked to GitHub Classroom, each student receives a **private**, **markable**, **independent** copy.

---

## 🗂️ Repository Architecture Diagram

```mermaid
flowchart TB

    classDef bigText font-size:18px,fill:#f5f5f5,stroke:#333,stroke-width:1px,padding:20px;

    ROOT["📦 12se-programming-for-the-web-template"]
    STU["📘 SE12-student — Student Booklet and Appendices"]
    TEA["🧑‍🏫 SE12-teacher — Teacher Resources and Marking Guides"]
    SRC["🛠️ src/ — Server, Database, Logic"]
    PUB["🌐 public/ — Front-end Assets"]
    README["📄 README.md"]
    LICENSE["⚖️ LICENSE (MIT)"]

    ROOT --> STU
    ROOT --> TEA
    ROOT --> SRC
    ROOT --> PUB
    ROOT --> README
    ROOT --> LICENSE

    class ROOT,STU,TEA,SRC,PUB,README,LICENSE bigText;
