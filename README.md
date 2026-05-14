<div align="center">

# 🚀 Workify

### Your Gateway to Jobs, Internships & Scholarships

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Responsive](https://img.shields.io/badge/Responsive-Design-4CAF50?style=for-the-badge&logo=google-chrome&logoColor=white)](https://github.com/mostafa00950/Web-Client-Project)

**Workify** is a modern, fully client-side web platform that centralizes job opportunities, internships, and scholarships — empowering users to explore and apply, while giving admins complete control over posted listings.

[Features](#-features) · [Demo](#-project-structure) · [Tech Stack](#%EF%B8%8F-tech-stack) · [Getting Started](#-getting-started) · [Usage](#-usage)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#%EF%B8%8F-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [JavaScript Concepts](#-javascript-concepts-used)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌟 Overview

Workify solves a real problem: opportunity discovery is scattered across the web. This platform brings **jobs**, **internships**, and **scholarships** under one roof with a smooth, dynamic experience — no backend, no page reloads, no clutter.

Built entirely with vanilla HTML, CSS, and ES6 JavaScript, Workify demonstrates what modern front-end development can accomplish using native browser APIs and thoughtful architecture.

---

## ✨ Features

### 🔐 User Authentication
- **Registration** — Create a new account with form validation
- **Login** — Secure login with session persistence via cookies
- **Admin Detection** — Separate admin access flow with elevated privileges
- **Logout** — Clean session termination and state reset

### 🛠️ Admin Dashboard
Admins have full CRUD control over all listings:

| Action | Jobs | Scholarships / Internships |
|--------|------|---------------------------|
| ➕ Add | ✅ | ✅ |
| ✏️ Update | ✅ | ✅ |
| 🗑️ Delete | ✅ | ✅ |

### 💼 Jobs System
- Browse all available job listings
- **Live search** — Results update as you type
- **Filter by Location** — Target jobs in your area
- **Filter by Job Type** — Full-time, part-time, remote, etc.

### 🎓 Scholarships & Internships
- Browse all available opportunities
- **Filter by Funding** — Paid or unpaid
- **Filter by Location** — Find local or international opportunities

### ⚡ Live Search
Zero-reload search powered by native DOM events and JavaScript's `filter()` method — fast, smooth, and instant.

### 🎨 Dynamic UI
The interface reacts in real time to every user action:
- Live counters for listings and applications
- Inline success and error messages
- Welcome popup on login (powered by cookies)
- All updates happen without a single page refresh

### 💾 Data Persistence
| Data | Storage Method |
|------|---------------|
| Jobs & Scholarships | `localStorage` |
| Applications | `localStorage` |
| Contact Messages | `localStorage` |
| Login State | `localStorage` |
| Username & Welcome Popup | Cookies |

### 📬 Contact Form
Users can send messages directly through the platform. All messages are stored in `localStorage` for admin review.

### 📱 Responsive Design
Fully responsive layout that adapts seamlessly across:
- 🖥️ Desktop
- 📱 Tablet
- 📲 Mobile

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic structure and page markup |
| **CSS3** | Styling, animations, and responsive layout |
| **JavaScript (ES6+)** | Application logic, DOM manipulation, data management |
| **localStorage** | Client-side data persistence |
| **Cookies** | Session and preference storage |

> No frameworks. No libraries. No build tools. Pure web standards.

---

## 📁 Project Structure

```
WORKIFY/
│
├── public/
│   ├── css/
│   │   └── styles.css          # Global styles & responsive design
│   │
│   ├── images/                 # Static assets and icons
│   │
│   └── js/
│       ├── data.js             # ES6 classes & data models (User, Job, Internship, Application)
│       ├── script.js           # Core app logic, DOM rendering, search & filters
│       ├── login.js            # Login flow, cookie handling, admin detection
│       └── register.js         # Registration logic & validation
│
├── index.html                  # Home / landing page
├── jobs.html                   # Jobs listing & search page
├── scholarship.html            # Scholarships & internships page
├── admin.html                  # Admin dashboard (protected)
├── login.html                  # User login page
└── register.html               # User registration page
```

---

## 🚀 Getting Started

No installation required. Workify is a pure front-end project.

### Prerequisites
- Any modern web browser (Chrome, Firefox, Edge, Safari)
- A local server (optional but recommended)

### Running Locally

**Option 1 — Direct open (simplest)**
```bash
# Clone the repository
git clone https://github.com/mostafa00950/Web-Client-Project.git

# Navigate into the project
cd Web-Client-Project

# Open index.html in your browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

**Option 2 — Using VS Code Live Server (recommended)**
1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code
2. Right-click `index.html` → **Open with Live Server**

**Option 3 — Using Python's built-in server**
```bash
# Python 3
python -m http.server 8080

# Then open: http://localhost:8080
```

---

## 📖 Usage

### As a Regular User
1. **Register** an account on the Register page
2. **Log in** with your credentials
3. Browse **Jobs** or **Scholarships** using the navigation
4. Use the **search bar** and **filters** to narrow results
5. **Apply** for opportunities directly through the platform
6. Use the **Contact** form to send messages

### As an Admin
1. Log in with admin credentials
2. You'll be redirected to the **Admin Dashboard**
3. From the dashboard you can:
   - Add new job listings or scholarships
   - Edit any existing listing
   - Delete outdated or filled positions
   - Monitor all submitted applications

> ℹ️ Admin accounts are detected automatically based on credentials defined in `data.js`.

---

## 🧠 JavaScript Concepts Used

### ES6 Classes
Structured data models for clean, reusable code:
```javascript
class User { ... }
class Job { ... }
class Internship { ... }
class Application { ... }
```

### Array Methods
```javascript
// Adding new items
jobs.push(newJob);

// Filtering results
const results = jobs.filter(job => job.location === selectedLocation);

// Finding a specific item
const job = jobs.find(j => j.id === targetId);

// Finding index for updates/deletes
const index = jobs.findIndex(j => j.id === targetId);

// Rendering all items
jobs.forEach(job => renderJobCard(job));
```

### DOM Manipulation
```javascript
const card = document.createElement('div');
card.innerHTML = `<h3>${job.title}</h3>`;
container.appendChild(card);
element.textContent = updatedCount;
```

### Event Listeners
```javascript
searchInput.addEventListener('input', handleLiveSearch);
filterSelect.addEventListener('change', applyFilters);
form.addEventListener('submit', handleSubmit);
deleteBtn.addEventListener('click', handleDelete);
```

### Error Handling
```javascript
try {
  const data = JSON.parse(localStorage.getItem('jobs'));
  // ...
} catch (error) {
  console.error('Failed to load data:', error);
}
```

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. **Fork** the repository
2. **Create** a feature branch
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Commit** your changes
   ```bash
   git commit -m "feat: add your feature description"
   ```
4. **Push** to your branch
   ```bash
   git push origin feature/your-feature-name
   ```
5. **Open** a Pull Request

Please make sure your code follows the existing style and is well-commented.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">


⭐ If you found this project helpful, please consider giving it a star!

</div>
