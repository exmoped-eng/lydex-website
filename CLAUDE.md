# Lydex Solutions Website

## What this is

Company website for Lydex Solutions Ltd (Company Number 17117278, incorporated 25 March 2026).
A small UK app development studio run by Ed and Cheryl Talbot, building mobile games and educational apps.
The website serves three purposes:
1. Apple Developer Organisation requirement — Apple needs a live website on the company domain with a matching company email
2. Public-facing brand presence for both apps
3. Hosting privacy policies and support pages required by App Store and Google Play

## Hosting & tech constraints

- Hosted on Namecheap shared hosting (cPanel, Apache)
- Document root: `/home/edsbbprg/lydexsolutions.co.uk/`
- PHP 8.x available, Node.js is NOT available on the server
- No build step — files are uploaded directly via cPanel file manager or FTP
- Must be static HTML/CSS/JS or simple PHP only
- No npm, no webpack, no bundler, no React, no frameworks
- Google Fonts via CDN are fine
- SSL is active (HTTPS)
- This is NOT a SPA — each page is a separate HTML file

## Brand

- Company: Lydex Solutions Ltd
- Primary colour: Deep navy #1E3A5F
- Accent colour: Gold #C9A84C
- Background: #FAFAF8
- Text: #1A1A1A
- Muted text: #6B6B6B
- Border: #E2E0DB
- Tone: Professional but approachable. Quality indie studio, not corporate. No emojis, no hype language.
- Contact email: ed@lydexsolutions.co.uk
- Copyright: © 2026 Lydex Solutions Ltd

## Site structure

```
index.html                  — Homepage
mills-through-time.html     — Mills Through Time app page
spellstar.html              — SpellStar app page
about.html                  — About Lydex Solutions
contact.html                — Contact / support page
mills-privacy.html          — Mills Through Time privacy policy
spellstar-privacy.html      — SpellStar privacy policy
mills-support.html          — Mills Through Time support page
spellstar-support.html      — SpellStar support page
css/
  style.css                 — Shared stylesheet
images/
  logo.png                  — Company logo (to be added)
  mills/                    — Mills Through Time screenshots (to be added)
  spellstar/                — SpellStar screenshots (to be added)
```

## Pages — content guidance

### Homepage (index.html)
- Company name and logo
- One-liner: what Lydex Solutions does
- Two app cards: Mills Through Time (strategy game, coming soon) and SpellStar (educational app, in development)
- Brief about section
- Contact email
- Footer with company registration number and privacy policy links

### Mills Through Time (mills-through-time.html)
- App description: Nine Men's Morris strategy game, 7 historical eras (Caveman to UltraModern), career mode with themed AI opponents, ad-free, no tracking, no internet required
- Feature highlights: 4 game modes (Career, Quick Play, Time Challenge, Local 2-Player), 7 themed boards with unique artwork, 14 themed game pieces, AI with 4 difficulty levels, in-app history of Nine Men's Morris
- Status: Coming soon to the App Store
- Pricing: Free with optional premium unlock (£3.99) for additional eras
- Privacy: No personal data collected, no tracking, no ads, no internet required
- Links to privacy policy and support page
- App Store badge placeholder (link to be added when live)

### SpellStar (spellstar.html)
- App description: Gamified spelling practice for UK primary school children aged 4-11, curriculum-aligned with DfE statutory word lists
- Feature highlights: 13 game modes, weekly spelling list import (photo, type, share code, QR), teacher/classroom mode, parent progress reports, avatar customisation, badge system
- Status: In development
- Pricing: Free tier with Spell Cast mode, paid tiers from £3.49/month
- Privacy: All data stored locally on device, no cloud, no tracking, COPPA and UK Children's Code compliant
- Links to privacy policy and support page

### About (about.html)
- Who we are: Ed and Cheryl Talbot, husband and wife team based in England
- What we do: build mobile games and educational apps
- Our approach: AI-assisted development, privacy-first, no ads, fair pricing
- Company registration details

### Contact (contact.html)
- Email: ed@lydexsolutions.co.uk
- For app support: link to relevant support pages
- Not a contact form — just clear contact information

### Privacy policies
- Mills Through Time: No personal data collected. No tracking, no analytics, no ads, no third-party SDKs, no internet required. Mention ICO registration number (pending — leave placeholder).
- SpellStar: Local-only data storage. Data collected: child first name, school year, learning progress, PIN (hashed). No cloud, no external APIs, no tracking, no analytics. PIN-gated parent area. COPPA and UK Children's Code compliant. Mention ICO registration number (pending — leave placeholder).

### Support pages
- Simple pages with FAQ-style content
- How to contact us
- App-specific troubleshooting basics

## Design rules

- Mobile-first responsive design — Ed works primarily from iPhone
- Clean, minimal, fast-loading
- No hero images or large stock photos
- No animations beyond subtle hover transitions
- Consistent nav across all pages
- Fonts: load from Google Fonts CDN. Pick something clean and modern with character — not Inter, not Roboto, not Arial
- All pages must be valid HTML5
- Semantic markup (header, nav, main, section, footer)
- Accessible — proper heading hierarchy, alt text, sufficient contrast
- All links must work — no dead links, no placeholder "#" hrefs (use real paths or leave the link out)

## What NOT to do

- No JavaScript frameworks (React, Vue, Angular, etc.)
- No build tools (webpack, vite, parcel, etc.)
- No npm or package.json
- No CSS frameworks (Tailwind, Bootstrap, etc.)
- No dark mode toggle (not needed)
- No cookie banner (we don't use cookies)
- No blog (not needed yet)
- No pricing tables with elaborate tier comparisons
- No stock photography or placeholder images
- No "coming soon" countdown timers
- No newsletter signup forms
- No chatbots or live chat widgets

## Deployment
After committing and pushing to GitHub, deploy to live site with:
ssh -i "C:\Users\Ed Talbot\.ssh\id_lydex" edsbeprg@184.94.213.157 -p 21098 "cd /home/edsbeprg/lydexsolutions.co.uk && git pull"