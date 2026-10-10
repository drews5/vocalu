# Vocal U birthday grams

A responsive, dependency-free birthday site using Vocal U's existing Yearbook font. Offers $5 personalized Happy Birthday videos and $50 in-person song performances.

## Open bookings

Set the verified `venmoHandle` (without @) and `bookingEmail` in `birthday-config.js`. Until configured, payment and email submission are disabled and the page clearly says bookings are not open. The copy-request action is available but does not submit anything.

Requests open a prefilled email in the visitor's email app. The visitor must send it. There is no order database, payment verification, or automatic reservation. Confirm in-person date/location before collecting payment. Venmo links include package price and a booking note; Venmo handles the transaction.

## Hosting

Serve the repository root as a static site. The GitHub Pages workflow builds a dedicated artifact containing only the page, configuration, and font. Enable GitHub Pages with **GitHub Actions** as the source in repository Settings → Pages if not already enabled. No packages or build step are needed.

## Validation

The inline script and configuration are checked with Node's syntax checker. Browser interaction and production deployment need verification in a browser after hosting is available.
