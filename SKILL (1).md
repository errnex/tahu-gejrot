# Maps Lead Hunter

Use this when the user wants to find businesses on Google Maps to pitch custom app / website services — specifically businesses OUTSIDE Indonesia that have NO website yet, only an email, phone number, Instagram, or Facebook. For every qualified business found, write one unique, personalized outreach message ready to copy-paste.

## Goal

Find real local businesses that are visible on Maps and have customers, but have no website of their own — then give Sky a different outreach template for each one, matched to whatever contact channel that business actually has, so he can sell them a custom website or app.

## Inputs (ask only what is missing)

- **Region**: country / city / area to hunt in. Must be OUTSIDE Indonesia. If Sky does not name one, propose one (start with US small cities, UK, Australia, or Canada) and confirm.
- **Category / niche**: e.g. barbershops, salons, restaurants, cafes, gyms, dental clinics, auto repair, real estate agents, pet groomers. If not named, pick one niche per run and say which.
- **How many leads**: default 10 per run.
- **Outreach language**: default English. If the business is in a non-English-speaking country, write the template in the local language when it can be done correctly; otherwise English.

## Tools

- **Places connector** (`places`) for Maps search and place details — read `/opt/hatch/connectors/places/CONNECTOR.md` before searching. Use it to get name, category, address, phone, website field, rating, review count, and social links.
- **Web search** to verify the no-website claim: search `"<business name>" <city>` and check the results.

## Qualification rules

- **Outside Indonesia only.** Exclude any business located in Indonesia (country code ID).
- **No website of their own.** The Maps listing has an empty website field AND a web search turns up no official site / domain owned by the business. A Facebook page, Instagram profile, or a listing on a directory (Yelp, TripAdvisor, JustEat, etc.) is NOT a website — those still qualify.
- **At least one reachable contact**: email, phone/WhatsApp number, Instagram, or Facebook page.
- **Prefer active businesses**: recent reviews, photos, or social posts — they have customers and money, just no web presence. Best prospects.
- **Skip**: chains / franchises with a corporate site, businesses that already have an app, permanently closed listings, and anything with no contact channel at all.

## Search method

1. Search Maps per category + city, one city x one niche at a time.
2. For each candidate, pull place details and record: name, category, city/country, Maps link, phone, email, Instagram, Facebook, rating + review count, and what is missing (website / online booking / menu-prices page).
3. Verify no-website with a web search before qualifying. Do not guess.
4. Dedupe against leads already found in earlier runs (keep the running list in `~/workspace/maps-leads/leads.md`, append-only, one line per business with date found).
5. Never contact anyone. Finding leads and writing templates is the whole job — Sky sends the messages himself.

## Outreach template rules (this is the core — every template must be different)

- **One unique message per business. Never reuse the same text.** Personalize with real observed details: business name, what they do, city, and one specific thing actually seen (a review quote, a photo, a rating, a service they offer, something customers ask about in reviews).
- **Structure (4 parts, short):**
  1. Personal hook, 1 line — proves you actually looked at them.
  2. The gap — what they are missing (no website / no online booking / customers cannot see prices, menu, or opening hours before visiting).
  3. The offer, 1 line — custom website / app / booking page built for them.
  4. One low-friction CTA — reply to the message, a quick call, or "want me to mock up a simple version so you can see it first?"
- **Tone:** human, short, plain words. No AI slop, no buzzword soup, no fake flattery, no em-dash stuffing. Sound like a person who found them on Maps, not a marketing agency.
- **Length:** 4-6 sentences max (under ~100 words) for email / DM; even shorter for WhatsApp.
- **Channel-matched:** pick the template form to the channel the business actually has:
  - Email available → email version, with a subject line.
  - Only Instagram → Instagram DM version.
  - Only phone → short WhatsApp version (or a 30-second call script if Sky prefers calling).
  - Only Facebook → Messenger version.
  - Several channels → write for the best one, and note the fallback channel.
- **Language:** English by default; local language for non-English countries when it can be written correctly.
- **Never invent facts.** No fake numbers, no fake competitor claims, no claims about what their customers do that reviews do not show. If a detail is unknown, leave it out.
- **Sign-off:** Sky / Restu — custom apps & websites (add portfolio link only if Sky provides one).

## Output format

Per run, deliver:

1. **Leads table** — one row per business: name, category, city/country, contacts found (email / phone / IG / FB), what is missing.
2. **One outreach block per business** — business name + channel + the full message, ready to copy-paste. Each block must read differently from the others.
3. **Save it** — append the leads and their templates to a dated file under `~/workspace/maps-leads/` so Sky can track who was already contacted and who was not.

## Example (shape only — never copy this text into a real template)

Lead: Fade Theory Barbershop, Austin TX, 4.9 stars (210 reviews), Instagram only, no website, no online booking.

> Hi, I found Fade Theory on Google Maps — 4.9 stars and the fade photos on your Instagram are clean. I noticed you don't have a website yet, so new customers can't see prices or book before walking in. I build custom websites and booking pages for local shops. Want me to mock up a simple one for Fade Theory so you can see it first? — Sky

## Hard rules

- Outside Indonesia only, no exceptions.
- No website = qualifies; a social profile is not a website.
- One message per business, always personalized, never templated-identical.
- Do not message, call, or email any business yourself. Sky sends.
- Do not contact the same business twice across runs — check the leads file first.
- Do not present an unverified contact (a guessed email, a wrong number) as real. If it cannot be verified from Maps / the business's own pages / search results, mark it unverified.
