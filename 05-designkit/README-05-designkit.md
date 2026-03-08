# 🎨 DesignKit — Fashion × Tech Brand Identity Generator

<p align="center">
  <img src="https://img.shields.io/badge/Project-DesignKit-8E44AD?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Fashion%20×%20Tech-E91E63?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Canvas-API-F39C12?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/Canvas-API-8E44AD?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Complete-2ECC71?style=flat-square" />
</p>

<p align="center">
  <em>"Where fashion design instinct meets frontend development — creative logic expressed in code."</em>
</p>

---

## 📌 About This Project

DesignKit is a **creative brand identity generator** built at the intersection of fashion design training and full-stack development. It generates cohesive colour palettes, typography pairings, and visual brand previews — all powered by the HTML5 Canvas API and vanilla JavaScript.

This project is personal. My background includes formal fashion design training and a graphic design award from the Department of Education. DesignKit is the project where those skills meet code — where I stop being a developer who used to design, and become a developer who codes their design instincts.

---

## ✨ Features

- **Colour palette generator** — applies colour theory principles (complementary, analogous, triadic) to produce harmonious palettes, not random ones
- **Typography pairing system** — curated combinations of display serif, body sans, and mono label fonts — the three-font system used by professional brand designers
- **Live Canvas API preview** — brand identity rendered visually in real time using HTML5 Canvas
- **Export options** — download as PDF, CSS variables file, or JSON design token set
- **Mood-based generation** — input a brand mood (minimal, earthy, editorial, bold) and the algorithm adjusts the output accordingly

---

## 🎨 The Design System Behind It

DesignKit doesn't pick colours at random. It uses applied colour theory:

| Mood | Colour Strategy | Typical Output |
|---|---|---|
| Deep & Minimal | Monochromatic scale | Near-black → warm white |
| Warm & Earthy | Analogous warm tones | Burnt sienna → cream |
| Soft & Dreamy | Low-saturation pastels | Muted lilac → ivory |
| Bold & Editorial | High-contrast split-complementary | Deep navy + vivid accent |

### Typography Logic

```javascript
const typePairings = {
  editorial: {
    display: 'Cormorant Garamond',   // emotion, elegance
    body: 'IBM Plex Sans',           // readability, trust
    mono: 'IBM Plex Mono'            // precision, detail
  },
  modern: {
    display: 'Syne',
    body: 'DM Sans',
    mono: 'Space Mono'
  }
};
```

---

## 💡 What I Learned

- Using the **HTML5 Canvas API** to render visual output — drawing shapes, text, and colour blocks programmatically
- Implementing **colour theory in JavaScript** — converting between HEX, HSL, and RGB to generate harmonious palettes algorithmically
- Building a **multi-format export system** — generating PDFs and CSS files dynamically from JavaScript
- How **design systems work technically** — design tokens, CSS custom properties, and why they matter
- Bridging **creative instinct and code logic** — the hardest skill to teach, and the most valuable one to have

---

## 🖥️ Screenshots

![DesignKit Preview](./assets/designkit-preview.png)

---

## 📂 Project Structure

```
designkit/
├── index.html              # Main application
├── assets/
│   ├── designkit-preview.png
│   └── designkit-preview-2.png
└── README.md
```

---

## 🛠️ Canvas API Highlight

```javascript
// Render colour palette to canvas
function drawPalette(ctx, colours) {
  const swatchWidth = ctx.canvas.width / colours.length;

  colours.forEach((hex, i) => {
    ctx.fillStyle = hex;
    ctx.fillRect(i * swatchWidth, 0, swatchWidth, 60);
  });
}

// Render typography specimen
function drawTypeSample(ctx, pairing) {
  ctx.font = `300 32px "${pairing.display}"`;
  ctx.fillStyle = '#1a1a1a';
  ctx.fillText('Brand Heading', 20, 100);

  ctx.font = `300 16px "${pairing.body}"`;
  ctx.fillStyle = '#666';
  ctx.fillText('Body copy — readable and refined', 20, 130);
}
```

---

## 🔗 Related Projects

| Project | Description |
|---|---|
| [DevPortfolio](../devportfolio) | Personal portfolio — demonstrates the same design sensibility in a full site |
| [PrintLab](../printlab) | CAD and 3D print docs — physical design meets digital documentation |
| [SafeReport](../safereport) | Privacy-first GBV platform — social impact through considered design |

---

## 👩‍💻 About the Developer

**Tasneem Mahomed** — Full-Stack Developer · Fashion Designer · Graphic Design Award Recipient · Johannesburg, South Africa

Built as part of the [Fine Tuned Logic](https://github.com/ftlcollective) portfolio — *Systems That Shape Your Life.*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-tasneemmahomed-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tasneemmahomed)
[![Email](https://img.shields.io/badge/Email-ftlcollectivejhb@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ftlcollectivejhb@gmail.com)

---

<p align="center">
  <b>Fine Tuned Logic</b> · <em>Systems That Shape Your Life</em><br/>
  Fashion &nbsp;•&nbsp; Health &nbsp;•&nbsp; Tech &nbsp;•&nbsp; Johannesburg
</p>
