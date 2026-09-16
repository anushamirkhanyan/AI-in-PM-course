---
name: add-travel-entry
description: Parse a natural language travel entry ("Buenos Aires, want to go for Usuai, the end of the world, asado, empanadas and alfajores, still dreaming") and format it as a structured card entry with place, country, why, and status — ready to add to the bucket list.
---

# Add Travel Entry

Convert casual, natural language travel notes into a clean, structured entry for
the bucket list.

## Steps

1. The user provides a travel entry in casual language, e.g.:
   - "Tokyo, cherry blossoms and ramen, been there"
   - "Iceland, Northern lights and hot springs, booked a trip"
   - "Bali, temples and beaches, still dreaming"

2. Parse the entry and extract:
   - **Place** — the main location/city
   - **Country** — infer from context or ask if unclear
   - **Why** — a one-liner about what they want to do or why it matters
   - **Status** — one of:
     - `dreaming` — want to go someday
     - `booked` — have a trip planned/booked
     - `been` — have already visited

3. Format it as a JSON object:
   ```json
   {
     "id": [next_available_id],
     "place": "Place Name",
     "country": "Country",
     "why": "One-line reason or what excites you",
     "status": "dreaming|booked|been",
     "color": "#[hex color based on status]"
   }
   ```

4. Color hints by status:
   - **dreaming** → use purples/pinks (`#c084fc`, `#f472b6`, `#e879f9`)
   - **booked** → use warm oranges/reds (`#fb923c`, `#f97316`, `#f5576c`)
   - **been** → use cool cyans/blues (`#22d3ee`, `#06b6d4`, `#0ea5e9`)

5. Provide the user with:
   - The formatted JSON entry
   - Instructions on where to add it in `index.html` (into the `travels` array)
   - A preview of how it will look on the page
