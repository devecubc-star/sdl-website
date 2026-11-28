# Sustainable Development Lab website

A small static site (plain HTML, CSS and a little JavaScript; no build step) for the Sustainable Development Lab (SDL), built to run on **GitHub Pages**.

```
index.html      Home: Mission, Vision, four-step process
research.html   Research: sports-equipment circular economy cycle
team.html       Team: 2 leads + 6 members
contact.html    Contact: survey link, email, phone numbers
css/style.css   All styling (colours are variables at the top)
js/main.js      Mobile menu, scroll animation, copy-email button
assets/         logo.png, favicon.png, hockey-stick.svg, team/ (photos)
```

## Things to fill in

Search for `EDIT:` in the HTML files to jump to each spot.

| What | Where | How |
|---|---|---|
| Team names, roles, bios | `team.html` | Each person is one `<article class="person">` block. Replace `Full Name`, the role, and the bio text. |
| Team photos | `assets/team/` + `team.html` | Add a square-cropped JPG or PNG (about 400×400), then change that person's `src="assets/team/placeholder.svg"` to your file and update the `alt` text. |
| Survey link | `contact.html` | In the survey card, change `href="#"` to your survey URL, delete `aria-disabled="true"`, and delete the "Link coming soon." line. |
| Phone numbers | `contact.html` | Replace the `Team Lead 1/2` and `Number coming soon` text. Copy or delete a `<div class="phone">` to add or remove a number. |
| Email | `contact.html`, footer | Already set to `devec.ubc@gmail.com`. |

## Review before publishing

- **Wording.** The Home and Research text was supplied by the team. Edit it in `index.html` and `research.html`.
- **Board approval.** MOA §11.3 says no Party makes public representations for the SDL, or uses another Party's name or logo, without Board approval. The site names BeSci and EPA in text only and uses no other club's logo. Get Board sign-off before going public.
- **Research topic.** The sports-equipment work is worded as "exploring" because the Project Document shows no partner secured yet.
- **Internal details.** No budgets, funding sources or partner pipeline appear on the site.

## Preview locally

From this folder:

```powershell
python -m http.server 8000
```

Then open http://localhost:8000.

## Publish on GitHub Pages

1. Create a GitHub repository (ideally under an account or organization tied to `devec.ubc@gmail.com`, so ownership survives turnover).
2. Upload these files to the `main` branch, with `index.html` at the top level.
3. In the repository, go to **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute or two the site is live at `https://<account>.github.io/<repository>/`. A custom domain can be added in the same settings page.

## Handoff

The MOA (§3.4, §12) expects documentation to live in a shared repository. Keep this site in the same place, add the next team's names, and update the dates and cluster details each program year.

## Design notes

The look borrows from the logo: the S-curve (wave dividers and the leaf-shaped Mission/Vision cards), the dark-to-mint gradient (buttons, process bubbles and photo rings), the circle (team photos, hero rings, process bubbles and the research cycle) and the pill shape from the project-document title bar (navigation and buttons). The site is light-only, on a white background. The logo is static; the only motion is a gentle fade-in on scroll and the arrows on the research cycle, and both switch off for visitors who prefer reduced motion.
