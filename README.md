# United Social Services Inc. (USS) Fundraising Website

Final animated client-revision package updated August 20, 2026.

Original deployment reference: https://uss-fundraising.lewissteve552686.chatgpt.site

## Package contents

- `website-source/` — complete production source, responsive styles, automated route tests, official transparent logo and local image assets.
- `brand-assets/USS_Official_Logo_Transparent.svg` — exact client-supplied official USS monogram used as the single primary visible logo.
- `documentation/` — client source material, confirmed link map, implementation checklist, photo sources and final QA report.

## Run locally

Requirements: Node.js 22.13 or newer and npm.

```bash
cd website-source
npm run install:ci
npm run dev
```

## Build and test

```bash
npm run lint
npm test
npm run start
```

## Main editable files

- `website-source/app/site.tsx` — all page routes, approved copy, carousels, forms and confirmed link configuration.
- `website-source/app/globals.css` — responsive design, reveal animation, carousel transitions and button motion.
- `website-source/app/layout.tsx` — title, description and logo metadata.
- `website-source/public/` — official logo, founder portrait and locally packaged photography.

## Integration behavior

- Primary donation actions route visitors through the website donation experience and then to the confirmed Zeffy form.
- Amazon needed-item purchases open in a new tab.
- The dedicated DAF & Endowment page connects donors to the approved USS Donor-Advised Fund and Endowment & Legacy Fund forms.
- Contact and partner forms prepare a pre-addressed email to `lwallace@usstx.org` in the visitor's email application.
- Financial gifts are processed by the selected third-party provider; the website does not store payment-card information.
