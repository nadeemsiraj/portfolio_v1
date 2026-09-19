# Mohd Nadeem Siraj — Portfolio

A single-file portfolio site. All CSS and JavaScript are inlined in `index.html`,
so there is nothing to build, install or compile. Open the file and it works.

---

## Before you publish — 4 things

**1. Add your photo.** Save it as `assets/images/Portfolio.png`.
Without it the page shows an "NS" monogram instead, so nothing breaks — but
a real photo does a lot of work on a portfolio.

**2. Add your CV.** Save it as `assets/Mohd-Nadeem-Siraj-CV.pdf`.
The Download CV button stays hidden until that file exists, so visitors never
hit a 404. If you don't have a PDF, open the site and press `Ctrl+P` → Save as
PDF; the print stylesheet produces a clean black-and-white résumé from the page
itself.

**3. Replace the placeholder domain.** Five places in `index.html` use
`https://nadeemsiraj.github.io/` — the canonical link, `og:url`, `og:image`,
and the JSON-LD block. Also update `robots.txt` and `sitemap.xml`. Find and
replace the whole string with your real address. Getting this right is what
makes your link show a preview card on LinkedIn and WhatsApp.

**4. Check the testimonials.** The Testimonials section quotes Sapan Chaudhary
and Rajan Verma by name and job title. If those quotes aren't things they
actually said and agreed to publish, remove the section or get their sign-off
first. Hiring managers do check.

---

## Deploying

**GitHub Pages** — push this folder to a repo, then Settings → Pages → deploy
from `main` / root. If the repo is named `<username>.github.io` it serves at
your root domain.

**Netlify or Vercel** — drag the folder onto the dashboard. Done.

**Any shared host** — upload the contents via FTP to `public_html`.

The contact form posts to Formspree (`formspree.io/f/xqpkzobw`) and needs no
server, but it does need the site to be on `http(s)://`, not opened as a local
file.

---

## Editing content

Everything is plain HTML — search for the text you want to change.

| What | Where to look |
|---|---|
| Name, tagline, pitch | `<header class="hero">` |
| Rotating phrases under your name | `var roles=[...]` in the script |
| The 3D cloud's technologies | `var ITEMS=[...]` — `sys`, `net` or `ops` sets the colour |
| Stat counters | `data-to="..."` attributes |
| Skill chips and bars | `<section id="skills">` |
| Jobs | `<section id="experience">` |
| Colours, fonts, spacing | The `:root` block at the top of `<style>` |

**One rule if you edit the cloud:** every entry in `ITEMS` should have a
matching chip in the Skills section, otherwise clicking that tag scrolls but
highlights nothing. Where the wording differs, add an entry to the `ALIAS`
map in the script.

---

## What's built in

- 3D tech cloud with perspective depth, drag-to-spin momentum and
  colour-coding by discipline
- Pointer-tilt cards, scroll reveals, animated counters and skill bars
- Dark and light themes, remembered between visits
- Copy-to-clipboard on your email and phone
- Print stylesheet that turns the page into a résumé
- Person schema (JSON-LD), Open Graph tags, sitemap and robots.txt
- Honeypot spam trap on the contact form
- Respects `prefers-reduced-motion`; animation pauses when off-screen or when
  the tab is in the background
- Keyboard-accessible equivalents for the cloud, skip link, focus styles,
  and WCAG AA text contrast in both themes
- Readable without JavaScript

## Browser support

Chrome, Edge, Firefox and Safari, current and previous versions. Uses
`backdrop-filter`, `color-mix()` and Pointer Events. Internet Explorer is not
supported.
