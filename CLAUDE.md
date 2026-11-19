# TrackCamp: theathletecoaches.com

Static website for Caleb Foster Elite Coaching, published with GitHub Pages from the `main` branch (custom domain in `CNAME`).

- `index.html`: The Everything Track Camp (camp info, schedule, coaches, registration)
- `coaching.html`: private 1-on-1 and group coaching (pricing, booking, contact form)
- Plain HTML/CSS/JS with styles inline in each page. No framework or build step.
- Project skills live in `.claude/skills/` (design, SEO, performance, conversion, pricing, Stripe, and marketing: analytics, copywriting, social, popups, email, referrals, paid ads, psychology, forms).

## Marketing plan

The marketing plan lives in a private Claude doc, not in this repository: https://claude.ai/artifact/Wio6v3TS5RuPfaNfSptm73. Read it with the docs tools before any marketing work, and keep its status line current. This repository is public, so never copy the plan's contents (prices, budgets, strategy) into files here.

## How to make changes

Anything pushed to `main` goes live on the public site, so:

1. Never push or commit directly to `main`.
2. Make changes on the session's working branch. Reuse one branch; don't create a new branch for every change.
3. Open a pull request into `main` that explains in plain language what changed and why.
4. Merge only after the owner explicitly says to.
5. Before opening the PR, open the changed pages in a browser and check that they render without script errors.

## Business facts to keep consistent

- The only contact email is `elitepc.coaching@gmail.com`. Don't add any other address.
- The first camp was 3 days. The upcoming camp is 2 days, Friday and Saturday, January 8–9, 2027, for ages 12–17. Camp times are not set yet (the Time card says TBA).
- Camp registration (every Register button and the 1-Day/2-Day pass buttons on `index.html`) goes to the Jotform at https://pci.jotform.com/form/263176564795068. The form also collects the waiver, medical info, and pass choice.
- Private and group coaching bookings on `coaching.html` go through Acuity Scheduling (and Calendly for small groups). The "Pay Your Way" option takes Venmo, Cash App, and Zelle.
- Google Analytics 4 Measurement ID is `G-MW5Z6PEV12`, installed in the `<head>` of both pages. A click listener at the end of each page sends `register_click`, `coaching_book_click` and `contact_click` events, and the coaching contact form sends `contact_submit`. Keep these when editing links, and never send names, emails or other personal details to Analytics.
