# Setup

Run once per workspace. Answers are baked in; you should never see these again.

1. **Firm or practice name?** → `{{FIRM_NAME}}`
2. **Who reads the output?** Role and name if you have one. → `{{RECEIVER}}`
3. **Area of law?** Default: employment. → `{{PRACTICE_AREA}}`
4. **Jurisdiction?** Affects document types. Default: Ontario, Canada.
   → `{{JURISDICTION}}`
   - Derived: expected document set. Ontario → ROE, ESA references.
5. **Which documents do clients usually send?** Default: employment contracts,
   job offers, job descriptions, pay stubs, termination letters, ROEs.
   → `{{EXPECTED_DOCS}}`
6. **Which fields matter most?** The ones that come back wrong. Default: length
   of service, compensation. → `{{PRIORITY_FIELDS}}`
7. **Where do client folders live?** Default: Google Drive.
   → `{{SOURCE_LOCATION}}`
8. **Where does the output need to land?** Where the receiver already works.
   → `{{OUTPUT_LOCATION}}`

?? 2, 6 and 8 need a real answer from a real receiver. Defaults are a guess
   until then.
