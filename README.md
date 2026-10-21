# FUTURE | فيوتشر

A responsive, bilingual Arabic/English educational website with exactly four main HTML pages. Built with HTML5, CSS3, Vanilla JavaScript, Bootstrap 5 and a real Three.js scene.

## Files
- `index.html`: About FUTURE / homepage
- `register.html`: student and teacher registration
- `services.html`: educational services
- `why-us.html`: why choose FUTURE and FAQ
- `assets/css/style.css`: design system and responsive layout
- `assets/js/main.js`: navigation, translation, validation, and WhatsApp workflow
- `assets/js/translations.js`: Arabic/English dictionaries
- `assets/js/3d-scene.js`: Three.js hero scene and fallback
- `assets/images/`: add your own logo here

## Run locally
Extract the ZIP and open `index.html` in a modern browser. For best results, run a local server from this folder with `python -m http.server 8000`, then visit `http://localhost:8000`. The CDNs require an internet connection.

## Add your logo
Put your own file at `assets/images/logo.png`. The current shared header uses a typographic placeholder so the layout works without a logo. To use your image, replace `<span class="brand-mark">✦</span>` in `assets/js/main.js` header/footer templates with `<img src="assets/images/logo.png" alt="FUTURE logo" class="brand-image">` and add `.brand-image{width:42px;height:42px;object-fit:contain}` to the CSS.

## Configure WhatsApp
In `assets/js/main.js`, replace `const WHATSAPP_NUMBER="201XXXXXXXXX"` with your actual number in digits only, including country code. For Egypt use `20` followed by the number without its leading zero (example pattern `2010XXXXXXX`, replace Xs with your real digits). Do not include `+`, spaces, or hyphens. The site only prepares a message and opens WhatsApp after a user action; the user must press Send. No backend, database, API key, or paid service is needed for this workflow.

## Test registration
- Student: open `register.html?type=student`, fill name, phone, stage, grade, and consent; submit.
- Teacher: open `register.html?type=teacher`, fill name, phone, subjects, select at least one stage, and consent; submit.
- Test `register.html?type=student&stage=primary` and `register.html?type=student&stage=preparatory` for automatic stage selection.
- Confirm WhatsApp opens with a prepared message. Optional empty fields are omitted. Form values are not cleared before opening WhatsApp.

## Test language and 3D
Use the `العربية | EN` switcher; page language and direction change between Arabic RTL and English LTR while form values remain. The homepage renders a Three.js book, geometric shapes, star and particles. The scene pauses while the page is hidden and respects reduced-motion settings. If WebGL/Three.js is unavailable, a static decorative fallback appears.

## Privacy and factual claims
The form does not store submitted personal data in local storage or send it to analytics. No backend is included. Service descriptions are informational placeholders; confirm actual services before publishing. No fake testimonials, statistics, awards, or outcomes are claimed.
