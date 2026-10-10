# Vocal U birthday grams

A responsive, dependency-free birthday site using Vocal U's existing Yearbook font. Offers $5 personalized Happy Birthday videos and $50 in-person song performances.

## Open bookings

Set the verified `venmoHandle` (without @) and `bookingEmail` in `birthday-config.js`. Until configured, payment and email submission are disabled and the page clearly says bookings are not open. The copy-request action is available but does not submit anything.

Requests open a prefilled email in the visitor's email app. The visitor must send it. There is no order database, payment verification, or automatic reservation. Confirm in-person date/location before collecting payment. Venmo links include package price and a booking note; Venmo handles the transaction.

## Hosting

Deploy the repository root on the Vercel project that owns `vocalu.org`. Use the Other framework preset with no build command. No packages or build step are needed. Connect `drews5/vocalu` with `main` as its production branch.

`vercel.json` rewrites both `/birthday` and `/birthdays` (including trailing-slash variants) to the same `birthday.html` page. Assets use root-relative URLs so they resolve on either route. The existing root page and other static files remain available. The obsolete GitHub Pages workflow is removed.

The domain must already be assigned to this Vercel project, or be assigned through Vercel's domain settings. Repository configuration cannot assign a custom domain or prove a production deployment. Verify both `https://vocalu.org/birthday` and `https://vocalu.org/birthdays` after the production build completes.

## Validation

The inline script and configuration are checked with Node's syntax checker. Browser interaction and production deployment need verification in a browser after hosting is available.
