---
name: add-airworthiness-entry
description: Parse aviation intelligence notes (ADs, incidents, reg changes) and format them as structured entries for the Airworthiness Watch page — extracting key fields like authority, aircraft/system, effective date, and classification.
---

# Add Airworthiness Entry

Convert rough aviation intelligence notes into clean, structured entries for the Airworthiness Watch briefing board.

## Steps

1. The user provides an aviation note in casual language, e.g.:
   - "EASA issued an AD on the CFM56 fan blade inspection interval, effective next month"
   - "Boeing 737 MAX 8 crash in Ethiopia, structural failure investigation ongoing"
   - "FAA Part 21 amendment changes certification procedures for electric aircraft"

2. Classify the entry type:
   - **AD** — Airworthiness Directive (FAA/EASA)
   - **Incident** — accident, incident, or safety event with factual summary
   - **Regulation** — regulatory change or amendment (Part 21/25, CS/FAR, etc.)

3. Extract and parse:
   - **Authority** — FAA, EASA, NTSB, etc.
   - **Aircraft/System** — what's affected (e.g., "Boeing 737 MAX", "CFM56 fan blade")
   - **Effective Date** — when it takes effect (or date of event)
   - **Summary** — one-line reason or what it means
   - **Source** — where it came from (regulatory body, news outlet, etc.)

4. Format as JSON object:
   ```json
   {
     "id": [next_available_id],
     "type": "ad|incident|regulation",
     "title": "Short title",
     "aircraft": "Aircraft or system affected",
     "authority": "FAA|EASA|NTSB|etc",
     "date": "YYYY-MM-DD",
     "summary": "One-line factual summary",
     "icon": "📋|⚠️|📜"
   }
   ```

5. Provide:
   - The formatted JSON entry
   - Where to add it in `index.html` (into the appropriate `entries` array by type)
   - A preview of how it will appear on the page
