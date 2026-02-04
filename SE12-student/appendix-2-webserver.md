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
```

## What this code does:

- Creates an Express app
- Serves static files from a ```public``` folder
- Sends ```index.html``` when the user visits the home page
- Starts the server on ```localhost:3000```
---

## 🗂 Serving Files to the Browser

Your server can send:

- HTML files
- CSS files
- JavaScript files
- Images
- JSON data

Example route sending JSON:

```javascript
app.get("/data", (req, res) => {
  res.json({ message: "Hello from the server!" });
});
```
---

## 🗄 Connecting to a SQLite Database

Your server will connect to a SQLite database to store and retrieve catalogue data.

Example:

```javascript
const sqlite3 = require("sqlite3").verbose();
const db = new sqlite3.Database("catalogue.db");
```

Query example:

```javascript
app.get("/items", (req, res) => {
  db.all("SELECT * FROM items", [], (err, rows) => {
    if (err) {
      res.status(500).json({ error: err.message });
      return;
    }
    res.json(rows);
  });
});
```

This route:

- Runs a SQL query
- Returns all rows as JSON
- Sends the JSON to the front‑end

---

## 🔄 Request and Response Cycle

1. The browser sends a request (e.g., /items)
2. Express receives the request
3. Express runs a SQL query
4. The database returns results
5. Express sends the results back as JSON
6. The browser displays the data

This cycle is the core of your PWA’s functionality.
---

## 🧪 Testing Your Server

You can test your server using:
- The browser
- VS Code REST Client extension
- Postman
- Terminal tools like curl

Check that:
- Routes return the correct data
- Errors are handled properly
- JSON is formatted correctly
---

## 🔐 Security Basics

Your server should:

- Validate user input
- Avoid exposing database errors
- Use parameterised SQL queries where possible
- Avoid sending unnecessary data

These practices help protect your application.
---

## 📝 Summary Checklist

Your web server must:

```checklist
- [ ] Use Node.js  and Express
- [ ] Serve HTML, CSS, and JavaScript files
- [ ] Connect to a SQLite database
- [ ] Provide routes that return JSON
- [ ] Handle errors safely
- [ ] Support your PWA’s functionality
```
