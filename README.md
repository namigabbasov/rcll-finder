# RCLL Database Finder

An interactive legal database navigator for the Robert Crown Law Library at Stanford Law School.

## Features

- **Guided paths** — navigate by topic or source type to get curated database recommendations
- **Browse all** — search and filter 100+ databases by name, category, or access type
- **AI search** — coming soon

## Structure

```
rcll-finder/
├── index.html      # The entire app — self-contained, no dependencies
└── README.md
```

## Local development

Just open `index.html` in a browser. No build step, no dependencies.

```bash
open index.html        # macOS
start index.html       # Windows
xdg-open index.html   # Linux
```

Or use VS Code's Live Server extension for auto-reload on save.

## Deploy

Deployed via Netlify. Push to `main` branch to trigger a new deploy.

- **Publish directory:** `/` (root)
- **Build command:** (none)
- **Build directory:** (none)

## Data

All database entries and URLs are in the `DBS` array in `index.html`. To add or update a database, find the array and add an entry with:

```js
{ 
  n: "Database Name",       // display name
  c: "Category",            // browse category
  url: "https://...",       // actual link
  ac: [],                   // access flags: "sls", "pw", "ai"
  d: "Short description."   // one sentence
}
```

To add a database to a guided path, find the relevant path in the `TOPIC` or `SOURCE` arrays and add the name to the `dbs` array.

## Contact

Reference librarians: reference@law.stanford.edu · 650 725.0800
