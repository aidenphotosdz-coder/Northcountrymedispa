# North Country Massage & Medi Spa — Website (v1)

A redesigned, mobile-first website for **North Country Massage & Medi Spa** (Prince Albert, SK).
Static HTML/CSS/JS — no build step, no dependencies. Opens in any browser.

---

## Preview locally

Just open `index.html` in a browser. For the embedded booking page to behave exactly
like production, you can optionally run a tiny local server:

```bash
# from the project folder
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (GitHub Pages)

1. Push this folder to a GitHub repository.
2. Repo **Settings → Pages → Build and deployment**.
3. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**.
4. Save. The site goes live at `https://<user>.github.io/<repo>/` in a minute or two.

`index.html` is the entry point and all links are relative, so it works from the repo root.

---

## Structure

```
index.html              Home page
book.html               On-site booking (embeds the Mangomint scheduler)
<treatment>.html        17 individual treatment pages (e.g. botox-dysport.html)
assets/
  style.css             Single shared stylesheet (whole site is themed here)
  logo-black.svg        Full logo lockup (dark)
  logo-white.svg        Full logo lockup (light — used in footer)
  mark-black.svg        Lotus icon mark (dark)
  mark-white.svg        Lotus icon mark (light — used in nav/hero)
PLACE HOLDER LOGOS/     Original logo source files
```

### Treatment pages
Medical Cosmetics: `botox-dysport`, `dermal-fillers`, `laser-treatments`, `skin-resurfacing`, `skin-tightening`
Aesthetics: `eyebrows-eyelashes`, `facials-peels`, `hydrafacial`, `alumier-peels`, `hair-removal`, `manicures-pedicures`, `teeth-whitening`
Therapeutic: `massage-therapy`, `relaxation-massage`, `cold-laser`, `shockwave`, `mens-therapy`

To restyle the whole site, edit `assets/style.css` (CSS variables at the top control the palette).

---

## Features

- Responsive, mobile-first layout with a clean full-screen mobile menu
- Transparent header that turns solid on scroll
- Sticky **Call / Book Now** bar on mobile + always-visible Book button on desktop
- On-site booking page embedding the Mangomint scheduler
- Hover-reveal "Signature Treatments", animated stats, testimonial slider, FAQ accordion
- Scroll-reveal animations, back-to-top, full dropdown navigation

---

## Notes for review (v1)

- **Photography is placeholder** (Unsplash). Swap in real spa / team / treatment photos before launch — this is the single biggest visual upgrade remaining.
- **Hours** shown are a sensible placeholder; confirm and update if displayed.
- **Booking embed:** `book.html` embeds `booking.mangomint.com`. If Mangomint's settings
  block being shown inside a frame, the page automatically offers an "Open booking in a new
  window" button and a click-to-call fallback. If you want the calendar to always render
  inline, enable embedding in Mangomint or paste their official embed snippet into `book.html`.
- Content (service descriptions) mirrors the current live site.

## Contact details used on the site
- Address: 683 7th St. E, Prince Albert, SK
- Phone: (306) 922-2255
- Email: info@northcountrymedispa.com
- Booking: booking.mangomint.com/northcountrymedispa
- Gift cards: clients.mangomint.com/gift-cards/northcountrymedispa
