# LexisNexis Risk Solutions (lexisnexis-risk-solutions)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

LexisNexis Risk Solutions is the risk-data and analytics arm of RELX, headquartered in Alpharetta, Georgia, and one of the small number of intermediaries that sit between United States property and casualty carriers and the distribution channel. In insurance it does not underwrite risk; it sells the contributory databases and scores that carriers rate against — C.L.U.E. Auto claims history, Current Carrier prior-coverage verification, Motor Vehicle Records across all fifty states, Driver Discovery undisclosed-driver detection, InsurView public-records attributes and VIN Services vehicle data — alongside telematics exchange, data prefill, fraud detection, claims and life-insurance underwriting products.

Because the United States has no federal insurance regulator and no open-insurance mandate, value in this market accrued to exactly this layer rather than to the carriers, and LexisNexis Risk reaches its customers through carrier policy-administration and rating systems rather than through an open API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lexisnexis-risk-solutions/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lexisnexis-risk-solutions/refs/heads/main/apis.yml)

## API Posture

A real first-party developer portal exists at [developer.lexisnexisrisk.com](https://developer.lexisnexisrisk.com/) (HTTP 200, a SwaggerHub Portal instance). Its landing page is anonymously readable and publicly enumerates six insurance API products. That landing page is the entire public surface — every product route returns HTTP 302 to `/sp-portal/session-expired` for an anonymous client, so all reference documentation, schemas and endpoint detail sit behind a login.

- **Developer portal:** https://developer.lexisnexisrisk.com/ — HTTP 200, product catalogue public, reference docs login-gated
- **Downloadable OpenAPI/Swagger:** none. `/openapi.json`, `/swagger.json`, `/api-docs` and `/sitemap.xml` all 404; the SwaggerHub registry owner `lnrs` resolves but publishes zero APIs
- **ACORD posture:** ACORD is named as an industry-organization alliance partner only. No AL3, ACORD XML, NGDS or IVANS transaction is documented publicly
- **Quote / bind / issue / FNOL:** none exposed. The products are risk-data lookups consumed inside a carrier's quoting, underwriting and claims workflow, partner-only under contract
- **Auth model:** portal session login; no public API authentication scheme documented. No valid OIDC or OAuth authorization-server metadata is served
- **Webhooks / events:** none documented
- **Postman / GraphQL / gRPC:** none found
- **Home market:** United States

The visible integration seam is the policy administration system, not an open API — for example the [Guidewire Marketplace listing for LexisNexis Risk Solutions Motor Vehicle Records for PolicyCenter](https://marketplace.guidewire.com/product/lexisnexis-risk-solutions-motor-vehicle-recordsfor-policycenter/01t3n00000TGZ6NAAX).

## Tags

- Insurance
- United States
- Risk Data
- Property and Casualty
- Underwriting
- Claims
- Life Insurance
- Auto Insurance
- Data Analytics
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

### C.L.U.E. Auto

A contributory claim-history information exchange containing up to seven years of personal automobile claims matching the search criteria, used by carriers during quoting and underwriting.

- **Human URL:** [https://developer.lexisnexisrisk.com/clue_auto](https://developer.lexisnexisrisk.com/clue_auto) (login required)

#### Properties

- [Documentation](https://risk.lexisnexis.com/products/clue-auto)
- [API Reference](https://developer.lexisnexisrisk.com/clue_auto)

### C.L.U.E. Auto with Current Carrier

C.L.U.E. Auto combined with Current Carrier, which identifies the carriers of existing or previous insurance policies so an underwriter can validate coverage and underwriting information and assess auto and property risk.

- **Human URL:** [https://developer.lexisnexisrisk.com/clue_auto_cc](https://developer.lexisnexisrisk.com/clue_auto_cc) (login required)

#### Properties

- [Documentation](https://risk.lexisnexis.com/products/current-carrier)
- [API Reference](https://developer.lexisnexisrisk.com/clue_auto_cc)

### Driver Discovery

Identifies potentially undisclosed drivers residing at an applicant's address, helping auto insurance carriers detect additional household drivers that were not declared on the application.

- **Human URL:** [https://developer.lexisnexisrisk.com/driver_discovery](https://developer.lexisnexisrisk.com/driver_discovery) (login required)

#### Properties

- [Documentation](https://risk.lexisnexis.com/products/driver-discovery)
- [API Reference](https://developer.lexisnexisrisk.com/driver_discovery)

### InsurView

Leverages one of the industry's largest collections of public records and other data sources to provide a view of the consumer that complements traditional insurance scoring.

- **Human URL:** [https://developer.lexisnexisrisk.com/insurview](https://developer.lexisnexisrisk.com/insurview) (login required)

#### Properties

- [Documentation](https://risk.lexisnexis.com/products/insurview)
- [API Reference](https://developer.lexisnexisrisk.com/insurview)

### Motor Vehicle Record (MVR)

Motor Vehicle Record data allowing insurance companies to evaluate driver histories consistently in all fifty states, sourced from state departments of motor vehicles.

- **Human URL:** [https://developer.lexisnexisrisk.com/mvr](https://developer.lexisnexisrisk.com/mvr) (login required)

#### Properties

- [Documentation](https://risk.lexisnexis.com/products/motor-vehicle-records)
- [API Reference](https://developer.lexisnexisrisk.com/mvr)

### VIN Services

Vehicle registration and title data keyed on the vehicle identification number, used in auto quoting, underwriting and prefill.

- **Human URL:** [https://developer.lexisnexisrisk.com/vin_services](https://developer.lexisnexisrisk.com/vin_services) (login required)

#### Properties

- [API Reference](https://developer.lexisnexisrisk.com/vin_services)

## Links

- [Website](https://risk.lexisnexis.com/)
- [Insurance solutions](https://risk.lexisnexis.com/insurance)
- [Products](https://risk.lexisnexis.com/products)
- [Developer Portal](https://developer.lexisnexisrisk.com/)
- [Insurance Alliance Program](https://risk.lexisnexis.com/about-us/alliance-partnerships/insurance)
- [Industry Organization Alliances (ACORD)](https://risk.lexisnexis.com/about-us/alliance-partnerships/insurance/industry-organization)
- [Customer Support Hub](https://lnrs.my.site.com/CustomerSupportHub/s/)
- [Insights and Resources](https://risk.lexisnexis.com/insights-resources)
- [LinkedIn](https://www.linkedin.com/company/lexisnexis-risk-solutions)
- [Twitter](https://twitter.com/LexisNexisRisk)

## Maintainers

- Kin Lane — kin@apievangelist.com
