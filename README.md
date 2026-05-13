# Restaurant-Roulette-Frontend

The frontend for Restaurant Roulette, a web app that helps indecisive users pick a restaurant based on cuisine, price, distance, and rating preferences. Built as a team project for CP 317 — Software Engineering at Wilfrid Laurier University.

## My Role

This was a 10-person team project. I worked on the 3-person frontend sub-team responsible for the entire client-side of the application. A separate backend sub-team built the server, database, and search API.

My contributions on the frontend included:

- Building and styling the core pages (landing, login, signup, profile, preferences)
- Implementing client-side form validation (regex-based email and password checks, password visibility toggles, error messaging)
- Session handling via `localStorage` to persist user state and preferences across pages
- A reusable design system built on CSS custom properties for consistent theming
- Coordinating with the backend sub-team on the API contract for authentication and preferences

## Frontend Features

- **Landing page:** Hero section with location input, dynamically-positioned filter dropdowns (cuisine, price, distance, rating), feature highlights, testimonials, and a CTA section
- **Login page:** Email/password form with regex validation, password visibility toggle, and inline error messaging
- **Signup page:** Multi-field registration form with password strength rules, password confirmation matching, and terms-of-service checkbox validation
- **Profile dashboard:** Tabbed interface covering profile details, preferences, search history, favorites, and account settings
- **Preferences page:** Search radius slider, price-range checkboxes, searchable cuisine list (live filter by typing), minimum rating slider with dynamic star display, additional filters (open now, reservations, delivery, takeout, outdoor seating), and reset-to-defaults
- **Geolocation support:** The preferences page uses the browser's Geolocation API (`navigator.geolocation.getCurrentPosition`) to capture the user's current coordinates
- **Persistent user session:** Login state and saved preferences stored in `localStorage`; navbar updates dynamically to show a user dropdown menu when logged in
- **Responsive design:** CSS media queries adapt layouts for mobile screens across all pages

## Tech Stack

- **HTML5:** Semantic markup across all pages
- **CSS3:** Custom design system using CSS variables, flexbox, grid, and media queries
- **Vanilla JavaScript:** No frameworks; DOM manipulation, event handling, form validation, `localStorage`, and the Geolocation API
- **Font Awesome:** Icons via CDN
- **Git:** Version control across the team

## File Structure

```
restaurant-roulette-frontend/
├── index.html           # Landing page
├── login.html           # Login page
├── signup.html          # Signup page
├── profile.html         # User profile dashboard
├── preferences.html     # Restaurant preferences page
├── styles.css           # Global styles & design system
├── auth.css             # Auth page styles
├── profile.css          # Profile page styles
├── preferences.css      # Preferences page styles
├── script.js            # Landing page logic (filters, CTA, nav)
├── auth.js              # Login & signup logic (validation, session)
├── profile.js           # Profile dashboard logic (tabs, forms)
└── preferences.js       # Preferences page logic (sliders, geolocation, save/reset)
```
