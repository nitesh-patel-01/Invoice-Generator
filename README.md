# 🧾 InvoiceMaker Pro

> **Free online invoice generator for Indian freelancers & small businesses.**  
> Create professional GST-compliant invoices in seconds — no signup, no login, no watermarks.

🔗 **Live Demo:** [invoice-generator-neon-alpha.vercel.app](https://invoice-generator-neon-alpha.vercel.app/)

---

## ✨ Features

| Feature | Details |
|---|---|
| 📄 **PDF Download** | One-click high-quality PDF export via jsPDF + html2canvas |
| 🇮🇳 **GST Ready** | GSTIN, HSN/SAC codes, per-item tax % for GST-compliant invoices |
| 🖼️ **Logo Upload** | Upload business logo — processed 100% in-browser |
| 💱 **Multi-Currency** | INR, USD, EUR, GBP, AED, JPY, SGD |
| 📱 **Mobile Friendly** | Fully responsive on Android, iPhone, tablet, desktop |
| 🔒 **100% Private** | No server, no storage — all data stays in your browser |
| 🏷️ **Status Stamp** | Mark invoice as Paid / Unpaid / Overdue |
| 📋 **Copy as Text** | Copy full invoice as plain text for email/chat |
| ♾️ **Unlimited Items** | Add unlimited line items with individual tax & discount % |
| 🌙 **No Signup** | Zero registration — open and use instantly |

---

## 🚀 Getting Started

### Option 1 – Use Live (No Setup)
Simply visit [invoice-generator-neon-alpha.vercel.app](https://invoice-generator-neon-alpha.vercel.app/) in any browser.

### Option 2 – Run Locally
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/invoice-generator.git

# Navigate into folder
cd invoice-generator

# Open in browser (no build step needed)
open index.html
# OR on Windows:
start index.html
```
That's it. No npm install, no build process, no dependencies to install.

### Option 3 – Deploy to Vercel (1 click)
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/invoice-generator)

Or manually:
```bash
npm i -g vercel
vercel --prod
```

---

## 📁 Project Structure

```
invoice-generator/
│
├── index.html              # Main app — entire tool in one file
├── 404.html                # Custom 404 error page
├── sitemap.xml             # XML sitemap for Google Search Console
├── robots.txt              # Crawl instructions for search bots
├── vercel.json             # Vercel deployment config + security headers
├── og-image-preview.html   # Open Graph image template (1200×630)
└── README.md               # This file
```

---

## 🔧 Tech Stack

| Technology | Usage |
|---|---|
| **HTML5** | Single-file app structure |
| **CSS3** | Custom properties, Grid, Flexbox, responsive layout |
| **Vanilla JS** | Real-time preview, calculations, PDF generation |
| **jsPDF 2.5.1** | PDF generation engine |
| **html2canvas 1.4.1** | Invoice screenshot → PDF |
| **Google Fonts** | Playfair Display + DM Sans |
| **Font Awesome 6.5** | Icons |
| **Vercel** | Hosting & deployment |

> **Zero frameworks. Zero npm packages. Zero build step.**  
> Everything loads from CDN — the entire app is one HTML file.

---

## 📸 Screenshots

> *(Add screenshots of the invoice tool, preview, and PDF output here)*

---

## 🛠️ Customization Guide

### Change Business Defaults
Edit the `window.onload` function in `index.html`:
```js
window.onload = () => {
  document.getElementById('from_name').value = 'Your Default Business Name';
  document.getElementById('from_gstin').value = 'YOUR_GSTIN_HERE';
  // ...
};
```

### Change Brand Colors
Edit the `:root` CSS variables at the top of `index.html`:
```css
:root {
  --accent: #1a5cff;   /* Primary blue — change to your brand color */
  --gold: #c9a84c;     /* Gold accent */
  --ink: #0f1923;      /* Dark text/backgrounds */
}
```

### Add New Currency
In the `<select id="currency">` element, add:
```html
<option value="₹">₹ INR – Indian Rupee</option>
<!-- Add your currency: -->
<option value="CAD">CAD – Canadian Dollar</option>
```

### Change Contact Info
Search and replace in `index.html`:
- Phone: `7974823298` → your number
- Email: `niteshpatel7479@gmail.com` → your email
- Also update `sitemap.xml` with your actual domain

---

## 🔍 SEO Setup Checklist

After deploying to your domain:

- [ ] Update `canonical` URL in `<head>` of `index.html`
- [ ] Update all URLs in `sitemap.xml`
- [ ] Update `Sitemap:` line in `robots.txt`
- [ ] Generate `og-image.jpg` from `og-image-preview.html` and upload to root
- [ ] Submit `sitemap.xml` to [Google Search Console](https://search.google.com/search-console)
- [ ] Submit `sitemap.xml` to [Bing Webmaster Tools](https://www.bing.com/webmasters)
- [ ] Run [Google Rich Results Test](https://search.google.com/test/rich-results) to verify FAQ schema

---

## 🐛 Known Issues & Fixes

**Q: Google Search Console shows "Server connection error"**  
A: This is a Vercel deployment issue, not a code issue. Fix:
1. Go to your Vercel dashboard → Project Settings
2. Ensure `Root Directory` is set to the folder containing `index.html`
3. Run `vercel --prod` to force a fresh deployment
4. Wait 2-3 days after deployment for Google to re-crawl

**Q: PDF quality is blurry**  
A: The `scale: 2` option in html2canvas is already set for 2x resolution. For higher quality, increase to `scale: 3` in the `downloadPDF()` function (note: larger file size).

**Q: Logo not showing in PDF**  
A: Ensure the logo is uploaded fresh before downloading PDF. Logos are stored as base64 data URLs in memory — they reset on page refresh.

---

## 📞 Contact & Support

**Created by Nitesh Patel**

| Channel | Details |
|---|---|
| 📧 Email | [niteshpatel7479@gmail.com](mailto:niteshpatel7479@gmail.com) |
| 📞 Phone | [+91 79748 23298](tel:+917974823298) |
| 💬 WhatsApp | [Chat Now](https://wa.me/917974823298?text=Hi%2C%20I%20need%20help%20with%20InvoiceMaker%20Pro) |
| 🌐 Blog | [niteshpatelweb.blogspot.com](https://niteshpatelweb.blogspot.com) |

---

## 📄 License

This project is open source. Feel free to fork, modify, and use for personal or commercial projects.  
If you find it helpful, a ⭐ star on GitHub would be appreciated!

---

## 🙏 Acknowledgements

- [jsPDF](https://github.com/parallax/jsPDF) — PDF generation
- [html2canvas](https://html2canvas.hertzen.com/) — DOM to canvas rendering
- [Google Fonts](https://fonts.google.com/) — Playfair Display & DM Sans
- [Font Awesome](https://fontawesome.com/) — Icon library
- [Vercel](https://vercel.com/) — Hosting platform

---

<p align="center">Made with ❤️ in India &nbsp;|&nbsp; <a href="https://invoice-generator-neon-alpha.vercel.app/">Live Demo</a></p>
