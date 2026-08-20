# Final Quality Assurance Report

Date: August 20, 2026

## Release status

- Production build: passed.
- ESLint: passed.
- Automated tests: 6 passed, 0 failed.
- Browser interaction and responsive layout checks: passed.
- Package integrity and final archive test: passed.

## Automated coverage

The final suite verifies:

1. Final page metadata without development-preview branding.
2. Successful HTML responses for all 16 public routes.
3. Approved campaign, Mission, Vision, Values, founder and Motto content.
4. Confirmed Zeffy, Amazon needed-item, social, contact, phone and address destinations.
5. DAF/Endowment, future-language, founder LinkedIn and $100 campaign revisions.
6. Exact Current Needs and Future Needs donation-routing designations.

## Routes checked

`/`, `/about`, `/our-work`, `/our-work/pathways-to-home`, `/our-work/bridge-to-stability`, `/campus`, `/impact`, `/ways-to-give`, `/donate`, `/major-gifts`, `/partner`, `/stories`, `/contact`, `/daf-endowment`, `/privacy`, `/terms`.

## Content, visual and performance checks

- The exact client-supplied SVG is the visible header/mobile/footer logo. Attachment, public aliases, packaged brand asset and production-build copies share the same SHA-256 hash.
- All 38 packaged JPEG assets were inspected for clarity, proportions and irrelevant branding. All 36 displayed mission-photo references are unique; the founder portrait remains the approved local image.
- The AUROLA image and its source reference were removed. The replacement campus photograph contains no visible unrelated branding.
- The approved founder portrait, organization logo and USS monogram favicon are stored locally.
- Enlarged type, navigation, long headings, cards, forms, campaign content and footer rules were audited at 320px, 375px, 430px, 768px, 1024px, 1440px and 1600px. No horizontal overflow was detected.
- Desktop and 320px hero layouts were visually inspected in the browser. The mobile menu opened with all eight navigation links visible, and the responsive logo rendered at 42px mobile, 46px tablet and 52px desktop.
- `/donate?fund=today` rendered “Fund USS Today” and “Current Needs / Where Most Needed Today.” `/donate?fund=future` rendered “Build USS Tomorrow,” “Future Needs” and “Campus, Housing & Future Infrastructure,” without current-needs copy.
- The campaign share fallback displayed the approved “Campaign link copied.” confirmation.
- Carousels use opacity and transform transitions, pause during hover/focus and provide accessible previous, next and dot controls.
- Only the first hero image receives high-priority loading; subsequent and below-fold images are lazy loaded.
- Scroll reveals use `IntersectionObserver` instead of continuous scroll handlers.
- `prefers-reduced-motion` disables automatic carousel rotation and motion-heavy effects.
- Representative stock subjects are not presented as actual United Social Services Inc. (USS) participants or properties.
- All 16 public routes, 673 rendered anchor occurrences, 13 unique external destinations and 37 rendered image sources were statically audited. No missing route, placeholder link, unsafe external target, missing local image, unexplained empty alt or missing intrinsic image dimensions was found.
- Core Zeffy, PayPal, Cash App, Venmo, Facebook, Instagram, USS LinkedIn and Maps destinations returned live responses. The approved Amazon short link resolved to the intended Amazon wishlist; Amazon and the founder LinkedIn profile limited automated access, so their exact client-approved destinations were additionally verified in source and rendered markup.
- Both packaged PDF implementation guides were regenerated from the current link map and release rules, rendered page by page and checked for obsolete destinations.

## Known integration behavior

The contact and partner forms intentionally open the visitor's configured email application. They do not silently transmit or store form data. Financial gifts and needed-item purchases are completed on the selected third-party provider.
