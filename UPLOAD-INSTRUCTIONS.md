# 3580 Karrington Place — website upload instructions

This package contains the current home-sale website, including all 31 gallery photos and captions, the walkthrough video, the $384,900 asking price, the open-house banner, and recent home updates.

## Upload the site

1. Unzip `3580-Karrington-Place-Website.zip` on your computer.
2. In your hosting account, open the website's file manager or its static-site upload tool.
3. Upload `index.html` and the entire `assets` folder into the site's web root. This is often called `public_html`, `www`, or the publish directory. Keep `index.html` directly inside that directory, alongside `assets`.
4. Keep the folder names and filenames unchanged. Upload all the photos and the MP4 video.
5. Open your new website address and check the hero photo, gallery, walkthrough, navigation, and contact form.

The ZIP has `index.html` at its top level. If your host accepts a ZIP upload, upload and extract it into the web root. If it asks for a folder, select the folder containing `index.html` and `assets`. No install command, build command, database, or server-side app is required. Choose a host that serves static HTML and MP4 files. This package is not a WordPress theme.

Use HTTPS on your hosting account. Domain and DNS configuration are handled by your hosting provider. These files do not transfer your existing ChatGPT site's sharing restrictions to the new host; access is controlled by the new host.

## Contact form

The form is configured to submit inquiries through FormSubmit to **meganhett@gmail.com**, using the same-page AJAX endpoint. It automatically includes your new page address in the inquiry rather than the old ChatGPT site address.

After uploading, submit one test inquiry from your new website. If FormSubmit requests activation, open its confirmation email in Megan's inbox (check spam too) and confirm the form. Then submit another test and verify receipt before sharing the site with buyers. Delivery has not been independently verified in this export. The form requires an internet connection and the FormSubmit service.

FormSubmit's official setup and activation instructions: https://formsubmit.co/ and https://formsubmit.co/help

## Update the content

The website's HTML, styling, and JavaScript are all in `index.html`. Open it in a plain-text code editor, make your changes, and upload the revised file. There is no separate login-based administration dashboard in this package.

- **Price and statistics:** Search for `$384,900` or the section with `id="overview"`.
- **Room measurements and recent updates:** Search for `Room sizes at a glance.` or `Recent home updates`.
- **Open house:** Search for `id="openHouseBanner"`. Update the visible date and hours, the corresponding `datetime` attributes, and `data-expires`. The current event is October 10, 2026, 11 a.m.–1 p.m. Central Time, and hides on page loads after `2026-10-10T13:00:00-05:00`.
- **Hero image:** Replace `assets/hero-exterior.jpg` using the same filename, or change its `src` in the overview section.
- **Walkthrough:** Replace `assets/3580-karrington-walkthrough.mp4` and optionally `assets/walkthrough-poster.jpg`. Also update the displayed tour duration if it changes.
- **Gallery captions:** Search for the relevant caption in the section with `id="gallery"`. Each photo has a `data-label` (displayed title), `data-caption` (lightbox caption), and image `alt` text. Keep visible titles descriptive; filenames are not used as titles. Escape `&` as `&amp;` and double quotes inside attributes as `&quot;`.
- **Gallery photos/order:** Gallery images are in `assets/gallery-photos`. Keep the `src` and `data-full` paths pointed at the same image. Photo order follows the `.gallery-item` buttons in the HTML. If adding or removing photos, update the `See all 31 photos` text and numbered `aria-label` descriptions. The first five buttons form the preview; later buttons have the `gallery-overflow-item` class. Keep virtual-staging disclosures where applicable.
- **Inquiry recipient:** Search for `meganhett@gmail.com` and update both the form action and the AJAX endpoint. A new recipient must activate the form with FormSubmit.

Keep a backup of the ZIP before editing. No API keys, passwords, repository credentials, or hosting-specific configuration are included.
