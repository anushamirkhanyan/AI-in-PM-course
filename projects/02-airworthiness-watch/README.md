# Airworthiness Watch

A personal aviation intelligence briefing board that curates and tracks Airworthiness Directives (ADs), notable incidents, regulatory changes, and aviation history.

## What it is

- **Static HTML briefing board** — no backend, no build steps
- **Multi-feed design** — separate sections for ADs, incidents, regulations, and "on this day" history
- **Filterable by category** — view all entries, or drill down by type
- **Curated reference** — grows over time as new entries are added
- **Aviation enthusiast-friendly** — styled like a real intelligence briefing, with Boca Juniors colors (blue & yellow)

## How to use

### View the page

Open `index.html` directly in your browser or share the GitHub raw link.

### Add a new entry

Use the `/add-airworthiness-entry` skill:

```
I want to add: "EASA issued an AD on the CFM56 fan blade inspection interval, effective next month"
```

The skill will:
1. Classify the entry (AD, Incident, or Regulation)
2. Extract key fields (authority, aircraft/system, date, summary)
3. Return formatted JSON
4. Tell you where to paste it in `index.html`

### Edit manually

Open `index.html` and find the `entries` array in the `<script>` tag. Add a new object:

```javascript
{
  id: 7,
  type: "ad",
  icon: "📋",
  title: "Inspection Requirements for XYZ Component",
  aircraft: "Airbus A350",
  authority: "EASA",
  date: "2025-02-20",
  summary: "New mandatory inspection procedure effective immediately.",
}
```

Then save and refresh.

## Entry types

- **AD** — Airworthiness Directive from FAA/EASA
- **Incident** — notable accident, incident, or safety event
- **Regulation** — regulatory change, amendment, or new rule

## Feeds

1. **Airworthiness Directives** — FAA/EASA compliance requirements
2. **Notable Incidents** — factual summaries of accidents and safety events
3. **Regulation Watch** — changes to Part 21/25, CS-23, etc.
4. **On This Day** — aviation history rotator (picks random or today's date match)

## Course learning goals

This project teaches:
- Data classification and structured entry in PM workflows
- How skills can parse natural language into structured data
- Curating and maintaining growing reference documents
- Styling and filtering for different data types
- Building reference tools that serve as team knowledge bases

## Notes

- The page filters by entry type with buttons at the top
- Aviation history entries are pre-populated; new ones can be added to the array
- Colors follow Boca Juniors (blue #003087 + yellow #FFD700) for a distinctive briefing aesthetic
- Each entry shows authority, aircraft/system affected, and effective date for quick reference
