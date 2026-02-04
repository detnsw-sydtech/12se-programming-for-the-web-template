# Appendix 1 – Progressive Web Application (PWA) Guide  
### Programming for the Web – Software Engineering Stage 6 (Year 12)

A **Progressive Web App (PWA)** is a web application that behaves like a native mobile or desktop app. PWAs can be installed, work offline, load quickly, and provide a smooth user experience.

This guide explains the key components you will implement in your project.

---

## 🌐 What Makes a Web App “Progressive”?

A PWA is built using standard web technologies (HTML, CSS, JavaScript) but includes extra features that allow it to behave like an app.

A PWA must be:

- **Progressive** – works for every user, regardless of browser  
- **Responsive** – adapts to different screen sizes  
- **Connectivity‑independent** – works offline or with poor internet  
- **App‑like** – feels like a native application  
- **Fresh** – updates automatically  
- **Safe** – served over HTTPS  
- **Discoverable** – identifiable as an app by search engines  
- **Installable** – can be added to a device’s home screen  

---

## 🧩 Core Components of a PWA

A PWA requires three main components:

### **1. Web App Manifest (`manifest.json`)**
A JSON file that tells the browser how your app should behave when installed.

It includes:

- App name and short name  
- App icons  
- Theme colour  
- Background colour  
- Display mode (e.g., fullscreen, standalone)  
- Start URL  

Example structure:

```json
{
  "name": "My Catalogue App",
  "short_name": "Catalogue",
  "start_url": "/index.html",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#000000",
  "icons": [
    {
      "src": "icons/icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    }
  ]
}
```

### **2. Service Worker**
A JavaScript file that runs in the background and enables:

- Offline support  
- Caching  
- Faster loading  
- Background tasks  

A service worker:

- Does **not** have access to the DOM  
- Must be served over **HTTPS**  
- Must be registered in your JavaScript code  

Basic registration example:

```javascript
if ("serviceWorker" in navigator) {
  navigator.serviceWorker.register("/service-worker.js");
}
```

### **3. HTTPS

PWAs require secure hosting.

In development, your local server (localhost) is considered secure enough for testing.
When deployed, your PWA must be served over **HTTPS** to:
- Protect user data
- Enable service workers
- Improve trust and security
---

## 📦 Caching and Offline Behaviour

Your service worker can:

- Cache HTML, CSS, JS, and image files
- Serve cached files when offline
- Update the cache when new versions are available

This allows your PWA to load even without internet access.




