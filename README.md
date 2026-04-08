# Portfolio Site (Cloudflare Pages)

A full-screen banner scroll portfolio template hosted on **Cloudflare Pages** with media served from **Cloudflare R2** (free tier).

## 📦 What’s Included
- `index.html`: full-screen banner layout with hover menu and scroll sections
- `styles.css`: styling for banners, menu, and animations
- `about.html`, `artwork.html`, `services.html`, `contact.html`: linked pages
- `media/`: placeholder images for upload to R2

## ✅ How to Use
1. **Create a GitHub repository** and commit this folder.
2. **Deploy with Cloudflare Pages**:
   - In Cloudflare Dashboard → **Pages** → Create project
   - Connect your GitHub repo
   - Set **Build command** empty and **Build output directory** to `.`
3. **Upload media to R2**:
   - Bucket name: `media`
   - Upload files from `media/` folder (e.g., `hero-poster.png`)
   - URLs will be: `https://173125ae54d69c4ba4e9f4992609de84.r2.cloudflarestorage.com/media/filename.png`
4. **Replace placeholder content** in HTML files with your own text/images.

## 🔄 Updating Your Portfolio
- Edit `index.html` for banner content and links.
- Add real images/videos to R2 bucket `media` and update URLs.
- Each photo is an `<img>` block; each video is a `<video>` or embedded `<iframe>`.

## 📌 Notes
- For best performance, keep images and videos reasonably sized (resize offline before uploading).
- Cloudflare Pages serves the HTML/CSS; Cloudflare R2 stores your large media assets.
