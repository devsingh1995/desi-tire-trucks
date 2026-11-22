# Desi Tire And Parts Inc. website

Four responsive pages: `index.html`, `about.html`, `services.html`, `contact.html`.

## Preview
Open `index.html` in a browser, or run `python -m http.server 8000` from this folder and visit `http://localhost:8000`.

## Deployment
Upload all files and the `assets/` folder to any static host (Netlify, Cloudflare Pages, GitHub Pages, cPanel/Hostinger static hosting). Configure your domain and HTTPS.

## Important
- The contact form opens a pre-addressed email in the visitor's installed email app. It does **not** send messages through a server. To collect submissions directly, integrate a hosted form service or backend.
- Telephone links use the two numbers you supplied. No physical office address or unverified service guarantees are invented.
- Replace relative Open Graph image with an absolute URL once you have a domain. Add canonical links and `url` field in schema after the domain is set.
- For privacy compliance, review any analytics/cookies and add a privacy policy if collecting personal information through a future online form.
- Fonts load from Google Fonts; fallback fonts are included.
- The supplied logo retains its light background; a transparent source can replace it later.

## Instagram section on homepage
The homepage has an Instagram-themed five-image gallery using the company's supplied photos, with live links to https://www.instagram.com/desi_truck_trailer_tires/. These are **not represented as the latest Instagram posts**.

To display specific Instagram posts/reels, edit `assets/script.js` and add up to five **public post URLs** in the `INSTAGRAM_POST_URLS` array. The homepage will show their Instagram embeds automatically, each with a working link to the original post. Example:

```js
const INSTAGRAM_POST_URLS = [
  'https://www.instagram.com/reel/EXAMPLE_POST_CODE/',
  'https://www.instagram.com/p/EXAMPLE_POST_CODE/'
];
```

Instagram's public profile cannot reliably be scraped for the newest five posts on a static website. To update automatically whenever the account publishes, use an approved Instagram API integration or a reputable hosted Instagram feed widget. Instagram itself controls whether individual post embeds load in a visitor's browser.


### Instagram reels (homepage)
The homepage now contains five **hand-selected** public Instagram reel embeds using Instagram's official embed.js script, plus direct links that work if embeds are blocked. This is not an automatically updating latest-five feed. To change reels, edit the `data-instgrm-permalink` and companion links within the `instagram-reels` section in `index.html`. The first supplied reel credits @arsh_damesha_official rather than the company account; it was included exactly as supplied. Instagram can block embeds in restrictive browser settings or require sign-in.
