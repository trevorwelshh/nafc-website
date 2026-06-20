# Not A Film Camera — Website

Static marketing site + legal pages for the [Not A Film Camera](https://apps.apple.com/app/apple-store/id6468926207) iOS app.

Plain HTML/CSS — no build step.

## Structure

```
index.html      Landing page (App Store link)
privacy.html    Privacy Policy
terms.html      Terms of Service
404.html        Not-found page
styles.css      Shared styles
robots.txt
sitemap.xml
```

## Local preview

Open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (Cloudflare Pages)

1. Push this repo to GitHub.
2. In the Cloudflare dashboard: **Workers & Pages → Create → Pages → Connect to Git**, and pick this repo.
3. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
4. Deploy. Then add the custom domain **notafilmcamera.com** under the project's **Custom domains** tab (Cloudflare will set the DNS records automatically if the domain is on your Cloudflare account).

Every push to the default branch redeploys automatically.

## Notes

- The legal pages reflect the app's current behavior (on-device storage, Apple in-app purchases, no third-party analytics/tracking). **Review them before publishing** and adjust to your situation.
- App Store links use `ct=website` for attribution.
