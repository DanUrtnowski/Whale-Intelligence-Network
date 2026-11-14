# Whale Intelligence Network — public milestone record

Publicly reportable milestones only. Internal review material stays private.

## 2026-11-14 — Plain-language copy

- Home headings are plain labels instead of essayistic ones (e.g. “Four streams, one timeline”).
- Sources methodology essays collapse into five expandable panels, keeping the health table
  above the fold.
- Footer drops the duplicated stream list for a single line of four links.

## 2026-11-14 — QA fixes

- Sources table crash fixed: source health is merged onto the edition list instead of read from
  the status payload, which carries health only.
- Ocean Explorer renders again: the map painted only inside requestAnimationFrame, which
  background and headless browsers defer, so it now paints its first frame synchronously and
  keeps a timer fallback.
- News excludes shared-name false positives (Orca Security, ORCA Computing, Blue Whale-2026
  exercise, Dune costumes) and de-duplicates syndicated headlines.
- Conservation publishes one record per destination instead of nine titles on one NOAA page.
- Escape closes the mobile menu; the home stat reads “Edition records”.

## 2026-11-14 — News lane readability

- The News lane is grouped into topic sections (right whales, blue whales, humpbacks, orcas,
  ship strikes, entanglement, strandings, vaquita, other whales, conservation).
- Added a source filter and 30-headline pages instead of one 450-item column.
- Headline search now narrows the lane across every topic group and source.
- Removed headlines that only shared a name with a cetacean: Orcas Island ferry news, wetsuits
  and keyboard reviews from the orca query.

## 2026-11-13 — Feed curation

- Measured every news feed's actual yield and retired the five that produced no cetacean items.
- Replaced them with twelve Google News topic queries and a Guardian marine-life feed; the News
  lane now carries 450 records from 17 feeds.
- Added exclusion rules for headlines that share a name with another industry, cross-feed
  duplicate suppression, and per-stream publish limits.

## 2026-11-13 — Data expansion: News lane and Whale Atlas

- Live at the project's own address, verified over public HTTPS.
- A **News** lane with twelve independent open feeds — Google News topic queries plus Oceana,
  Woods Hole, Mongabay, Hakai, the New England Aquarium, NOAA, ScienceDaily, Pacific Whale
  Foundation and Cascadia Research — publishing headline, publisher and link only.
- **arXiv** preprints added to the Research lane, labelled as not yet peer reviewed.
- A **Whale Atlas**: historical cetacean records from OBIS, licence-filtered to CC0 and CC BY,
  aggregated into 1° cells of about 111 km with species-group and period filters. The site
  receives aggregated cells, never an individual position.
- Explainer copy trimmed throughout.

## 2026-11-13 — Three sourced streams published

- Live site with three independent, real streams: **Research** (Crossref REST API),
  **Conservation** (NOAA Fisheries North Atlantic right whale health updates) and
  **Policy & Notices** (Federal Register API, NOAA/NMFS cetacean documents).
- Every record carries its source, canonical link, the source's publication date and
  the date it was first seen. Research records resolve through their DOI; policy
  records distinguish proposed rules, final rules and notices; a deadline appears only
  when the source supplies one.
- A source registry with per-source enable switches, polling intervals, rights
  declarations and health status, so a fourth connector does not require changes to the
  scheduler, the publisher or the feed layout.
- Versioned publishing: a complete edition snapshot is written before the pointer moves,
  the previous good edition is retained, and corrections are kept as revisions.
- Safety gate: records that could reveal a recent or sensitive animal location, unclear
  rights or unclear identity are held in a private review queue instead of published.
- Last successful source check is reported separately from last content change; a
  stopped collector leaves the last good edition online with a visible age.
- The Ocean Explorer returns with species, date and layer filters and on-click
  provenance. Its synthetic data sits in a labelled **Illustrative Demo** layer that is
  off by default and excluded from live counts.
- A Sources & Methodology page documents every endpoint, cadence, republished field and
  the limits of the map.

### Stated limitations

- Snapshot storage is blocked on billing activation, so the public site currently serves
  the most recent complete edition bundled at build time.
- The dedicated public address is being moved to its own hostname; until that DNS record
  exists the site is served from its Cloudflare Pages address.
- The individual-whale registry is not cleared for public release and is not published.
- No population figures, no animal positions, no social accounts.

## 2026-11-03 — Public showcase established

- Public project description published, separating proposed capabilities from
  established facts.
- Confirmed in public that a contributor's editorial content, voice, likeness and
  personal material remain under that person's approval and are not published.

## 2026-10-31 — Concept preview and reviewer walkthrough

- A working concept preview built to let a subject-matter reviewer judge scope,
  visual identity, content structure and the mapping explorer before any
  organisation, account or real dataset exists.
- A verification guard that refuses a corroborated status without a named human,
  a check date and two distinct origins.
- A spatial explorer with layered records, provenance on selection and buffer
  analysis, built without a heavy map dependency.
- All demonstration content labelled as demonstration content; no external links
  presented as citations, because attributing fabricated material to a real
  publisher would be worse than having no citation.
