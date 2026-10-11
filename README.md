# Island Futures

A proposed reorganization of [Island Futures](https://www.mvislandfutures.org/) for young people and career seekers on Martha’s Vineyard. Retains the original logo, Manrope/Raleway typography, coastal colors, ocean photograph, and selected career imagery.

## Run

Requires Node.js 20 or later. No third-party runtime or build dependencies.

```sh
npm run dev
npm run build
npm run check
```

The build generates static pages into `dist/`. Vercel uses the tracked configuration. No environment variables are required.

## Information architecture

- Explore careers: 16 pathway guides with role examples, training, funding, and next steps.
- Training & certifications: 13 program entries, searchable and filterable by career, location, and training type.
- Find work: local job boards, employer careers pages, and regional sources, explicitly distinguished from verified vacancies.
- How to apply: a practical checklist, provider handoffs, and application help.
- Paying for training, guidance, student resources, employer resources, events, and about pages.
- Saved paths: device-local shortlist of career and training pages.
- Twenty-two old route names forward to their new destinations.

## What the original site review found

The original website already has professional pathways, training information, financial aid resources, and a job board. The main navigation puts most destinations inside “Explore”; certifications are nested within industry pages, and the general “Resources” label does not explain the available help. Career exploration, training, funding, and applications are separate destinations without a consistent next-step journey.

The revised sitemap uses visitors’ tasks as navigation labels and connects each pathway to training, financial support, and applying. Original guide links preserve access to deeper information that has not been independently revalidated.

Current-content issues observed in October 2026:

- The interpretation pathway describes the ACE MV program as paused.
- Automotive training on the Island is described as planned, with details pending.
- Some event descriptions have a past date without a year or a date marked TBD.
- Electrical training is a four-year classroom route toward a journeyman license; the broad original “often under two years” statement must not be applied to every licensed trade.
- A certificate of course completion, certification preparation, and professional licensure are not interchangeable.

## Content and data

Edit `src/data.mjs` for careers, training, job sources, and funding resources. Edit `scripts/build.mjs` for page templates and static explanatory content. `public/styles.css` and `public/app.js` contain the presentation and browser interactions.

Information is based on the original site's published pathways and linked providers. The directory is curated, not a live feed. It makes no guarantee of current enrollment, vacancies, funding awards, or admissions eligibility. Before an official organization launch, the content owner should validate every program's provider, current status, cost, duration, requirements, and application URL, then establish a routine review and expiry process.

Applications go directly to provider/employer websites. Guidance and employer buttons open clearly labeled email drafts. This version has no application intake, automated application routing, email delivery backend, CMS, accounts, or job-posting administration. No inquiries were submitted during development.

The checklist and saved paths use localStorage, with a visible message when storage is unavailable. No applicant documents or personal records are collected. The privacy page describes this behavior.

## Source references

- https://www.mvislandfutures.org/career-pathways
- https://www.mvislandfutures.org/resources
- https://www.mvislandfutures.org/job-board
- https://www.mvislandfutures.org/financialaid
- https://www.mvislandfutures.org/mvrhs
- https://www.mvislandfutures.org/events
- Individual original pathway pages linked from each revised guide.
- https://acemv.org/trades/electrician/
- https://acemv.org/ece/
- https://capecod.edu/ccape/community-career-and-professional-education/cape-and-islands-area-health-education-center/medical-interpreter-certificate/
- https://www.massbay.edu/academics/automotive

Original photographs and brand assets remain the property of their respective rights holders and are reused for this requested Island Futures implementation. Fonts are locally served Google Fonts (Manrope and Raleway).

## Deployment and indexing

This is a proposed replacement hosted separately on Vercel; it does not change mvislandfutures.org or its DNS. Pages use `noindex,nofollow` and a disallowing robots.txt while this proposal is reviewed. For an approved domain launch, update indexing directives, add canonical URLs and a sitemap, and configure server redirects for legacy URLs.

## Verification

- Static check validates all 65 HTML routes and internal asset/link targets.
- Browser checks cover career search, zero-result recovery, career filters, linked program filters, provider links, saved path persistence, application checklist persistence, and program-specific guidance prefills.
- Desktop and mobile layouts, menu controls, console errors, and horizontal overflow were checked.
- Email drafts and external applications were not sent or submitted.

A live outbound link check identified three original 404 destinations. The MV Times, Vineyard Gazette, and medical interpreter links were updated to current destinations; medical interpreter details were refreshed from the new provider page. Some external sites block automated requests, so reachability is not a guarantee of current eligibility or openings.
