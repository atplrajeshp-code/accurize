# Accurize Technologies Website — V3 Page-by-Page Redesign

This static website package gives each page family its own visual treatment while preserving consistent Accurize branding and navigation.

## Deployment
Upload the contents of this folder to the root of the GitHub repository connected to Vercel. `index.html` must be directly at the repository root. For Vercel static HTML, use framework preset `Other`, no build command, and root output directory.

## Included in this redesign
- Page-family visual treatments for About, Services, Training, Projects, Project Details, College Programs, Resources, Contact/Enquiry, Locations, Gallery, Testimonials, Policies and 404.
- Route-specific hero photography and topic accent colors.
- Responsive mobile navigation.
- Existing SEO metadata, canonical tags, structured data, sitemap, robots.txt, enquiry links and page content retained where present.

## Before connecting the official domain
Test all links on desktop and mobile, verify that enquiry submissions open the intended email client, test phone and WhatsApp links, and run PageSpeed Insights. This is a static HTML website; form delivery/analytics requires an actual connected backend or analytics service.


## Technical SEO and conversion tracking update (October 2026)

- Canonical URLs, Open Graph URLs and JSON-LD WebPage/BreadcrumbList markup currently use `https://accurizetechnologiesweb.vercel.app`. When the production custom domain is connected and selected as the primary domain, update canonical URLs and sitemap URLs to that primary domain and redirect the alternate host.
- `sitemap.xml` lists 70 HTML pages; `robots.txt` allows crawling and points crawlers to the sitemap. The 404 page is marked `noindex`.
- Page descriptions and titles are unique across the current HTML pages. Images use lazy loading/async decoding to reduce initial page work.
- Lead interactions push `phone_click`, `email_click`, `whatsapp_click`, `enquiry_cta_click`, and `enquiry_submit` events into `window.dataLayer`. These are event hooks only; they do not send analytics data to Google until a valid Google Tag Manager container or GA4 tag is installed.
- To enable GA4 tracking: create a GA4 property, add its Google tag or GTM container to every page, publish it, then test phone, email, WhatsApp and enquiry events in GA4 DebugView/Tag Assistant. Do not paste secret credentials into public HTML.
- Static HTML forms prepare an email and WhatsApp message; they do not save leads to a server/database. For durable lead capture, connect a secure form endpoint or CRM and test spam protection and consent requirements.
- After deployment, verify `/robots.txt` and `/sitemap.xml` in a browser, then submit the sitemap in Google Search Console. Check live URLs and mobile/Core Web Vitals in Search Console/PageSpeed Insights.
