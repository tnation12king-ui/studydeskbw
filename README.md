# Study Desk website

Study notes, past papers and worked practice for Botswana university students.

This folder is the whole website. It is a static site (HTML plus JSON data), so it runs on any free static host. There is no server, database or build step.

## What's in the folder

| File | What it is |
|---|---|
| `index.html` | The whole site: home page, course pages, notes reader, practice, mock exams and the sign-up lock |
| `data/*.json` | One file per course with its notes, questions and mock exams |
| `favicon.svg`, `apple-touch-icon.png` | Browser and phone home-screen icons |
| `og.jpg` | The preview image shown when the link is shared on WhatsApp, Facebook or X |
| `404.html` | The page shown for a wrong link |
| `robots.txt`, `sitemap.xml` | Help Google find the site (replace `YOUR-DOMAIN` first) |
| `netlify.toml` | Settings for Netlify (ignored by other hosts) |

## Put it online with Netlify (free, about 5 minutes)

1. Create a free account at netlify.com.
2. On the Sites page, choose **Add new site → Deploy manually**.
3. Drag this whole folder onto the page. Netlify gives you a link such as `studydesk-bw.netlify.app`.
4. Open the link and check that the sign-up lock, a course page, its notes and a practice round all work.

Other free hosts work the same way: Vercel (drag and drop or GitHub import), Cloudflare Pages, or GitHub Pages (upload the files to a repository and turn on Pages).

## Use your own domain

1. Buy a domain, e.g. `studydesk.co.bw` from a `.co.bw` registrar, or a `.com` from Namecheap or Cloudflare.
2. In Netlify: **Domain management → Add a domain**, then follow the DNS steps it shows. HTTPS is switched on for you.
3. In `robots.txt` and `sitemap.xml`, replace `YOUR-DOMAIN` with your domain and upload the folder again.

## Updating content

Each course's notes and questions live in `data/<course>.json`. To update a course, replace that file and upload the folder again (Netlify: **Deploys → drag the folder**). The question and topic totals shown on the home page are in the `COUNTS` line near the top of the main script in `index.html`.

## Before you promote it widely

- **Past papers and lecture content.** The notes are written from lecture slides and the questions include past exam papers. Universities usually own the copyright in their papers and slides, so check with UB (or get permission) before charging for access or advertising heavily.
- **The sign-up lock** sends each visitor's name, email and visit time to your Google Form. Keep the "What happens to your details" note on the lock accurate if you change that.
- **Four CHE 101 cards** (the practice test, hydrate lab, revision video and draft notes) still link to pages on claude.ai. Move them into this site, or make sure those pages are shared publicly, before launch.
