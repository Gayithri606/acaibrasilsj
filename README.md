# acaibrasilsj.com

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
