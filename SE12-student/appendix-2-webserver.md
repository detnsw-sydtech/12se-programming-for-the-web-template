# Appendix 2 – Web Server Guide  
### Programming for the Web – Software Engineering Stage 6 (Year 12)

This guide explains how a web server works and how you will use **Node.js** and **Express** to build the back‑end of your Progressive Web App (PWA). 

The server is responsible for handling requests, processing data, and sending responses to the front‑end.

---

## 🌐 What Is a Web Server?

A **web server** is software that:

- Listens for incoming requests from a browser  
- Processes those requests  
- Sends back a response (HTML, CSS, JavaScript, JSON, images, etc.)  

In this unit, you will build your own server using:

- **Node.js** → runs JavaScript on the server  
- **Express.js** → a framework that makes server development easier  

---

## 🧩 How the Client–Server Model Works

Your PWA uses a **client–server architecture**:

### **Client (Front‑End)**
- Runs in the browser  
- Displays the user interface  
- Sends requests to the server  
- Receives and displays data  

### **Server (Back‑End)**
- Runs on Node.js  
- Uses Express to handle requests  
- Connects to the SQLite database  
- Sends JSON data back to the client  

---

## 🚀 Setting Up an Express Server

A basic Express server looks like this:

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.use(express.static("public"));

app.get("/", (req, res) => {
  res.sendFile(__dirname + "/public/index.html");
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
