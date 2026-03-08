# 💙 MindBridge — Mental Health Awareness Platform

<p align="center">
  <img src="https://img.shields.io/badge/Project-MindBridge-2E86C1?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Mental%20Health-8E44AD?style=for-the-badge" />
  <img src="https://img.shields.io/badge/API-Integration-F39C12?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Public%20API-Integrated-2ECC71?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Complete-2ECC71?style=flat-square" />
</p>

<p align="center">
  <em>"Mental health tools are often cold and clinical. This one isn't."</em>
</p>

---

## 📌 About This Project

MindBridge is a **responsive mental health awareness platform** with daily mood tracking, guided journaling, and curated support resources — built with empathy, not algorithms.

This is my **first full API integration project**, demonstrating how external data sources can be wired into a meaningful, human-centred user interface. The API pulls daily mental health resources and helpline information, surfacing the most relevant content based on the user's mood check-in.

The core design principle: **warmth over clinical efficiency.** Most health apps feel like dashboards. MindBridge feels like a conversation.

---

## ✨ Features

- **Daily mood tracker** — six mood states, one-tap check-in, zero friction
- **Mood history chart** — browser-stored weekly overview, visualised with vanilla JS
- **Guided journaling** — daily prompts that change to encourage honest reflection
- **API-powered resources** — curated helplines, articles, and exercises loaded dynamically
- **Local storage only** — journal entries and mood data stay in the user's browser, never on a server
- **Fully responsive** — designed mobile-first, works on any screen size

---

## 🔌 API Integration

This project marks my first hands-on work with external APIs — a core milestone in my full-stack development journey.

```javascript
// Fetching daily mental health resource via public API
async function loadTodaysResource() {
  const response = await fetch('https://api.mentalhealthresources.io/daily');
  const data = await response.json();
  renderResource(data);
}
```

| Integration | Purpose |
|---|---|
| Mental Health Resource API | Pulls daily helplines, exercises, and reading |
| Browser LocalStorage API | Stores mood logs and journal entries client-side |
| Date API | Personalises daily prompts and greetings |

---

## 💡 What I Learned

- How to **fetch and parse JSON** from a public API using async/await
- **Error handling** — what happens when an API is unavailable, and how to fail gracefully
- Using **localStorage** to create a persistent user experience without a backend
- Designing for **emotional tone** — colour, language, and pacing all affect how a tool feels to use
- Building a **mood visualisation** from scratch using pure JavaScript and DOM manipulation

---

## 📂 Project Structure

```
mindbridge/
├── index.html              # Main application
├── assets/
│   ├── mindbridge-preview.png
│   └── mindbridge-preview-2.png
└── README.md
```

---

## 🖥️ Screenshots

![MindBridge Preview](./assets/mindbridge-preview.png)

---

## 🧠 Mental Health Resources Included

| Resource | Contact | Type |
|---|---|---|
| Samaritans SA | 0800 567 567 | Crisis line · 24/7 |
| SADAG Helpline | 0800 456 789 | Depression & anxiety |
| Lifeline SA | 0861 322 322 | General crisis |
| 5-Minute Grounding | In-app | Guided exercise |
| Burnout Guide | In-app | Reading resource |

---

## 🔗 Related Projects

| Project | Description |
|---|---|
| [SafeReport](../safereport) | Anonymous GBV reporting platform — privacy-first |
| [SecureForm](../secureform) | Cybersecurity demo — XSS prevention |
| [DevPortfolio](../devportfolio) | Personal developer portfolio |

---

## 👩‍💻 About the Developer

**Tasneem Mahomed** — Full-Stack Developer · Mental Health Advocate · Johannesburg, South Africa

Built as part of the [Fine Tuned Logic](https://github.com/ftlcollective) portfolio — *Systems That Shape Your Life.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tasneemmahomed-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tasneemmahomed)
[![Email](https://img.shields.io/badge/Email-ftlcollectivejhb@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ftlcollectivejhb@gmail.com)

---

<p align="center">
  <b>Fine Tuned Logic</b> · <em>Systems That Shape Your Life</em><br/>
  Fashion &nbsp;•&nbsp; Health &nbsp;•&nbsp; Tech &nbsp;•&nbsp; Johannesburg
</p>
