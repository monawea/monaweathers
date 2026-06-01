# Mona Weathers — Project Notes

## Mobile hamburger menu

When adding or fixing a hamburger menu, always use the **show by default, hide on desktop** pattern. The reverse (hide by default, show on mobile via `max-width` media query) fails because the base `display: none` rule overrides the media query if it appears later in the stylesheet.

**Correct pattern:**
```css
/* Show by default */
.nav-hamburger { display: flex; flex-direction: column; ... }

/* Hide on desktop */
@media (min-width: 861px) { .nav-hamburger { display: none; } }
```

**Broken pattern (do not use):**
```css
.nav-hamburger { display: none; ... }
@media (max-width: 860px) { .nav-hamburger { display: flex; } } /* overridden by rule above */
```

## Deployment

- GitHub repo: https://github.com/monawea/monaweathers
- GitHub Pages preview: https://monawea.github.io/monaweathers/
- Production host: Hostinger (monaweathers.com) — auto-deploys from GitHub main branch
- Git commits require: `git -c commit.gpgsign=false commit`
- Git push requires a personal access token embedded in the URL: `git push https://<TOKEN>@github.com/monawea/monaweathers.git main`

## Forms

- Challenge application form (work-with-me.html): Formspree `https://formspree.io/f/xlgvkgqz`
- Cohort application form (cohort.html): Formspree `https://formspree.io/f/mlgvqrkj`

## Key design details

- Email `monaweathers1@gmail.com` must NOT appear on any website page
- Isabelle Lesschaeve photo: use class `face-top` (`object-position: center 15%`) to keep her face centered
- Cohort community is called **The Growth Squad**
- Legal entity: Steady Systems LLC, Georgia
