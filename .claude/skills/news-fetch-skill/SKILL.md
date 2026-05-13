# news-fetch Skill

> Showcase version — abbreviated skill spec.

## Purpose

Harvest daily tech hotspots from GitHub Trending, X/Twitter KOLs, and official tech blogs into a structured intel digest.

## Inputs

- `sources` (list) — which sources to query
- `min_score` (int) — minimum engagement threshold
- `output_path` (str) — where to write the digest

## Output

A markdown digest at `content_library/intel/YYYY-MM-DD.md` with:

```
## 🔥 Top Picks
- [title](url) · score · 1-line summary

## 🧪 Emerging
- ...
```

## Notes
- Full prompt logic, dedup strategy and KOL list not included in showcase version.
