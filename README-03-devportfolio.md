# 🌐 DevPortfolio — Personal Developer Portfolio

<p align="center">
  <img src="https://img.shields.io/badge/Project-DevPortfolio-1a1a2e?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Type-Personal%20Portfolio-6C3483?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Frameworks-Zero-2ECC71?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Responsive-Mobile%20First-2E86C1?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Complete-2ECC71?style=flat-square" />
</p>

<p align="center">
  <em>"Proving frontend fundamentals before reaching for a framework."</em>
</p>

---

## 📌 About This Project

DevPortfolio is my **personal developer portfolio** — built entirely from scratch using pure HTML, CSS, and vanilla JavaScript. No React. No frameworks. No libraries.

This was a deliberate choice. Before reaching for tools that abstract away the fundamentals, I wanted to prove that I understand what those tools are abstracting. Every layout, animation, and interaction in this project was written by hand.

The portfolio showcases my projects, skills, background, and advocacy work — and serves as the central hub for my presence as an emerging full-stack developer.

---

## 🎯 Why No Framework?

| With Framework | Without Framework |
|---|---|
| Component abstraction | Manual DOM management |
| State management built-in | Vanilla JS state handling |
| Pre-built routing | Custom scroll & navigation |
| Faster to build | Deeper understanding of what's happening |

> The goal was not speed — it was **understanding.** A developer who knows why React exists writes better React.

---

## ✨ Features

- **Fully responsive** — mobile-first layout, tested across all screen sizes
- **Dark mode toggle** — preference stored in localStorage, persists across sessions
- **Smooth scroll navigation** — custom JS, no libraries
- **Skill bars** — animated on scroll using Intersection Observer API
- **Project cards** — dynamically rendered from a JavaScript data array
- **Contact form** — client-side validated, no backend dependency
- **Zero dependencies** — no npm, no node_modules, no build step needed

---

## 💡 What I Learned

- The **CSS Grid and Flexbox** systems deeply — building complex layouts without Bootstrap
- How the **Intersection Observer API** works — triggering animations when elements enter the viewport
- **localStorage** for persisting user preferences (dark/light mode)
- Writing **semantic, accessible HTML** — proper heading hierarchy, ARIA labels, landmark elements
- How to structure a **pure JS project** without a module bundler — script organisation and dependency order
- Why **mobile-first CSS** produces cleaner, more maintainable stylesheets than desktop-first

---

## 📂 Project Structure

```
devportfolio/
├── index.html              # Full single-page application
├── assets/
│   ├── devportfolio-preview.png
│   └── devportfolio-preview-2.png
└── README.md
```

---

## 🖥️ Screenshots

![DevPortfolio Preview](./assets/devportfolio-preview.png)

---

## 🛠️ Technical Highlights

```javascript
// Skill bars — animate on scroll using Intersection Observer
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.style.width = entry.target.dataset.width;
    }
  });
});

document.querySelectorAll('.skill-fill').forEach(bar => {
  observer.observe(bar);
});
```

```javascript
// Dark mode toggle — persists via localStorage
function toggleTheme() {
  const current = localStorage.getItem('theme') || 'dark';
  const next = current === 'dark' ? 'light' : 'dark';
  document.body.setAttribute('data-theme', next);
  localStorage.setItem('theme', next);
}
```

---

## 🔗 Related Projects

| Project | Description |
|---|---|
| [SafeReport](../safereport) | Anonymous GBV reporting platform |
| [MindBridge](../mindbridge) | Mental health platform with API integration |
| [DesignKit](../designkit) | Fashion × Tech brand identity generator |
| [SecureForm](../secureform) | Cybersecurity-aware form with XSS prevention |
| [PrintLab](../printlab) | CAD and 3D print documentation hub |

---

## 👩‍💻 About the Developer

**Tasneem Mahomed** — Full-Stack Developer · Cybersecurity Learner · Johannesburg, South Africa

Built as part of the [Fine Tuned Logic](https://github.com/ftlcollective) portfolio — *Systems That Shape Your Life.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tasneemmahomed-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tasneemmahomed)
[![Email](https://img.shields.io/badge/Email-ftlcollectivejhb@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ftlcollectivejhb@gmail.com)

---

<p align="center">
  <b>Fine Tuned Logic</b> · <em>Systems That Shape Your Life</em><br/>
  Fashion &nbsp;•&nbsp; Health &nbsp;•&nbsp; Tech &nbsp;•&nbsp; Johannesburg
</p>
