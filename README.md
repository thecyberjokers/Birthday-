<div align="center">

# 🎁 Secret Birthday Gift

**A Shinchan-themed, interactive birthday surprise — a midnight countdown, a secret passcode, floating gift boxes, a cake to blow out, a photo clothesline and a typewriter love letter. Pure HTML, CSS and vanilla JavaScript.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)
![Responsive](https://img.shields.io/badge/Responsive-Mobile%20%7C%20Desktop-ff69b4?style=for-the-badge)

[Features](#-features) • [Quick Start](#-quick-start) • [Customize](#%EF%B8%8F-customize-it) • [Single-File Build](#-single-file-version) • [Structure](#-project-structure) • [Disclaimer](#%EF%B8%8F-disclaimer) • [Credits](#-credits--license)

</div>

---

## ✨ Features

| Step | What happens |
| :--- | :--- |
| 🕛 **Midnight countdown** | An analog + digital stage clock counts down to `12:00:00 AM`, then velvet curtains open with a light burst. |
| 🔐 **Secret passcode** | A 4-digit PIN screen with a phone-style dial pad and full keyboard support. Wrong code? Shinchan reacts and the card shakes. Default passcode: **`2026`**. |
| 💖 **Teaser** | Curved animated headings and a "Do you wanna see it?" YES / NO moment (NO makes Shinchan plead 🥺). |
| 🎁 **3 gift boxes** | 📸 hanging Polaroid **memories clothesline** · 🎂 **birthday cake** with 7 candles to blow out + confetti · 💌 **typewriter love letter** with a 3D Polaroid. |
| 🎵 **Background music** | A built-in music-box "Happy Birthday" (generated live with the Web Audio API) **or your own song**. Floating 🎵 button to mute / unmute. |
| 📱 **Responsive** | Works on phones, tablets and desktops. No frameworks, no build step. |

> 🔒 **Note:** the passcode is a *fun gate*, not real security — it lives in the client-side JavaScript, so anyone who views the source can read it.

---

## 🚀 Quick Start

```bash
git clone https://github.com/rc8447327-jpg/Secret-Birthday-Gift.git
cd Secret-Birthday-Gift
```

Then simply **double-click `index.html`**, or serve it locally:

```bash
python3 -m http.server 8000      # open http://localhost:8000
```

> The countdown starts on load. Browsers block autoplay audio, so the music starts on your **first tap / key press** (e.g. the first passcode digit).

### 🌐 Deploy for free

- **GitHub Pages:** *Settings → Pages → Deploy from branch → `main` / root → Save.*
- **Vercel / Netlify:** drag-and-drop the folder (or just the [single-file build](#-single-file-version)). `vercel.json` is already included.

---

## ⚙️ Customize It

### 1. Change the passcode
`script.js`:
```js
const TARGET_PASSCODE = "2026"; // any 4 digits — a birth year, a date like 1408, etc.
```

### 2. Replace the photos
Swap the files in `assets/` (keep the same names): `memory1.jpg` … `memory5.jpg`.
Square images (1:1, ~1024 px) look best.

### 3. Write your own letter
`script.js` → edit the `LETTER_SECTIONS` array (headline, two paragraphs, closing line).

### 4. Add your own song 🎶
Put your track at **`assets/song.mp3`** — it loops automatically. If the file is missing, the built-in music-box tune plays instead.
*(Only use music you have the right to use.)*

---

## 📦 Single-File Version

Want to share it as **one file**? A single `index.html` can contain everything — CSS, JS, all images/GIFs (as base64) and the music code — so you can upload just that one file anywhere.

- Add your own song there by setting `const BIRTHDAY_SONG = "https://…/song.mp3";` near the top of the script.
- Google Fonts are still loaded online; offline, the browser falls back to default fonts.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `0`–`9` | Type the passcode |
| `Backspace` | Delete last digit |
| `Enter` | Submit passcode / blow out all candles |
| `Space` | Blow out candles / scroll memories right |
| `←` `→` | Scroll the photo clothesline |
| `Esc` | Close any open modal |

---

## 📂 Project Structure

```text
Secret-Birthday-Gift/
├── assets/                 # photos, Shinchan GIFs/PNGs (and optional song.mp3)
├── index.html              # markup
├── style.css               # design system & animations
├── script.js               # passcode, gifts, cake, letter, countdown
├── music.js                # background music (own song or built-in music box)
├── vercel.json             # Vercel config (clean URLs)
├── LICENSE                 # MIT
└── README.md
```

---

## 🛠️ Tech Stack

**HTML5** (semantic markup, inline SVG) · **CSS3** (keyframes, glassmorphism, grid/flex, media queries) · **Vanilla JS (ES6+)** (DOM, particle effects, Web Audio API)

---

## ⚠️ Disclaimer

This is a **personal, non-commercial, fan-made project** made for fun and learning.

- **Characters & media:** Shinchan / *Crayon Shin-chan* and any other characters, GIFs or images belong to their respective copyright and trademark owners. No ownership or affiliation is claimed.
- **Photos & music:** only upload photos of people who have agreed to it, and only use music you are allowed to use. Don't publish someone's private photos without their consent — keep the repo private or swap in placeholders before making it public.
- **Passcode:** it is client-side only and provides no real security.
- The software is provided **"as is"**, without warranty of any kind.

---

## 🙌 Credits & License

- Built on the open-source **[Secret-Birthday-Gift](https://github.com/saklincodes/Secret-Birthday-Gift)** template by **[@saklincodes](https://github.com/saklincodes)** (MIT).
- Customized and extended (passcode fix, background music, single-file build) by **[@rc8447327-jpg](https://github.com/rc8447327-jpg)** — *TheCyberJokers*.

Licensed under the **[MIT License](LICENSE)**. Please keep the original copyright notice in `LICENSE` when you reuse or fork this project.

<div align="center">

Made with 💖 for someone special · ⭐ star the repo if it made you smile

</div>
