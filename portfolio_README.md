# Jay Gajjar — Portfolio (Flutter Widget Tree)

An interactive Flutter DevTools-style portfolio. Single HTML file. Zero build steps.

---

## 🚀 Deploy to GitHub Pages (5 minutes)

### Option A: User Site at `https://j-j-gajjar.github.io`

1. Go to GitHub and create a new repo named **exactly** `j-j-gajjar.github.io` (the name must match your username + `.github.io`).
2. Drop these files into the repo root:
   - `index.html` (the portfolio)
   - `jay_gajjar_resume.pdf` (so the "Download Resume" button works)
3. Commit + push.
4. Open repo **Settings → Pages** and confirm:
   - Source: **Deploy from a branch**
   - Branch: `main` / root
5. Wait ~30 seconds. Visit `https://j-j-gajjar.github.io` ✅

### Option B: Project Site at `https://j-j-gajjar.github.io/portfolio`

1. Create any repo, e.g. `portfolio`.
2. Add `index.html` + `jay_gajjar_resume.pdf` to it.
3. **Settings → Pages → Source = main branch root.**
4. Visit `https://j-j-gajjar.github.io/portfolio` ✅

---

## 📝 Customizing content

Open `index.html` in any editor. Two places to edit:

### 1. Personal info (top of `<script>` block)

```js
const ME = {
  name: 'Jay Gajjar',
  initials: 'JG',
  role: 'Mobile App Developer',
  location: 'Surat, Gujarat · India',
  tagline: '...',
  email: 'gajjarjay52@gmail.com',
  phone: '+91 9574182452',
  github: 'https://github.com/j-j-gajjar',
  linkedin: 'https://www.linkedin.com/in/jjgajjar',
  resume: './jay_gajjar_resume.pdf'
};
```

### 2. Tree structure (`const tree = { ... }`)

Add/remove nodes here. Each node has:
- `id` — unique string
- `type` — `'W'` (widget), `'SW'` (stateful), `'C'` (container), `'T'` (text), `'L'` (list), `'M'` (method), `'P'` (property)
- `name` — what shows in the tree
- `detail` — key matching a view in `views = { ... }` (the right-pane content)
- `children` — array of child nodes (omit for leaf)
- `expanded: true` — open by default
- `highlight: true` — show blue accent bar (use sparingly for "important" nodes)
- `meta: '...'` — small label on the right side (e.g. dates, count)

### 3. Detail views (`const views = { ... }`)

Each view returns HTML. Wrap content in `<div class="fade-in">` for the smooth entry animation.

---

## ✨ Features

- **Boot sequence intro** — terminal `flutter run` animation on load
- **Interactive widget tree** — expand/collapse like Flutter Inspector
- **Live search/filter** — type in the search box to filter nodes
- **Real-time clock** in status bar
- **Easter eggs** — try typing `flutter` or `jay` anywhere on the page 🥚
- **Fully responsive** — works on mobile (tree on top, detail below)
- **Reduced-motion friendly** — respects OS-level setting and skips boot animation
- **Zero dependencies** — vanilla JS, single file, ~50KB total

---

## 🎨 Theming

All colors are CSS variables at the top of `<style>`:
- `--flutter` (primary blue): `#54C5F8`
- `--stateful` (orange): `#FFB454`
- `--container` (green): `#82E59A`
- `--text-amber`, `--list-purple`, `--method-pink` for syntax-style accents

Change them once and the whole UI rethemes.

---

## 🥚 Easter eggs

- Type `flutter` anywhere on the page → "flutter doctor" toast pops up
- Type `jay` → hints to download resume

