# Ildi & Kostas — wedding guest site

Single-page static site served by GitHub Pages at <https://mylo91.github.io>.
No build step: edit `index.html`, commit, push to `main`, live in ~1 minute.

> The repo is public. Don't commit anything you wouldn't want public (bank details, phone numbers, private photos).
> The site is hidden from search engines (`noindex` + `robots.txt`), but anyone with the link can open it.

## Files

| Path | What |
|---|---|
| `index.html` | Everything: layout, styles, translations, map, recommendations |
| `images/` | Photos for recommendation cards |
| `robots.txt` | Keeps search engines out |

## Editing text

All wording lives in the `T` object near the bottom of `index.html`, one block per language (`en`, `hu`).
Change the text for the same key in both blocks.

**TBA items:** `activities.when13` and `activities.when15`. Replace "Time & place TBA…" with e.g. `18:00 · White Tower`.

## Recommendations

Defined in the `RECS` list in `index.html`. Each has an `id`, a category (`food` / `drinks` / `sights`, which sets the colour), an icon, text in both languages and one or more `places` with coordinates.
Places marked `est:true` have estimated coordinates. Check them on the map.

## Adding photos

Save the photo as `images/<id>.jpg`, using the recommendation's `id`:

`trigona` · `soutzoukakia` · `tiki-boat` · `promenade` · `profiterole` · `byzantio` · `gyros` · `bougatsa` · `meze` · `drinks`

If the file exists it replaces the icon tile automatically. Otherwise the icon stays.

**Resize before committing**: about 1200 px wide, under 300 KB. Phone photos are 4–8 MB and would make the site slow.
Easy options: [squoosh.app](https://squoosh.app) (drag in → resize to 1200 → MozJPEG ~75 → download), or on Windows *Photos → Resize image*.
Only use your own photos or freely licensed ones (Unsplash / Wikimedia Commons).

## Map

- `STAY_ZONE`: the corner points `[lat, lng]` of the shaded "where we'd stay" area. Right-click in Google Maps to copy coordinates for a point.
- `VENUE`: Kiwi Garden's coordinates.

## Deploying

GitHub → Settings → Pages → *Deploy from a branch* → `main` / `(root)`.
