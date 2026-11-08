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

`index.html` is the whole site (based on the Claude prototype). The B&W grid is built
automatically from `assets/data/photos.js`. After adding or removing photos, regenerate it:

```bash
python3 tools/build-manifest.py
```

Files listed in `HIDDEN` inside that script stay in the repo but are left off the site.
`assets/images/prototype-color/` holds the four test colour photos from the prototype until
the real colour set is uploaded.
