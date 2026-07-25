# LexisNexis Risk Solutions (lexisnexis-risk-solutions)

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
