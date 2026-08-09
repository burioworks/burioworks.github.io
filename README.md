# burioworks studio website

The GitHub Pages site for `burioworks`, an independent software studio creating apps, tools, and games.

- Public site: <https://burioworks.com/>
- Yoin Privacy Policy: <https://burioworks.com/yoin/privacy/>
- Banso legal pages: <https://burioworks.com/banso-legal/>
- AdMob seller declaration: <https://burioworks.com/app-ads.txt>

## Site structure

```text
.
├── CNAME
├── index.html
├── styles.css
├── favicon.ico
├── favicon.png
├── robots.txt
├── sitemap.xml
├── app-ads.txt
├── README.md
├── assets/
│   ├── brand/
│   │   ├── burioworks-mark-vector.svg
│   │   └── burioworks-horizontal-lockup-vector.svg
│   └── products/
│       ├── banso/
│       │   └── banso-archive.webp
│       ├── roblox/
│       │   ├── scrap-world.webp
│       │   └── neko-shelter.webp
│       └── yoin/
│           ├── yoin-product-hero_1280x840.png
│           ├── yoin_feature_graphic_1024x500.png
│           └── yoin_icon_full_512.png
├── en/
│   ├── index.html
│   └── finallook/
│       ├── index.html
│       ├── privacy-policy.html
│       ├── terms-of-service.html
│       └── support.html
├── finallook/
│   ├── index.html
│   ├── privacy-policy.html
│   ├── terms-of-service.html
│   └── support.html
├── yoin/
│   ├── index.html
│   └── privacy/
│       └── index.html
└── banso-legal/
    └── existing Banso legal pages and assets
```

The Japanese-primary Home at `/` and English Home at `/en/` share the same structure and stylesheet, with explicit language links between them. Yoin has a Japanese-primary product page at `/yoin/` and a published Privacy Policy at `/yoin/privacy/`.

FinalLook remains visible as a project card but is intentionally not linked from Home while its public product assets and documents are incomplete. Japanese FinalLook routes live under `/finallook/`; their English equivalents mirror them under `/en/finallook/`. Each corresponding page has an explicit language link. All FinalLook product and document routes carry `noindex,nofollow,noarchive` and are excluded from `sitemap.xml` until release-ready.

## Development model

The site is static HTML and CSS with no build step, framework, CMS, backend, analytics, cookies, or JavaScript. Run any local static HTTP server from the repository root to preview route behavior.

GitHub Pages publishes from `main / root`:

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

## Custom domain and SEO

The canonical production origin is `https://burioworks.com/`. The branch publishing source keeps `CNAME` at the repository root with `burioworks.com`.

Publicly indexable routes are listed in `sitemap.xml`. `robots.txt` points crawlers to that sitemap. Home language variants use canonical and hreflang metadata on the custom domain, and Yoin uses canonical/Open Graph metadata on the custom domain.

After a custom-domain change, verify the domain under `Settings → Pages` and enable `Enforce HTTPS` once GitHub makes the option available.
