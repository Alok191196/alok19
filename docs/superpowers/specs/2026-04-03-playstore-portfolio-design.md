# Play Store Portfolio — Design Spec

## Overview

A static portfolio website for Alok Kumar Singh (Senior Android Developer) styled as a Google Play Store developer page. The goal is to land an Android Developer job by impressing recruiters with a familiar, professional interface that instantly communicates "Android expert."

## Target Audience

Recruiters and hiring managers for Android Developer positions. The Play Store aesthetic creates immediate recognition and signals deep Android ecosystem knowledge.

## Technical Stack

- **Static site:** Single HTML file with embedded CSS and JS
- **No frameworks:** Pure HTML/CSS/JS, no build step
- **Fonts:** Google Sans, Roboto, Roboto Mono (via Google Fonts CDN)
- **Icons:** Material Icons Round (via Google Fonts CDN)
- **Deployment:** GitHub Pages, Netlify, or Vercel (any static host)

## Layout

### Top Bar (fixed)
- Google Play logo (SVG with gradient)
- Search bar (pre-filled with "Alok Kumar Singh", readonly)
- User avatar (initials "A" with gradient)

### Sidebar (fixed left, 240px)
- Navigation items: Overview, Published Apps, Skills, Experience, Contact, About
- Dividers separating sections
- Certifications section (Google Certified, HackerRank)
- Active state highlights based on scroll position
- Hidden on screens < 900px

### Main Content (scrollable, right of sidebar)

#### 1. Developer Profile Header
- 96px app icon (Android bugdroid SVG, gradient background with shimmer)
- Name with verified badge
- Subtitle: "Senior Android Developer"
- Bio paragraph (6+ years, fintech, 1M+ users, Kotlin/Compose/KMM)
- Badge chips: Google Certified, HackerRank, Bengaluru
- Stats row: 6+ Years, 1M+ Users, 4 Apps, 4.9 Rating
- Action buttons: Contact (filled), LinkedIn (outlined)

#### 2. Performance Metrics
- 6-column grid bar with 1px gap borders
- Cells: Crash-Free (99.33%), Users (1M+), Deploy (-70%), Notif Rate (99.99%), Productivity (3-5x), PRs/Week (15+)
- Each cell shows value, label, delta
- Hover: background change

#### 3. Developer Rating
- Large 4.9 rating number with stars
- 5-bar breakdown chart with animated fills on scroll

#### 4. Published Apps
- Horizontal scrollable row of app cards (200px wide each)
- Each card: gradient banner image, mini icon, app name, developer name, star rating, category
- 4 apps: Trading App, Analysis App, Cashify, CricBuzz Clone
- Placeholder `href="#"` for Play Store links (user will add later)

#### 5. Skills & Categories
- Grouped by domain: Languages, Android, Architecture & Testing, Tools & AI
- Each skill is a chip with circular colored icon and label
- Hover: lift + background change, click: scale bounce

#### 6. Experience Reviews
- Card per role, styled as Play Store reviews
- Each card: company avatar (gradient circle), company name, role, period
- Star rating row
- Bullet list of achievements with highlighted metrics
- "Helpful" and "Share" action buttons
- Staggered slide-in animation

#### 7. Contact Information
- "Data Safety" styled card
- Rows: Email, Phone, Location, LinkedIn
- Each with circular icon, label, value
- Email and LinkedIn are clickable links

#### 8. About This Developer
- Education: B.Tech, PSIT, 2014-2018
- Certifications: Google Certified, HackerRank
- Interests: Strategy Games, Tech, Culinary, Sudoku

### Footer
- Copyright line with links (Privacy, Terms, About)

## Animations & Interactions

- **Scroll reveal:** `.reveal` elements fade up on intersection
- **Sidebar active state:** Updates based on scroll position
- **Rating bars:** Animate from 0% to target width when scrolled into view
- **Skill chips:** Scale bounce on click
- **App cards:** Scale up on hover
- **Review cards:** Staggered slide-in animation (0.1s delay per card)
- **Developer icon:** Shimmer animation on the gradient overlay

## Responsive Behavior

- **< 900px:** Sidebar hidden, main content full-width, developer header stacks vertically
- **< 600px:** Metrics grid becomes 2-column, dev actions stack vertically, rating breakdown stacks

## Files

- `portfolio-f-playstore.html` — The chosen portfolio (current working prototype)
- `portfolio-a-terminal.html` — Terminal variant (kept)
- `portfolio-b-ide.html` — IDE variant (kept)
- `portfolio-c-hybrid.html` — Hybrid variant (kept)
- `portfolio-d-scifi.html` — Sci-Fi variant (kept)
- `portfolio-e-android.html` — Android variant (kept)

## Remaining Work

1. Polish the chosen Play Store portfolio into a production-ready `index.html`
2. Add real Play Store links when user provides them
3. Optimize for deployment (minify if desired)
4. Deploy to a static host (GitHub Pages recommended)
