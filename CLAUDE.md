# TrackCamp: theathletecoaches.com

Static website for Caleb Foster Elite Coaching, published with GitHub Pages from the `main` branch (custom domain in `CNAME`).

- `index.html`: The Everything Track Camp (camp info, schedule, coaches, registration)
- `coaching.html`: private 1-on-1 and group coaching (pricing, booking, contact form)
- Plain HTML/CSS/JS with styles inline in each page. No framework or build step.
- Project skills live in `.claude/skills/` (design, SEO, performance, conversion, pricing, Stripe).

## How to make changes

Anything pushed to `main` goes live on the public site, so:

1. Never push or commit directly to `main`.
2. Make changes on the session's working branch. Reuse one branch; don't create a new branch for every change.
3. Open a pull request into `main` that explains in plain language what changed and why.
4. Merge only after the owner explicitly says to.
5. Before opening the PR, open the changed pages in a browser and check that they render without script errors.

## Business facts to keep consistent

- The only contact email is `elitepc.coaching@gmail.com`. Don't add any other address.
- The first camp was 3 days. The upcoming camp is 2 days.
- Bookings go through Acuity Scheduling. The "Pay Your Way" option takes Venmo, Cash App, and Zelle.
