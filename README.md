# 🌿 N&H Landscaping — Official Website

> Professional landscaping website for **N&H Landscaping**, a Hobart-based landscaping business serving the greater Tasmania area. Built with pure HTML, CSS and JavaScript — no frameworks, no dependencies, fast and lightweight.

---

## 🖥️ Live Site

**[https://nh-landscaping.vercel.app](https://nh-landscaping.vercel.app)**

---

## 📸 About

This is the official business website for N&H Landscaping, a local Hobart company specialising in:

- 💧 Drainage Solutions
- 🚜 Excavation & Earth Removal
- 🧱 Retaining Walls
- ⬜ Paving
- 🌱 Artificial Lawn Supply & Installation
- 🏡 Full Yard Makeovers

The design is inspired by the natural colours and landscapes of Tasmania — dolerite rock, Huon pine timber, Cradle Mountain mist, Southern Ocean teal and ancient rainforest green.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 / CSS3 / Vanilla JS | Core site — no frameworks |
| [EmailJS](https://www.emailjs.com) | Quote form → email delivery (no backend needed) |
| [Google reCAPTCHA v3](https://www.google.com/recaptcha) | Invisible bot protection on quote form |
| [Vercel](https://vercel.com) | Hosting & deployment |
| [Google Fonts](https://fonts.google.com) | Cormorant Garamond + Nunito Sans |

---

## ✨ Features

- **Tasmanian-themed design** — custom colour palette, mountain silhouette SVG, Tasmania map shape
- **Animated hero** — layered mist effects, floating particles, staggered text reveal
- **Custom cursor** — amber dot with trailing ring
- **Scroll reveal animations** — left, right and upward with stagger delays
- **Counter animation** — stats roll up when scrolled into view
- **Secure quote form** with 4-layer protection:
  - 🍯 Honeypot field (silent bot trap)
  - 🤖 Google reCAPTCHA v3 (invisible scoring)
  - ⏱️ Rate limiting (max 3 submissions per 10 minutes)
  - 🧹 Input sanitisation (strips malicious characters)
- **EmailJS integration** — quote form sends directly to business email, triggering a mobile push notification
- **Fully responsive** — works on all screen sizes
- **Zero backend** — 100% static, no server required

---

## 📁 Project Structure

```
nh-landscaping/
  └── index.html        # Entire site — HTML, CSS and JS in one file
  └── README.md         # This file
```

---

## 🚀 Deployment (Vercel)

This site is deployed on Vercel. To deploy your own copy:

**1. Install Vercel CLI**
```bash
npm install -g vercel
```

**2. Login**
```bash
vercel login
```

**3. Deploy**
```bash
cd nh-landscaping
vercel
```

**4. Redeploy after changes**
```bash
vercel --prod
```

For a custom domain, go to your Vercel project → **Settings → Domains** and add your domain. Vercel handles HTTPS automatically.

---

## ⚙️ Configuration

Before deploying, replace the placeholder values in `index.html` with your real keys.

### EmailJS Setup

1. Sign up at [emailjs.com](https://www.emailjs.com) (free)
2. Add an **Email Service** (connect Gmail or any email)
3. Create an **Email Template** using these variables:

```
Subject:  New Quote Request from {{from_name}}

Name:     {{from_name}}
Email:    {{from_email}}
Phone:    {{phone}}
Suburb:   {{suburb}}
Service:  {{service}}

Message:
{{message}}
```

4. Go to **Account → General** to get your Public Key
5. Replace in `index.html`:

```javascript
emailjs.init({ publicKey: "YOUR_EMAILJS_PUBLIC_KEY" });
const SVC = "YOUR_SERVICE_ID";
const TPL = "YOUR_TEMPLATE_ID";
```

---

### Google reCAPTCHA v3 Setup

1. Go to [google.com/recaptcha](https://www.google.com/recaptcha)
2. Register a new site:
   - **Type:** reCAPTCHA v3
   - **Domains:** your Vercel URL + custom domain
3. Copy the **Site Key**
4. Replace in `index.html` in **two places**:

```html
<!-- In the <head> script tag -->
<script src="https://www.google.com/recaptcha/api.js?render=YOUR_RECAPTCHA_SITE_KEY">

<!-- In the JavaScript section -->
const RCKEY = "YOUR_RECAPTCHA_SITE_KEY";
```

---

## 🔒 Security Features

| Layer | Method | Description |
|---|---|---|
| 1 | Honeypot field | Hidden input bots fill in — silently rejected if filled |
| 2 | reCAPTCHA v3 | Invisible background scoring — no user interaction needed |
| 3 | Rate limiting | Max 3 submissions per 10 minutes per device |
| 4 | Input sanitisation | Strips `< > " ' \`` characters from all fields |

---

## 🎨 Colour Palette

| Name | Hex | Inspired By |
|---|---|---|
| Dolerite | `#1c2026` | Tasmanian dolerite rock formations |
| Deep Forest | `#141d16` | Ancient Tasmanian rainforest |
| Huon Pine | `#b8762e` | Huon pine timber (endemic to Tasmania) |
| Huon Light | `#d4954a` | Huon pine heartwood glow |
| Southern Ocean | `#1a5c6e` | Southern Ocean deep teal |
| Cradle Mist | `#7fa8b8` | Cradle Mountain morning mist |
| Button Grass | `#3d5c2a` | Button grass plains |
| Leatherwood | `#ede8dc` | Leatherwood flower cream |

---

## 📞 Business Contact

**N&H Landscaping**
📍 Hobart, Tasmania, Australia
📞 +61 XXX XXX XXX
📧 info@nhlandscaping.com.au

---

## 📄 License

This project is proprietary. All rights reserved © 2025 N&H Landscaping.
Not for redistribution or reuse without written permission.

---

*Built with ❤️ for Tasmania*
