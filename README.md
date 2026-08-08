# burioworks studio website

The GitHub Pages site for `burioworks`, an independent software studio creating apps, tools, and games.

- Public site: <https://burioworks.github.io/>
- Banso legal pages: <https://burioworks.github.io/banso-legal/>
- AdMob seller declaration: <https://burioworks.github.io/app-ads.txt>

## Site structure

```text
.
├── index.html
├── styles.css
├── favicon.ico
├── favicon.png
├── app-ads.txt
├── README.md
├── assets/
│   ├── brand/
│   │   ├── burioworks-mark-vector.svg
│   │   └── burioworks-horizontal-lockup-vector.svg
│   └── products/
│       ├── banso/
│       │   └── banso-archive.webp
│       └── roblox/
│           ├── scrap-world.webp
│           └── neko-shelter.webp
├── finallook/
│   ├── index.html
│   ├── privacy-policy.html
│   ├── terms-of-service.html
│   └── support.html
└── banso-legal/
    └── existing Banso legal pages and assets
```

The Home page is a single-page studio overview. FinalLook has a short product page plus product-specific Privacy Policy, Terms of Service, and Support routes.

## Development model

The site is static HTML and CSS with no build step, framework, CMS, backend, analytics, cookies, or JavaScript. Run any local static HTTP server from the repository root to preview route behavior.

GitHub Pages continues to publish from `main / root`:

```text
Settings
└── Pages
    ├── Source: Deploy from a branch
    ├── Branch: main
    └── Folder: / (root)
```

Product-specific images, destination URLs, and document content are intentionally isolated and replaceable. Search for `TODO:` in the HTML to find pending content without changing the page layouts.

Only optimized production images referenced by the published pages belong in `assets/products/`. Original working images and unused exports stay outside the public repository.

The public repository keeps only the production brand assets used by the site:

- `assets/brand/burioworks-mark-vector.svg`
- `assets/brand/burioworks-horizontal-lockup-vector.svg`
- `favicon.ico`
- `favicon.png`

The SVG files are the approved path-based mark and horizontal lockup. Do not redraw or transform their geometry. Brand source material, references, documentation, alternate exports, and unused variants are intentionally excluded from the public repository.

## Production files that must be preserved

`banso-legal/` contains the existing Banso legal site. Its files and public URLs must remain unchanged.

`app-ads.txt` contains the production AdMob seller declaration. Do not alter, reformat, or add comments to this file. Only the exact seller declaration from the AdMob management screen should be present.

## Custom domain

The custom-domain and DNS cutover are pending and intentionally separate from this site implementation. Do not add or modify `CNAME` until that work is approved.
