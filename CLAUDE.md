# TrackCamp: theathletecoaches.com

Static website for Caleb Foster Elite Coaching, published with GitHub Pages from the `main` branch (custom domain in `CNAME`).

- `index.html`: The Everything Track Camp (camp info, schedule, coaches, registration)
- `coaching.html`: private 1-on-1 and group coaching (pricing, booking, contact form)
- Plain HTML/CSS/JS with styles inline in each page. No framework or build step.
- Project skills live in `.claude/skills/` (design, SEO, performance, conversion, pricing, Stripe, and marketing: analytics, copywriting, social, popups, email, referrals, paid ads, psychology, forms).

## Marketing plan

The marketing plan lives in a private Claude doc, not in this repository: https://claude.ai/artifact/Wio6v3TS5RuPfaNfSptm73. Read it with the docs tools before any marketing work, and keep its status line current. This repository is public, so never copy the plan's contents (prices, budgets, strategy) into files here.

## Open items (as of November 20, 2026)

Pick up here in a new session. Remove items as they're finished.

- **Prizes section (drafted, not live):** an Apple-style sideways-scrolling row of 5 prize cards (Gift Card, Camp Beanie, Hoodie, Backpack, Gift Card), saved in `drafts/prizes-section.html`. It goes in `index.html` directly before the "Your Host" section. Before publishing, the owner needs to give: how athletes win the prizes (the "daily games" line is a guess), the two gift card amounts, and optionally real photos to replace the gold icons. The `drafts/` folder is excluded from the website in `_config.yml`.
- **Camp times and location:** not set yet; the Time and Location cards on `index.html` say TBA.
- **Jotform:** consider adding the dates to the "How many days" question (Day 1: Fri Jan 8, Day 2: Sat Jan 9).
- **Completed-registration tracking:** the owner is setting up a Zapier zap ("Send measurement events in Google Analytics 4 for new submissions in Jotform") with event name `registration_complete`. An alternative is a `thank-you.html` page on the site that Jotform redirects to.
- **Privacy notice:** suggested a short footer note that the site uses Google Analytics.
- **Marketing:** dates are set, so the next steps are the dates announcement, early access for past families, and Instagram posts (see the marketing plan).
- **Search setup the owner must do:** verify the site in Google Search Console (add their verification meta tag to both pages' `<head>`, then submit `sitemap.xml`), and create a Google Business Profile.
- **Service area:** the site says "Fresno, CA" (titles, descriptions, Location card note, structured data). This was assumed; confirm with the owner.

## Search (SEO) setup

Both pages have a title and meta description that name Fresno, CA, a canonical link, share tags (`og-camp.jpg`, `og-coaching.jpg`, 1200×630), favicons (`favicon.ico`, `favicon-96.png`, `apple-touch-icon.png`), and a JSON-LD block in `<head>` (Organization + Person, plus an Event on `index.html` and a Service on `coaching.html`). `robots.txt` and `sitemap.xml` are at the root. When camp dates, times, location, prices or events change, update the visible page AND the JSON-LD and meta description to match, and bump `lastmod` in `sitemap.xml`. Keep titles under about 60 characters and descriptions under 160.

## How to make changes

Anything pushed to `main` goes live on the public site, so:

1. Never push or commit directly to `main`.
2. Make changes on the session's working branch. Reuse one branch; don't create a new branch for every change.
3. Open a pull request into `main` that explains in plain language what changed and why.
4. Merge only after the owner explicitly says to.
5. Before opening the PR, open the changed pages in a browser and check that they render without script errors.

## Business facts to keep consistent

- The only contact email is `elitepc.coaching@gmail.com`. Don't add any other address.
- The first camp was 3 days. The upcoming camp is 2 days, Friday and Saturday, January 8–9, 2027, for ages 12–17. Camp times and location are not set yet (the Time and Location cards say TBA).
- Each camp day has 4 parts, shown under "What to Expect": 1. Purpose of the Day (a Bible verse and theme, and how athletes should live it out), 2. Warmup, 3. 2 Rotating Event Stations, 4. Group Game & Day Recap. The verse card in step 1 shows Hebrews 12:1 as an example.
- Events (2 stations a day): "Day 1: Rhythm and Technique" = Long Jump and Hurdles; "Day 2: Speed and Power" = Speed & Blocks (sprints) and Shot Put.
- Camp registration (every Register button and the 1-Day/2-Day pass buttons on `index.html`) goes to the Jotform at https://pci.jotform.com/form/263176564795068. The form also collects the waiver, medical info, and pass choice.
- Private and group coaching bookings on `coaching.html` go through Acuity Scheduling (and Calendly for small groups). The "Pay Your Way" option takes Venmo, Cash App, and Zelle.
- Google Analytics 4 Measurement ID is `G-MW5Z6PEV12`, installed in the `<head>` of both pages. A click listener at the end of each page sends `register_click`, `coaching_book_click` and `contact_click` events, and the coaching contact form sends `contact_submit`. Keep these when editing links, and never send names, emails or other personal details to Analytics.
