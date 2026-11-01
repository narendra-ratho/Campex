# CAMPEX – Campus Lost & Found Management System
Static site: HTML5, CSS3, vanilla JS (ES6), Bootstrap 5 + Icons, Chart.js (CDN). Open `index.html` (or serve with `python -m http.server`).

## Demo accounts
- Admin: `admin@campex.edu` / `Admin@123`
- Student: `aarav@campex.edu` / `Student@123` (also `sneha@campex.edu`)

## Structure
`js/storage.js` data layer, auth, seed data, rule-based matching · `js/app.js` navigation and all page logic · `css/style.css` design system.

## Matching
Rule-based score out of 100: name similarity 40, category 20, location 20, date proximity 10, description keywords 10. Matches need ≥40. No AI is involved.

## Limitations
- localStorage is per-browser: data does not sync between devices or students.
- Client-side authentication is for demonstration only. Passwords are weakly hashed in the browser, sessions and roles can be edited via dev tools, and admin protection is not secure. A real deployment needs a server, database and proper auth.
- Images are compressed to max 600px JPEG; storage is ~5 MB per browser.
- User content is HTML-escaped before rendering.
