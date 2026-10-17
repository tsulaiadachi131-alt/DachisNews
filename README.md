# The Daily Brief

A magazine-style static news reading site. Open `index.html` in a browser. It needs no build step and uses no third-party news service.

## Public site

Visit the live site at https://tsulaiadachi131-alt.github.io/DachisNews/ . The GitHub Pages site publishes from the `main` branch, so updates to the site files are published automatically.

## Daily updates

A daily refresh is active in Codex. Each run updates the local `data.js` and the public repository's `data.js` from approved outlets only, with direct original-article links, priority rankings, and a rolling 14-day archive. GitHub Pages republishes the site after the repository update. The page displays the edition's last-updated date.

To update the site manually, edit `data.js` and add or replace story objects in `window.BRIEFING_STORIES`. Each story needs:

- `priority`: editorial importance rank; `1` appears first
- `title`: headline
- `summary`: concise, accurate description based on the linked article
- `category`: primary category: `Economics`, `Politics`, `Education`, `War`, or `Protest`
- `alsoCategories`: optional additional categories when a story clearly belongs in more than one section
- `region`: `Czechia`, `Georgia`, `EU`, or `USA`
- `source`: publisher name from the approved list
- `date`: publication date as `YYYY-MM-DD`
- `url`: direct link to the original article

Keep `window.BRIEFING_SOURCES` limited to the requested publications. Do not use other outlets, aggregators, or homepage links as story sources.
