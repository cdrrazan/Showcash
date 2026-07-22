<div align="center">

<img src="assets/banner.svg" alt="Showcash — products built by Rajan Bhattarai" width="100%">

<br>

[![Website](https://img.shields.io/badge/Website-cdrrazan.com-7c6cff?style=for-the-badge&logo=googlechrome&logoColor=white)](https://cdrrazan.com)
[![GitHub](https://img.shields.io/badge/GitHub-cdrrazan-181717?style=for-the-badge&logo=github)](https://github.com/cdrrazan)
[![X](https://img.shields.io/badge/X-@cdrrazan-000000?style=for-the-badge&logo=x)](https://x.com/cdrrazan)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-cdrrazan-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/cdrrazan)
[![dev.to](https://img.shields.io/badge/dev.to-cdrrazan-0A0A0A?style=for-the-badge&logo=devdotto)](https://dev.to/cdrrazan)

![Products](https://img.shields.io/badge/Products-11-38bdf8?style=flat-square)
![Live](https://img.shields.io/badge/Live-5-34d399?style=flat-square)
![Stack](https://img.shields.io/badge/Made%20with-HTML%20·%20CSS%20·%20Vanilla%20JS-f472b6?style=flat-square)
![No build](https://img.shields.io/badge/Build%20step-none-fbbf24?style=flat-square)

<p>A single-page, animated showcase of every product shipped by<br>
<b>Rajan Bhattarai</b> — full-stack Rails developer from Nepal 🇳🇵, GitKraken Ambassador,<br>
and author of <i>Case Brand when Dev</i>.</p>

</div>

---

## ✨ Preview

<div align="center">
<img src="assets/preview-hero.png" alt="Hero section with author profile and product grid" width="90%">
<br><br>
<img src="assets/preview-grid.png" alt="Product grid with live status badges and tech stacks" width="90%">
</div>

## 🚀 The product lineup

| | Product | What it is | Tech | Status |
|---|---|---|---|---|
| 💳 | **[Trackaru](https://trackaru.com)** | Subscription tracking — never miss a payment again | Rails | 🟢 Live |
| 🌐 | **Trovaru** | Domain & SSL operations platform for agencies | Rails | 🟡 In dev |
| 🔗 | **Linkaru** | URL shortening, analytics & QR codes | TypeScript | 🟡 In dev |
| 🎨 | **Linkart** | Link-in-bio pages, unlimited & instant | Rails | 🟡 In dev |
| 🔐 | **Signaru** | Browser-trusted TLS certs via Let's Encrypt | Rails · ACME | 🟡 In dev |
| 📓 | **Keeparu** | Private writing vault with deliberate public sharing | Rails | 🟡 In dev |
| 🎛️ | **[Kamandar](https://kamandar.byaru.com)** | Personal GitHub command center across 5 surfaces | Ruby stdlib | 🟢 Live |
| 🏷️ | **[Denizens](https://devis.im)** | Free `name.devis.im` subdomains & email aliases | Ruby · TS · Actions | 🟢 Live |
| 🤫 | **Pasten** | Stealth mode — coming soon | — | ⚪ Soon |
| 🏠 | **[Roost](https://roost.pages.dev)** | Local apps → live HTTPS on your own domain | Go · Docker · Caddy | 🟢 Live |
| 📋 | **[Boardly](https://boardly-gh.pages.dev)** | GitHub Projects boards on autopilot | TS · Actions | 🟢 Live |

## 🛠️ Running locally

The whole site is one self-contained `index.html` — no build step, no dependencies.

```sh
open index.html          # macOS — just open it
python3 -m http.server   # …or serve it → http://localhost:8000
```

## 🧬 How it's built

- **Plain HTML + CSS + vanilla JS** — zero frameworks, zero libraries
- **Data-driven grid** — products live in one JS array; cards render from it
- **Animations** — aurora background, staggered scroll-in reveals
  (`IntersectionObserver`), hover lift & glow, pulsing live badges
- **Resilient images** — GitHub OpenGraph covers with gradient-monogram fallbacks
- **Accessible** — semantic markup and full `prefers-reduced-motion` support

<div align="center">

---

Built with ❤️ by [Rajan Bhattarai](https://cdrrazan.com) · [@cdrrazan](https://x.com/cdrrazan)

</div>
