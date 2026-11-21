# Faisal Virjee: personal website

A single-page site. No build step, no framework, no tracking.

```
index.html                       the whole site (HTML, CSS, JS)
assets/faisal.jpg                headshot
assets/Faisal-Virjee-Resume.pdf  résumé with no phone number
.nojekyll                        tells GitHub Pages to serve files as-is
```

## Put it on GitHub Pages

1. Sign in to **github.com with your personal account**. Do not use a Cox GitHub Enterprise account for this.
2. Create a new public repository (for example `faisalvirjee.com`).
3. Upload everything in this folder to the repository root. Keep `index.html` at the top level and keep the `assets` folder.
4. Open **Settings → Pages**. Under "Build and deployment," choose **Deploy from a branch**, pick `main` and `/ (root)`, then save.
5. After a minute the site is live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

## Point your domain at it

1. Register the domain anywhere.
2. In **Settings → Pages → Custom domain**, enter your domain (for example `faisalvirjee.com`) and save. GitHub adds a `CNAME` file to the repository for you.
3. At your registrar's DNS settings:
   - Add four **A records** for the apex domain (`@`) pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`.
   - Add a **CNAME record** for `www` pointing to `YOUR-USERNAME.github.io`.
   - Check these addresses against GitHub's current "Managing a custom domain" documentation before you rely on them.
4. When DNS finishes updating (minutes to a few hours), tick **Enforce HTTPS** in Settings → Pages.

## After the domain is live

- In `index.html`, uncomment the `canonical` line near the top and set your domain.
- Change `og:image` to the full URL (`https://YOURDOMAIN.com/assets/faisal.jpg`) so link previews show your photo.
- Add the site link to your LinkedIn Featured section.

## Editing

- **Facts and numbers:** search `index.html` for the section you want. Every section is plain HTML.
- **Off the clock:** the four facets are drafts. Delete any block inside the `facets` section that you would rather not publish.
- **Colors and fonts:** all of them live in the `:root` block at the top of the `<style>` tag.
- **Email address:** it is assembled in the script at the bottom of the file so scrapers do not harvest it. Change it there.

## Before you publish

- Confirm the VDI baseline (~250 users in 2021) uses the same basis as today's ~3,000.
- Decide whether the résumé PDF should be public. It lists your employer, titles, and dates but not your phone number.
- Check with your employer's communications or social-media policy about publishing performance numbers.
