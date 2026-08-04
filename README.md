# Overjet (overjet)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Overjet is a dental AI platform that applies FDA-cleared computer vision to dental radiographs (bitewings, periapicals, panoramics, and CBCT) to detect, outline, and quantify oral health conditions - caries, calculus, bone level and bone loss, periapical radiolucencies (PARLs), and anatomical structures - for dental providers, DSOs, and insurance payers. Founded by MIT and Harvard researchers, Overjet also offers IRIS imaging, a Voice AI documentation suite, automated insurance verification, and payer-side claim review (ReviewPASS).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/overjet/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/overjet/refs/heads/main/apis.yml)

## Access Model — Partner-Gated, No Public API

Overjet is **not** a self-serve public API and does **not** publish a developer portal or API reference. As of this catalog entry there is no `developer.overjet.com`, no public API documentation, no published base URL, and no self-serve API keys.

Overjet delivers its AI as **OEM / partner integrations** embedded directly into imaging systems and practice management software rather than as a standalone HTTP API:

- **Delivery mechanism:** connector software installed on imaging workstations plus DICOM image routing. Radiographs are automatically routed to Overjet's cloud, analyzed in roughly 2-3 minutes, and results (annotations and measurements) are surfaced in the practice management or imaging UI when the dentist reviews findings.
- **Certified PMS/imaging integrations:** Open Dental, Dentrix (including Dentrix Ascend and Enterprise), Eaglesoft, Oryx, CareStack, plus imaging systems such as Carestream and MiPACS.
- **Payer side:** insurance verification and AI-assisted claim review (ReviewPASS) are provided to insurance payers under enterprise agreement.

Any programmatic access is arranged privately under a partner or enterprise contract; it is not open registration. The APIs described in `apis.yml` are therefore **logical, honestly-modeled surfaces** (`endpointsModeled: true`, `accessModel: partner-gated`) that represent the capabilities Overjet exposes to integration partners. They are **not** documented public endpoints, and no base URLs, request/response schemas, or authentication details are fabricated. Because no public specification exists, this repository intentionally omits `openapi/`, `plans/`, `rate-limits/`, `finops/`, and `collections/` directories.

## Tags

- Dental
- Dental AI
- Healthcare
- Radiograph Analysis
- Computer Vision
- Medical Imaging
- Caries Detection
- Insurance
- Partner API
- Gated

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (Modeled)

### Overjet Vision AI Image Analysis API

Modeled surface for submitting dental radiographs (bitewing, periapical, panoramic, CBCT) to Overjet's FDA-cleared Vision AI. In production this is fed by connector software and DICOM routing rather than a public HTTP endpoint. `endpointsModeled: true`, partner-gated.

### Overjet Detections & Findings API

Modeled surface for retrieving structured AI findings - outlined caries, calculus, bone level and bone-loss measurements, PARLs, and anatomical structures with per-finding confidence and segmentation. `endpointsModeled: true`, partner-gated.

### Overjet Insurance Verification API

Modeled surface for automated dental insurance eligibility and benefits verification. Delivered as a product feature and payer integration. `endpointsModeled: true`, partner-gated.

### Overjet Claims Review (ReviewPASS) API

Modeled payer-side surface for AI-assisted dental claim review and automated approvals (ReviewPASS). `endpointsModeled: true`, partner-gated.

### Overjet DSO Analytics API

Modeled surface for clinical and operational analytics aggregated across practices and providers. `endpointsModeled: true`, partner-gated.

## Pricing

Overjet does not publish pricing. It is quoted by contacting sales and is scoped per practice / per organization; third-party reviews cite roughly $1,000-$2,000+ per month for smaller practices, scaling with size, features, and integrations. There is no public, self-serve plans document, so no `plans/` directory is included.

## WebSocket

Overjet does not document any public WebSocket API. See `review.yml`.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/overjet)
- [Website](https://www.overjet.com/)
- [Documentation / Resources](https://www.overjet.com/resources)
- [Sign In](https://clinic.overjet.ai/signin)
- [Book a Demo](https://info.overjet.com/hp-book-your-demo)
- [Trust Center](https://www.overjet.com/legal/trust-center)
- [Blog](https://www.overjet.com/blog)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
