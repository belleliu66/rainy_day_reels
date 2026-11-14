# Rainy Day Reels

Portfolio website for Rainy Day Reels (videography, photography and editing).

## How it's built
- Plain static site: HTML pages plus one shared `styles.css`. No build step, no packages.
- Hosted on **Cloudflare Pages**, deployed automatically from the `main` branch on GitHub. Anything pushed to `main` goes live. Every file in the repo is published, so don't commit private notes.
- Videos and images are stored in **Cloudflare R2** and linked by their public URL:
  `https://pub-b90a8e956c8f4cb28ee9d0205af29830.r2.dev/<filename>` (encode spaces as `%20`).

## Pages
| File | Content |
|---|---|
| `index.html` | Home: video carousel, About intro, Portfolio grid, Services & Contact |
| `about.html` | Full About page |
| `portfolio.html` | Portfolio by category, with links to sample videos |
| `artwork.html`, `services.html`, `contact.html` | Redirects kept for old links (to the Portfolio page and the Services & Contact section) |

Fonts are in `fonts/`: **French** for the wordmark and page titles, **Indonesian** for section headings.

## Adding media
1. Export a short web clip: H.264 `.mp4`, up to 1080p, about 10 seconds, under ~15 MB, audio removed. Other codecs (MPEG-4 Part 2, HEVC, ProRes) show as blank tiles in most browsers.
2. Upload it to the R2 bucket.
3. Reference its R2 URL in the HTML. Never link to local files; they aren't deployed.

## Preview locally
```
python3 -m http.server 8000
```
Then open http://localhost:8000/ and check desktop and mobile widths (the layout changes at 900px and 600px).
