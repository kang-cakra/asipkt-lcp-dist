# ASIPKT | LCP — Production Build

Repository ini berisi **hasil build production** dari aplikasi web **ASIPKT LCP**. Semua file di sini sudah siap deploy ke static hosting manapun.

> ⚠️ **Jangan mengedit kode langsung di repository ini.** Semua pengembangan dilakukan di source code terpisah, lalu build ulang dan salin hasilnya ke sini.

## Tech Stack

- Vite (build tool)
- Progressive Web App (PWA) — service worker & web app manifest
- Asset hashed untuk caching optimal

## Deployment

Upload seluruh isi folder ini ke salah satu layanan hosting statis berikut:

- **GitHub Pages**
- **Vercel**
- **Netlify**
- **Nginx / Apache**
- Cloudflare Pages, dsb.

File `_redirects` sudah disertakan untuk kebutuhan SPA routing (Netlify/Cloudflare Pages).

## Menjalankan Local (Preview)

```bash
# contoh dengan Python
python -m http.server 8080

# contoh dengan Node
npx serve .
```

Lalu buka `http://localhost:8080`.

## Struktur File

| File/Folder | Keterangan |
| --- | --- |
| `index.html` | Entry point aplikasi |
| `assets/` | JS & CSS hasil build (hashed) |
| `sw.js` | Service worker |
| `registerSW.js` | Registrasi service worker |
| `manifest.webmanifest` | Konfigurasi PWA |
| `_redirects` | Aturan redirect SPA |
| `version.json` | Versi build |

## Update Build

Cukup hapus isi lama (kecuali `.git`), lalu salin hasil build terbaru ke folder ini, kemudian:

```bash
git add -A
git commit -m "build: update production assets"
git push
```
