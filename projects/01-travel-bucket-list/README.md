# Travel Bucket List

A static, shareable webpage that displays your travel dreams, booked trips, and
places you've been — with filterable status categories.

## What it is

- **Static HTML** — no backend, no build steps, just open `index.html` in a
  browser or share the GitHub link
- **Interactive** — filter by status (Dreaming / Booked / Been), hover effects,
  responsive design
- **Easy to update** — add new entries by editing the `travels` array in the
  HTML with structured JSON

## How to use

### View the page

Open `index.html` directly in your browser, or share the raw GitHub link:

```
https://raw.githubusercontent.com/anushamirkhanyan/AI-in-PM-course/main/projects/01-travel-bucket-list/index.html
```

(Once pushed, GitHub will serve it live.)

### Add a new entry

Use the `/add-travel-entry` skill:

```
I want to add: "Barcelona, Gaudí architecture and tapas, been there"
```

The skill will:
1. Parse your entry
2. Return a formatted JSON entry
3. Tell you where to paste it in `index.html`

### Edit manually

Open `index.html` and find the `travels` array in the `<script>` tag. Add a new
object:

```javascript
{
  id: 6,
  place: "Barcelona",
  country: "Spain",
  why: "Gaudí architecture and tapas",
  status: "been",
  color: "#06b6d4"
}
```

Then save and refresh the browser.

## Statuses

- **Dreaming** — want to go someday
- **Booked** — have a trip planned or booked
- **Been** — have already visited

## Tips

- Keep the "why" to one line — it shows on the card as a quote
- Pick a hex color that matches the status (see `/add-travel-entry` for hints)
- Increment the `id` by 1 for each new entry
- The page filters by status with buttons at the top

## Course learning goals

This project teaches:
- Static HTML pages as deployable artifacts (no server needed)
- How a skill can help format and structure data
- Git workflow for sharing homework via GitHub links
- Simple data management in front-end code
