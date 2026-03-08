# 🖨️ PrintLab — CAD & 3D Print Documentation Hub

<p align="center">
  <img src="https://img.shields.io/badge/Project-PrintLab-117A65?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-CAD%20%2F%203D%20Printing-2E86C1?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Based%20On-Real%20Industrial%20Work-E67E22?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/JSON-Data%20Layer-117A65?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Complete-2ECC71?style=flat-square" />
</p>

<p align="center">
  <em>"Physical and digital skills are not separate disciplines. This project is the proof."</em>
</p>

---

## 📌 About This Project

PrintLab is a **CAD and 3D print project documentation hub** powered by a JSON data layer — a lightweight, no-backend CMS concept that renders project cards, filter systems, and specs dynamically from structured data.

This is not a hobby project dressed up as portfolio work. **Every project documented in PrintLab is real.** The machine parts, the tolerances, the material choices, and the iteration logs all come from live industrial work carried out at **Ampoly Plastics in 2025**, where I designed and tested functional replacement parts and custom tooling on a working factory floor.

The technical concept behind PrintLab — a **JSON-driven CMS with no backend** — is the real development story here. It demonstrates that you don't need a database or a server to build a scalable, filterable, data-driven application.

---

## 🏭 Industrial Context — Ampoly Plastics, 2025

At Ampoly Plastics, I applied CAD design and 3D printing to solve real operational challenges:

| Challenge | Solution |
|---|---|
| Replacement part needed urgently | Designed to OEM spec in CAD, printed in PETG same day |
| Custom tooling required for new process | Modelled fixture from scratch, iterated twice before fit was correct |
| Cable management on production floor | Designed clip system, printed in PLA, deployed across 6 workstations |
| Safety guard bracket worn out | Reverse-engineered from original, printed as direct replacement |

> This is what hands-on development looks like. Not just writing code — using every tool available to solve real problems.

---

## ✨ Features

- **JSON-powered project cards** — all project data lives in a structured JSON array, rendered dynamically
- **Filter system** — filter by category (Functional, Decorative, Industrial, Prototype) with no page reload
- **Search** — live search across project names and descriptions
- **Spec display** — material, print time, layer height, and status per project
- **Status badges** — Complete / Testing / In Progress, colour-coded
- **Zero backend** — no server, no database, no build step

---

## 🗂️ The JSON Data Layer

The entire project archive lives in a single JavaScript data structure. Adding a new project means adding one object:

```javascript
const projects = [
  {
    id: "cable-organiser-v2",
    name: "Cable Organiser v2",
    category: "Functional",
    status: "Complete",
    material: "PLA",
    printTime: "4hr",
    layerHeight: "0.2mm",
    description: "Desktop cable management clip with revised snap-fit tab geometry. Improved retention force over v1 by ~40%.",
    tags: ["Industrial", "Functional", "Snap-fit"],
    date: "2025-02"
  },
  {
    id: "machine-guard-bracket",
    name: "Machine Guard Bracket",
    category: "Industrial",
    status: "In Use",
    material: "PETG",
    printTime: "8hr",
    layerHeight: "0.15mm",
    description: "Replacement safety guard bracket for Ampoly floor press. Matches OEM dimensions exactly.",
    tags: ["Industrial", "OEM-spec", "Replacement"],
    date: "2025-03"
  }
  // ... 12 more projects
];
```

---

## 💡 What I Learned

- Building a **JSON-driven CMS** — structuring data so it can be rendered, filtered, and searched without a backend
- Implementing **live filtering and search** using vanilla JavaScript array methods (`filter`, `includes`, `toLowerCase`)
- The real-world **CAD-to-print workflow** — tolerances, material selection, slicer settings, and why iteration is the process
- How **PETG differs from PLA** — heat resistance, flexibility, layer adhesion — and when to use each
- Why **documentation is part of the work** — a part with no record of how it was made is a liability, not an asset

---

## 🧰 Materials Reference

| Material | Properties | Used For |
|---|---|---|
| PLA | Easy to print, rigid, biodegradable | General functional parts, decorative |
| PETG | Heat resistant, slightly flexible, strong | Industrial parts near heat sources |
| TPU | Flexible, rubber-like, impact resistant | Grips, gaskets, flexible components |

---

## 📂 Project Structure

```
printlab/
├── index.html              # Main application
├── data/
│   └── projects.json       # All project data
├── assets/
│   ├── printlab-preview.png
│   └── printlab-preview-2.png
└── README.md
```

---

## 🖥️ Screenshots

![PrintLab Preview](./assets/printlab-preview.png)

---

## 🔗 Related Projects

| Project | Description |
|---|---|
| [DesignKit](../designkit) | Brand generator — creative skills expressed in code |
| [DevPortfolio](../devportfolio) | Personal portfolio — showcases PrintLab alongside all other projects |
| [SecureForm](../secureform) | Cybersecurity demo — technical thinking applied to a different domain |

---

## 👩‍💻 About the Developer

**Tasneem Mahomed** — Full-Stack Developer · CAD Designer · 3D Print Practitioner · Johannesburg, South Africa

Built as part of the [Fine Tuned Logic](https://github.com/ftlcollective) portfolio — *Systems That Shape Your Life.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tasneemmahomed-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tasneemmahomed)
[![Email](https://img.shields.io/badge/Email-ftlcollectivejhb@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ftlcollectivejhb@gmail.com)

---

<p align="center">
  <b>Fine Tuned Logic</b> · <em>Systems That Shape Your Life</em><br/>
  Fashion &nbsp;•&nbsp; Health &nbsp;•&nbsp; Tech &nbsp;•&nbsp; Johannesburg
</p>
