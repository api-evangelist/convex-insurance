# Convex

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

Convex Group Limited is an international specialty insurer and reinsurer, founded in 2019 by
Stephen Catlin and Paul Brand and headquartered in London, with operations in Bermuda,
Luxembourg, Guernsey and the United States. Convex underwrites complex commercial and specialty
risk — property, casualty, marine, energy, aviation, cyber, political risk and credit, crisis
management, accident and health, and equine/livestock/aquaculture — and writes property, casualty
and specialty treaty reinsurance through Convex Re Limited. Convex Insurance UK Limited is
authorised by the Prudential Regulation Authority and regulated by the FCA and the PRA. It is a
London company-market carrier rather than a Lloyd's syndicate, and reported roughly $5.2bn of
gross written premium in 2024.

## API posture

Convex has a real API programme and no public API.

Its [Digital Underwriting](https://convexin.com/underwriting/digital-underwriting/) team publicly
describes building "a suite of insurance specific API's" that auto quote, bind and portfolio-manage
high-volume, low-complexity specialty business, delivered either through a Convex-hosted broker
portal or by connecting Convex products "seamlessly into existing broker & client portals via
API's". That capability is arranged commercially, through named business-development contacts,
not through documentation.

As of 2026-07-25 there is:

- **No developer portal.** `developer.`, `developers.` and `docs.convexin.com` do not resolve;
  `/developers`, `/developer`, `/api` and `/integrations` all return 404; the full site sitemap
  (79 URLs) contains no developer or API page.
- **No API reference and no machine-readable definitions.** No OpenAPI, Swagger, AsyncAPI,
  GraphQL SDL, protobuf or Postman collection was found anywhere. No GitHub organisation exists.
- **A live but closed API host.** `https://api.convexin.com` answers every anonymous request —
  including every OpenAPI, Swagger and `.well-known` discovery path — with HTTP 401
  `{"message":"Unauthorized","http_status_code":401}`. The gateway is real; its shape is not
  observable from outside.
- **Gated broker surfaces.** `https://digital.convexin.com` is the "Convex Digital Underwriting"
  broker application, served as an Unqork-hosted app behind login. [Convex Quick
  Quote](https://convexin.com/underwriting/quick-quote/), the event-insurance quote-and-bind
  product, is reached by registering interest in a broker account.
- **No ACORD posture published.** Case-insensitive checks for ACORD, AL3, ACORD XML, NGDS, IVANS,
  Vertafore and Applied Epic across convexin.com, us.convexin.com and the Digital Underwriting
  one-pager returned zero hits, as did checks for Blueprint Two, PPL, Whitespace and ADEPT.
- **No webhooks or event catalog.**

Of the four insurance API verbs, quote and bind are described as capabilities but exposed only to
contracted partners; issue and FNOL have no API at all — claims are notified through the
[claims contact page](https://convexin.com/claims/).

This is the honest carrier posture, and the point of recording it: the United Kingdom has FCA and
PRA supervision but no open-insurance obligation, and the London Market's only market-wide data and
API modernisation effort (Blueprint Two, PPL, Whitespace, Ki, ACORD ADEPT) is aimed at brokers and
syndicates rather than developers. Convex's best API work is therefore invisible from the outside.

## Links

- Website — https://convexin.com/
- Digital Underwriting — https://convexin.com/underwriting/digital-underwriting/
- Digital Underwriting one-pager (PDF) — https://convexin.com/wp-content/uploads/2025/10/Convex-Digital-Underwriting-One-Pager-1025.pdf
- Convex Quick Quote — https://convexin.com/underwriting/quick-quote/
- Convex US — https://us.convexin.com/
- Contact — https://convexin.com/contact-us/
- LinkedIn — https://www.linkedin.com/company/convex-insurance

## Files

- [`apis.yml`](apis.yml) — APIs.json 0.19 company record for Convex.
- [`review.yml`](review.yml) — API Evangelist review: probe-by-probe findings, ACORD posture,
  quote/bind/issue/FNOL coverage, auth model and transports.
