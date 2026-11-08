# website
website-alberto-bonino

## Assets

Photos are WebP, exported with the grain-preserving settings (long edge 3000px, quality 86).

| Folder | Contents |
|---|---|
| `assets/images/cover/` | Full-screen cover / homepage hero images |
| `assets/images/projects/` | One subfolder per series, e.g. `projects/surf/`, `projects/architecture/` |
| `assets/images/about/` | Portrait and images for the About page |
| `assets/logo/` | The "ab" logo (SVG preferred) |

File naming: lowercase, hyphens, no spaces, numbered in display order — e.g. `projects/surf/surf-01.webp`.

## Site

`index.html` is the whole site. Photos and their collections come from `assets/data/photos.js`,
which is generated — don't edit it by hand. After adding/removing photos, or after editing
`assets/data/collections.json` (which photo belongs to which collection), run:

```bash
python3 tools/build-manifest.py
```

- Black & white photos: `assets/images/projects/black-and-white/`
- Colour photos: `assets/images/projects/colors/`
- Files listed in `HIDDEN` inside the script stay in the repo but are left off the site.
