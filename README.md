# The Inventor's Lab — V1

A static site, no build step. Open any .html file directly in a browser, or deploy as-is.

## Structure

- `index.html` — Lab homepage
- `workbench.html` — pulls its cards from `assets/data/workbench.js`
- `builders-corner.html` — placeholder cards, edit directly in the HTML for now
- `generator.html` — your original generator, unchanged logic/data, with the shared nav added
- `assets/css/site.css` — shared design tokens, nav, ticket card system
- `assets/data/workbench.js` — the list of experiments; add a new one by copying an existing object

## To edit

**Add a Workbench experiment:** open `assets/data/workbench.js`, copy one of the objects in the `WORKBENCH` array, fill in `topic` / `method` / `direction` / `sparked` / `details`. Three of the five entries (Pissy Password Bot, Good Luck Ramses, Gamified Triage) have placeholder topic/method/direction combos marked with a comment — swap in the real ones when you have them.

**Change the Lab Notes link:** it currently points to `https://your-substack-url.substack.com` in three places (`index.html`, `workbench.html`, `builders-corner.html`, and `generator.html`'s nav). Find-and-replace that URL once your Substack is live.

**Change site-wide colors/fonts:** edit the `:root` block at the top of `assets/css/site.css`.

## Deploy to Vercel

1. Push this folder to a GitHub repo (or drag-and-drop the folder into the Vercel dashboard).
2. In Vercel: New Project → Import → select the repo.
3. Framework preset: "Other" (it's static HTML, no build command needed).
4. Deploy.

No environment variables, no build step — it's just HTML/CSS/JS.
