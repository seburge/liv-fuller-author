# Liv Fuller Author

A responsive, five-page author website using the approved deep blue, teal, and cyan direction. Static HTML and CSS; no build step, dependencies, tracking, or credentials.

## Preview
Run `python3 -m http.server 8000` and visit http://localhost:8000.

## Hosting
Publish the repository root using any static host. A root-relative domain is not required; links also work from a GitHub Pages project subdirectory. This repository is source code, not a WordPress theme or import file. Uploading it does not change the existing WordPress site.

## Edit
Edit the five HTML pages in the repository root. Shared presentation is in `styles.css`.

## Contact and release notifications
Contact and release notifications are collected directly through Netlify Forms. The author's publicly listed email and Facebook remain available.

## Content and branding
Copy is based on the revised WordPress drafts reviewed in this conversation. Palette approximated from the supplied logo screenshot: #294381, #218f9f, #00d8ed. The supplied author portrait is in `assets/jen-about-picture.jpg` and appears on the About page. The supplied book illustration is in `assets/blessingboxhugh.webp` and appears on the Books page. No original logo artwork was available as a clean asset in this build. Publication timing is intentionally unspecified; update the book page and CTA when the release is confirmed.

## Reader and publicity resources
The homepage features The Blessing Box. Educator conversation starters and a media kit are available as pages and downloadable text files. Existing author and book artwork remain in assets/.

Contact and release-notification forms use Netlify Forms. Detection must be enabled in Netlify. Submissions are stored in the site's Forms dashboard; release signups do not automatically send a newsletter or release email. Export the release list and send the notification when the release is confirmed. Email notifications for contact submissions can be configured in Netlify Forms settings. The privacy page describes the collection purpose.

Add a sample chapter, confirmed release date, buying links, endorsements, and dated public events only after those materials are supplied and approved. The site currently makes no claims about these.

## Contact recipient routing

`contact.html` registers `contact` (Liv) and `contact-quincy` (Quincy). Its recipient picker updates both the form name and hidden `form-name` field before the browser posts the message. The hidden Quincy skeleton registers all matching fields with Netlify. Without JavaScript, Quincy has a direct email link and cannot accidentally be selected for Liv's form.

Before publishing this change, configure Netlify **Forms → Submission notifications**:

- Keep Liv's existing notification destination, scoped to the `contact` form.
- Add an email notification for `contact-quincy` to `Quincy@themousepatrol.com`.
- If Liv currently has a notification for **all forms**, scope it so Quincy submissions are excluded, preserving any separate release-signup and reader-feedback notifications.

The `contact-quincy` form becomes available after a deploy containing this HTML. Coordinate the deploy and notification setup, and verify the two form-specific destinations before considering routing complete. Existing submissions remain in the original `contact` form and are not resent.
