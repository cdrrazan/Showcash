# Showcash 🚀

A single-page, animated showcase of all products built by
[Rajan Bhattarai (@cdrrazan)](https://github.com/cdrrazan).

## Featured products

| Product | What it is | Status |
|---|---|---|
| [Trackaru](https://trackaru.com) | Subscription tracking — never miss a payment | Live |
| Trovaru | Domain & SSL operations platform for agencies | In development |
| Linkaru | URL shortening, analytics & QR codes | In development |
| Linkart | Link-in-bio pages | In development |
| Signaru | Browser-trusted TLS certs via Let's Encrypt | In development |
| Keeparu | Private writing vault with public sharing | In development |
| [Kamandar](https://kamandar.byaru.com) | Personal GitHub command center | Live |
| [Denizens](https://devis.im) | Free `name.devis.im` subdomains & email aliases | Live |
| Pasten | Stealth mode 🤫 | Coming soon |
| [Roost](https://roost.pages.dev) | Local apps → live HTTPS on your own domain | Live |
| [Boardly](https://boardly-gh.pages.dev) | GitHub Projects boards on autopilot | Live |

## Running locally

It's a single self-contained `index.html` — no build step, no dependencies.

```sh
open index.html          # macOS
# or serve it:
python3 -m http.server   # → http://localhost:8000
```

## Tech

Plain HTML + CSS + vanilla JS. Responsive grid, scroll-triggered staggered
animations (IntersectionObserver), animated aurora background, and
`prefers-reduced-motion` support.
