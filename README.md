# Kasoko Travels Website

A professional one-file travel website for Kasoko Travels, ready for GitHub and Vercel.

## Files

- `index.html` - the full website
- `README.md` - setup notes

## Test locally

Open `index.html` in your browser. Test the menu, language switch, display mode, maps and booking form.

## Deploy to GitHub + Vercel

1. Create a new GitHub repository.
2. Upload `index.html` and `README.md`.
3. Open Vercel and import the GitHub repository.
4. Framework preset: **Other** or **Static**.
5. Build command: leave empty.
6. Output directory: leave empty or use `.`.

## Booking and visitor alerts

The website already opens WhatsApp to `+255 746 584 214` when a customer sends a booking request.

For email alerts to `scbernard004@gmail.com`, create a Formspree form and paste the endpoint in `index.html` here:

```js
const ALERTS = {
  bookingEndpoint: 'https://formspree.io/f/YOUR_FORM_ID',
  visitorEndpoint: '',
  googleAnalyticsId: ''
};
```

Recommended setup:

- Use **Formspree** for booking/order email alerts.
- Use **Google Analytics 4** for website visitor tracking.
- Use **Beem** or **Africa's Talking** for SMS only through a secure backend/serverless function, not directly inside public HTML.

Visitor email alerts are optional because every page visit can create too many emails. If you still want them, create a separate Formspree endpoint and paste it in `visitorEndpoint`.

## Google Apps Script email option

You can also create a Google Apps Script Web App that receives the booking request and sends you an email. Paste the Web App URL into `bookingEndpoint`.

## Important

Do not paste SMS API secret keys inside `index.html` because GitHub makes the file public. Use a backend or Vercel serverless function for SMS.


## SEO + SSL Update

This version includes extra Google-ready setup:

- SEO title and description for Kasoko Travels.
- Search terms for Kasoko Travels, Arusha safaris, Tanzania hotels, airport transfers, Ngorongoro, Tarangire and Lake Manyara.
- Structured data using Schema.org TravelAgency / LocalBusiness / Organization.
- Open Graph and Twitter preview tags.
- `robots.txt` to allow Google to crawl the site.
- `sitemap.xml` to help Google discover the site.
- `vercel.json` with security headers including HSTS for HTTPS visits.

### Important after deployment

1. Deploy the folder to Vercel.
2. Vercel will provide HTTPS/SSL automatically after the domain/DNS is connected.
3. Open Google Search Console, add your Vercel or custom domain, verify ownership, and submit:
   `https://YOUR-DOMAIN/sitemap.xml`
4. Replace every placeholder URL `https://kasoko-travels.vercel.app/` inside `index.html`, `robots.txt`, and `sitemap.xml` with your real Vercel or custom domain.
5. Create a Google Business Profile for Kasoko Travels using the same phone number, email, website and Arusha service area. This helps people find the business when searching the name on Google and Google Maps.


## Logo
- `logo.svg` is included and used in the header, loading screen, footer, and browser tab icon.


## Premium branding update
- `logo.svg` = premium full logo used in the loader and footer.
- `logo-mark.svg` = premium icon mark used in the header and for favicon styling.
- The browser tab favicon now animates while the website is loading, then returns to the static company icon.


## Gallery and hotel update
- Added more destination cards and hotel/lodge cards.
- Added thumbnail galleries inside destination and hotel cards.
- Added a dedicated gallery section and hotel area guide.
- Added fallback images so cards do not remain blank if a remote hotel image blocks hotlinking.


## Luxury safari upgrade
- Homepage updated with a more premium safari-company look.
- Added a luxury concierge section, stronger gold/green brand styling and elevated card interactions.
- Added separate detail pages for 15 destinations and 12 hotels/lodges.
- Detail pages are kept in the root folder, with no extra folders, so GitHub/Vercel upload stays simple.
- Each detail page includes photos, location, highlights, price guide, booking flow, WhatsApp CTA and Google Map.

## Header update
- The header has been cleaned across the homepage and all detail pages.
- The small tagline under the Kasoko Travels logo was removed.
- Mobile spacing and menu alignment were improved for phones, tablets and desktop.

## Contact and order alert numbers
The website now lists these Mobile / WhatsApp numbers for customer bookings:
- 0746 584 214
- 0789 515 769
- 0744 355 769
- 0762 917 519

The homepage booking form includes a “Send order to” selector so a customer can choose which number receives the WhatsApp order. Email/SMS alert endpoint placeholders remain in `index.html` for Formspree, Google Apps Script, Beem, or another secure provider.
