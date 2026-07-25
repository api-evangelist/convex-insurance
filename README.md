# Convex

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
