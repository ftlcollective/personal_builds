# 🔐 SecureForm — Cybersecurity-Aware Input Validation

<p align="center">
  <img src="https://img.shields.io/badge/Project-SecureForm-2C3E50?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Cybersecurity-E74C3C?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Learning-In%20Public-117A65?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/XSS-Prevention-E74C3C?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Complete-2ECC71?style=flat-square" />
</p>

<p align="center">
  <em>"Security isn't a feature you add at the end. It's a mindset you build with from the start."</em>
</p>

---

## 📌 About This Project

SecureForm is a **documented demonstration of secure web form design** — built while actively studying cybersecurity fundamentals.

Every line of code is annotated with inline commentary explaining the **security reasoning** behind each decision. This is not just a form with validation — it is a walkthrough of how to think about user input as an attack vector, and how to defend against it at every layer.

This project exists to prove one thing: **I don't just study cybersecurity theory — I apply it in code.**

---

## 🛡️ Security Concepts Demonstrated

### 1. Cross-Site Scripting (XSS) Prevention

XSS attacks inject malicious scripts into web pages via user input. When another user views the page, the script executes — potentially stealing session data, cookies, or credentials.

```javascript
// Strip script injection attempts before processing
function sanitise(input) {
  return input
    .replace(/<script[\s\S]*?>[\s\S]*?<\/script>/gi, '')
    .replace(/<[^>]+on\w+\s*=/gi, '')      // inline event handlers
    .replace(/javascript:/gi, '')           // javascript: protocol
    .replace(/data:/gi, '');                // data: URI attacks
}
```

### 2. Input Validation

After sanitisation, fields are validated for correct structure — confirming format matches expectations even after attack patterns have been stripped.

```javascript
function validateEmail(value) {
  const clean = sanitise(value);
  const pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return { clean, valid: pattern.test(clean) };
}
```

### 3. Output Encoding

Any user-supplied data displayed back to the browser is HTML-encoded before rendering — even after sanitisation.

```javascript
function encodeForHTML(str) {
  return str
    .replace(/&/g, '&amp;')
    .replace(/</g, '&lt;')
    .replace(/>/g, '&gt;')
    .replace(/"/g, '&quot;');
}
```

---

## ✨ Features

- **Live XSS detection** — malicious patterns flagged and stripped in real time as the user types
- **Annotated source code** — every function includes inline commentary explaining the security decision
- **Console output panel** — shows exactly what the sanitiser is doing at each step
- **Three-layer defence** — sanitise → validate → encode on output
- **Graceful failure** — form is blocked cleanly when validation fails, with clear user feedback

---

## 🧱 Defence in Depth

| Layer | What It Does | Why It Matters |
|---|---|---|
| **Sanitise** | Strips script tags, event handlers, dangerous protocols | Removes raw attack vectors at the point of entry |
| **Validate** | Checks field structure after sanitisation | Catches malformed input that survived sanitisation |
| **Encode** | HTML-encodes all output before rendering | Prevents browser interpreting data as executable code |

> Never trust a single layer. Each one is designed to catch what the others miss.

---

## 💡 What I Learned

- The mechanics of **XSS attacks** — how they work, what they target, and why they're so common
- Writing **defence-in-depth security** — multiple independent layers, not a single check
- The difference between **sanitisation and validation** — both are needed, neither replaces the other
- How to **communicate security decisions** through code comments — important for team environments
- Why **output encoding** matters even when input has already been sanitised

---

## 📂 Project Structure

```
secureform/
├── index.html              # Full annotated application
├── assets/
│   ├── secureform-preview.png
│   └── secureform-preview-2.png
└── README.md
```

---

## 🖥️ Screenshots

![SecureForm Preview](./assets/secureform-preview.png)

---

## 🔗 Related Projects

| Project | Description |
|---|---|
| [SafeReport](../safereport) | Privacy-first GBV platform — security applied to social impact |
| [MindBridge](../mindbridge) | Mental health platform with API integration |
| [DevPortfolio](../devportfolio) | Personal developer portfolio — zero frameworks |

---

## 👩‍💻 About the Developer

**Tasneem Mahomed** — Full-Stack Developer · Cybersecurity Student · Johannesburg, South Africa

Currently studying cybersecurity foundations with a formal certification starting soon. Building in public — applying what I learn to real projects as I learn it.

Built as part of the [Fine Tuned Logic](https://github.com/ftlcollective) portfolio — *Systems That Shape Your Life.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tasneemmahomed-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tasneemmahomed)
[![Email](https://img.shields.io/badge/Email-ftlcollectivejhb@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ftlcollectivejhb@gmail.com)

---

<p align="center">
  <b>Fine Tuned Logic</b> · <em>Systems That Shape Your Life</em><br/>
  Fashion &nbsp;•&nbsp; Health &nbsp;•&nbsp; Tech &nbsp;•&nbsp; Johannesburg
</p>
