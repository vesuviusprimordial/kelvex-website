# Kelvex Heating & Air — website

Static HTML site. No build step, no dependencies.

## Deploy to Vercel
1. Put these files in a GitHub repo (root level, not in a subfolder).
2. Vercel → Add New → Project → import the repo.
3. Framework preset: **Other**. Leave build command and output directory empty.
4. Deploy, then add the domain `kelvexhvac.com` under Project → Settings → Domains.

Any static host works the same way (Netlify, Cloudflare Pages, GitHub Pages).

## Files — ALL AT ROOT LEVEL, NO FOLDERS

Upload every file in this folder to the repo root. There is no assets folder.

HTML: index, services, maintenance, pricing, about, contact, terms, privacy
Other: styles.css, sitemap.xml, robots.txt
Images: logo-horizontal.png, logo-horizontal-white.png, logo-stacked.png,
        icon.png, favicon-16.png, favicon-32.png, favicon.ico, apple-touch-icon.png

Do NOT upload any PREVIEW-*.png files — those are screenshots, not part of the site.

## Before going live — must do

### 1. Activate the contact form (5 minutes)
The form posts to Web3Forms but needs your key:
1. Go to https://web3forms.com — enter michael@kelvexhvac.com, no account needed.
2. They email you an Access Key.
3. In `contact.html`, find `REPLACE_WITH_YOUR_WEB3FORMS_KEY` and paste your key in its place.
4. Submit a test message from the live site and confirm it lands in your inbox.

Free tier covers 250 submissions/month. Submissions arrive as email — nothing is stored on the site.

### 2. Confirm the published rates
`pricing.html` now lists concrete rates ($149 diagnostic, $125/hr standard, $185/hr after-hours,
maintenance and winterization from $165/unit). **Change these to your real numbers before launch.**
Stripe requires visible pricing; these are placeholders based on Denver light-commercial norms.

### 3. Verify business details
Address, phone, and hours appear in the footer of every page and in the schema block in `index.html`.

## SEO notes
- Every page has a unique title, meta description, and canonical URL.
- `index.html` contains HVACBusiness + FAQPage structured data. Test at search.google.com/test/rich-results
- After deploying: submit the sitemap in Google Search Console.
- **Local ranking comes from your Google Business Profile, not this site.** Claim it, use the exact
  name/address/phone shown here, and collect reviews. That matters more than anything on these pages.
