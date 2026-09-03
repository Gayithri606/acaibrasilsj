# acaibrasilsj.com
**Status:** Delivered · Paid client engagement · 2026

> **Client engagement** — built and shipped as paid work for Açaí Brasil SJ, a family-run
> Brazilian açaí business working a trailer and farmers market stalls across San Jose
> and the South Bay.

**The brief:** Need a website and  that should show where the trailer will be this week and lets a customer submit a catering request.

**The judgment call:** the obvious build was a CMS with a hosting plan and a monthly bill.
But the owners don't need a CMS — they need to change a schedule from a phone, between
markets. So: one self-contained HTML file, with the weekly schedule read from a Google
Sheet they already keep. They edit a row; the site updates. No framework, no build step,
no npm, no dependencies, and no recurring cost to the client.

**What's in it:** bilingual EN/ES, a two-layer schedule with seasonality filtering,
self-hosted fonts, JSON-LD structured data for local search, deployed to Cloudflare
via GitHub Actions.

**Live:**

### Client feedback

> "Gayithri is an AI Engineer who actually listens and delivers. As a food truck owner, I am non-technical, but she took my vision and handled all the tech and AI integration seamlessly and built a stunning website for my mobile acai business. She is very skilled, thorough and is very easy to work with. Highly recommend her!"

<sub>Verified on my <a href="https://www.upwork.com/freelancers/gayithrip">Upwork profile</a> — 100% Job Success · 5.0 rating · Rising Talent.</sub>
<sub>— NAME, Açaí Brasil SJ</sub>
<br>
<sub>Code by Gayithri Ponnapalli. Photography, logo and branding belong to the client.</sub>

Website for **Açaí Brasil SJ**, a family owned Brazilian açaí bowl business operating from a
trailer and a farmers market stall across San Jose and the South Bay.

## What this is

One self-contained HTML file. No framework, no build step, no npm, no CMS, no dependencies and no
recurring cost. Deploying it means copying a folder.

- **Bilingual EN/ES.** A translation dictionary plus `data-i18n` attributes; the language toggle
  re-renders in place.
- **Two-layer schedule.** A hardcoded recurring week, overridden for any given day by an optional
  Google Sheet published as CSV. The owner taps a three-question Google Form when he parks and the
  site updates. If the fetch fails or times out after 4s, it falls back silently to the default
  week rather than showing an error.
- **Seasonality.** Stops can carry a season range and are filtered and badged by the current
  Pacific month, so a summer-only market does not advertise itself in December.
- **Timezone pinned to `America/Los_Angeles`.** "Today" is correct regardless of the visitor's
  device clock, and the Google Form timestamp is anchored to the sheet's timezone rather than the
  visitor's.
- **Self-hosted fonts** (Poppins, SIL Open Font License 1.1). No third-party font request.
- **Structured data**: JSON-LD `FoodEstablishment`.

## Editing

Almost everything lives in the `CONFIG` block and the `WEEK` array near the top of the script in
`index.html`. Copy changes must be made in **both** languages.

## Licence

Code by Gayithri Ponnapalli. Photographs, logo and brand are the property of Açaí Brasil SJ and are
not licensed for reuse.
