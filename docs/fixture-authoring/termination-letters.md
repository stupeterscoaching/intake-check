# Fixture authoring — termination letters

2026-10-14 · Why the five termination letters look the way they do, and what they
were modelled on. Written after an employment lawyer said the first versions were
far too thin: 35 to 84 words, where a real Ontario letter itemises everything.

Reuse this when redrafting any other fixture document. The method that worked:
research real examples, draft against one shared anatomy, then have a separate
checker read each draft against the fixture's answer key, the ESA arithmetic, and
a lawyer's eye for realism.

## Rules that keep a richer document from breaking a fixture

- **Every new fact gets compared with what the client said.** A fuller letter adds
  about thirty facts. Each one must agree, be something the client never raised,
  or be one of the fixture's designed discrepancies. Nothing else.
- **Amounts are correct under the ESA from the employer's own view of service.**
  Where that moved a figure the client had already stated (Okonkwo's notice, two
  weeks to three), the client's answer changed with it, so the designed set of
  discrepancies stayed exactly as the key describes.
- **A sparse fixture stays sparse through vagueness, not absence.** Arteaga's
  letter promises "all amounts owing under the ESA" without itemising, which real
  letters do. It keeps service, earnings and notice unverifiable.
- **File names never pre-label the test.** `pay-stub-UNKNOWN.md` told the pipeline
  what to find. Neutral names (`pay-stub-2.md`) make it read the contents.
- **No document explains the law to its reader.** Sentences like "overtime is not
  included, because the ESA bases termination pay on regular wages" are what make
  a letter read as written by AI.

## ESA rules the letters follow

| Rule | Detail | Source |
|---|---|---|
| Check jurisdiction first: the ESA covers provincially regulated employers only | Federally regulated work includes 'road transportation services, including trucks and buses, that cross provincial or international borders'. - Miller Thomson (Sept 2026): an Ontario-only carrier is provincially regulated. A carrier whose operations cross borders 'regularly and continuously' must follow the Canada Labour Code (CLC) 'rather than provincial employment standards'.  What the CLC requires instead: - Notice (graduated table since Feb 1, 2024): at least 2 weeks' written notice after 3 consecutive months, 3 weeks at 3 years, then one more week per completed year up to 8 weeks at 8+ years. Regular wages can be paid in lieu. - Severance after 12 consecutive months: the greater of 2 days' wages per completed year or 5 days' wages. - A written statement of vacation benefits, wages, severance pay and other benefits. It is due on the termination date when paying in lieu, or at least 2 weeks before it with working notice. - Unjust dismissal: non-union employees with 12+ months are protected, and written reasons are due within 15 days of a request after a complaint. - Deductions: CLC s.254.1.  The ROE rules (rules 16-17) are federal and apply either way.  ?? Bellweather Freight (long haul out of Hamilton): the fixture must decide whether its runs regularly leave Ontario. If they do, a letter framed under the ESA is itself a jurisdiction mismatch (README question 4).  Also: - https://www.millerthomson.com/en/insights/publications/doing-business-in-canada/transportation-operating-in-canadas-freight-logistics-and-transportation-sector/ - https://www.canada.ca/en/services/jobs/workplace/federal-labour-standards/termination.html - https://hrinsider.ca/terminating-a-federally-regulated-employee-new-requirements-that-employers-need-to-know/ | [link](https://www.canada.ca/en/services/jobs/workplace/federally-regulated-industries.html) |
| Notice must be in writing, addressed to the employee, served under ESA s.95, and name the termination date | O. Reg. 288/01 s.4(1): a notice of termination shall be '(a) given in writing; (b) addressed to the employee whose employment is to be terminated; and (c) served on the employee in accordance with section 95 of the Act'.  Service methods, s.95(1): - personally - by mail to the last known address, by a method that lets delivery be verified - by fax or email, if the person is equipped to receive it - by courier - in a sealed envelope left with someone who appears to be 16 or older at the last known address Text message is not on the list.  When service takes effect, s.95(2)-(5): - by hand: on hand-over - by mail: 5 days after mailing - by fax or email sent on a Saturday, Sunday or holiday, or after 5 p.m.: the next business day - by courier: 2 days after pickup  Ministry policy (Manual on O. Reg. 288/01): the notice 'must specify when the employment is to be terminated', even if the employee already knows. Oral notice counts only if it is longer than the statutory minimum and specific about the date.  Scope: - The rule applies after 3 months' continuous employment (ESA s.54). - O. Reg. 288/01 s.2 exempts, among others, employees guilty of wilful misconduct, fixed-term or fixed-task employees, and construction employees.  An immediate termination by phone or in a meeting is lawful if termination pay is paid under s.61. The letter then confirms the date and the payments.  Also: - https://www.ontario.ca/laws/statute/00e41#BK243 - https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/ontario-regulation-28801-termination-and-severance-employment | [link](https://www.ontario.ca/laws/regulation/010288) |
| Statutory notice by period of employment (ESA s.57) | Minimum notice by period of employment: - less than 1 year: 1 week - 1 year but less than 3: 2 weeks - 3 but less than 4: 3 weeks - 4 but less than 5: 4 weeks - 5 but less than 6: 5 weeks - 6 but less than 7: 6 weeks - 7 but less than 8: 7 weeks - 8 years or more: 8 weeks  Combining notice and pay: - Working notice and pay in lieu can be combined if the weeks add up. - If notice is longer than required, the statutory part is the last part, ending on the termination date.  Mass-termination notice (8, 12 or 16 weeks, with Form 1 to the Director) applies only when 50+ employees are terminated at one establishment within 4 weeks (s.58). It never applies to a single-employee letter.  Guide table: https://www.ontario.ca/document/your-guide-employment-standards-act-0/termination-employment#written | [link](https://www.ontario.ca/laws/statute/00e41#BK142) |
| Count the period of employment correctly: notice and severance use different rules | For notice (O. Reg. 288/01 s.8): - The period runs from the day the employee 'most recently commenced employment' to the day notice is given, or to the termination day if proper notice wasn't given. - Two successive periods of employment 'not more than 13 weeks apart' are added together. After a longer gap, only the latest period counts. - Leave or other inactive employment counts (ESA s.59(1)). The guide confirms that time off while the employment relationship continues counts, including sick leave, other leave and temporary lay-off.  For severance (ESA s.65(2)): - 'All time spent by the employee in the employer's employ, whether or not continuous and whether or not active' counts, for both the 5-year test and the amount. - So an earlier stint can count for severance but not for notice.  Unworked notice (s.65(4)): if notice wasn't given, severance is calculated as if the employee had worked through the notice period owed. The guide's 'Alex' example adds 8 weeks of pay in lieu to 10 years of service: $1,000 x 10.17 = $10,170.  Sale of business (ESA s.9): a buyer that employs the seller's employee takes on the seller's service. The exception is a hire more than 13 weeks after the earlier of the employee's last day with the seller and the day of the sale.  Also: - https://www.ontario.ca/laws/statute/00e41 (s.9, s.59, s.65) - https://www.ontario.ca/document/your-guide-employment-standards-act-0/continuity-employment - https://www.ontario.ca/document/your-guide-employment-standards-act-0/severance-pay | [link](https://www.ontario.ca/laws/regulation/010288) |
| Termination pay in lieu of notice is one lump sum of regular wages for each week of notice not given (ESA s.61) | s.61(1)(a) requires 'termination pay in a lump sum' equal to what the employee would have received under s.60 had notice been given. That means at least regular wages for a regular work week, for each week.  What counts as wages: - 'Regular wages' exclude overtime, public holiday pay, premium pay, vacation pay, termination pay and severance pay (s.1). - Some payments are not 'wages' at all (s.1): tips, expense and travelling allowances, and 'bonuses that are dependent on the discretion of the employer and that are not related to hours, production or efficiency'.  No regular work week, or paid other than by time (mileage, piece rate): use the average regular wages for the weeks worked in the 12 weeks immediately before the termination day (s.61(1.1), with s.60(2)).  Reductions: - Paid partial notice reduces the pay in lieu week for week. - Earnings from a new job do not reduce it (Manual Part XV). - ESA amounts are not subject to mitigation (Doorey).  Form of payment: in Pohl v. Hudson's Bay Co., 2022 ONSC 5230, paying ESA termination pay as bi-weekly salary continuance was 'entirely unacceptable'. Only an amount above the ESA can run as salary continuance or stop on re-employment.  Timing: due by the s.11(5) date (rule 10).  Guide example: 3 weeks x $800 = $2,400, plus 4% vacation pay of $96, for $2,496, plus 3 weeks of continued benefits.  Also: - https://www.ontario.ca/document/your-guide-employment-standards-act-0/termination-employment#pay - https://www.grosman.com/blog/employment-law/wrongful-dismissal/court-offers-another-warning-to-employers-to-take-care-when-dismissing-employees-without-cause/ | [link](https://www.ontario.ca/laws/statute/00e41#BK146) |
| Working notice: terms frozen, wages paid, benefits continued, and no vacation inside the notice period without consent | ESA s.60(1): during the statutory notice period the employer: - 'shall not reduce the employee's wage rate or alter any other term or condition of employment' - must pay each week no less than regular wages for a regular work week - must keep making benefit plan contributions to the end of the notice period  No regular work week: use the average over the weeks worked in the 12 weeks before notice was given (s.60(2)).  O. Reg. 288/01 s.7: the notice period can't include vacation time unless the employee agrees after receiving the notice.  The Manual adds that these duties attach only to the statutory part of a longer notice period, and that the wages are owed even if the employee is on leave or short-term disability.  Also: https://www.ontario.ca/document/your-guide-employment-standards-act-0/termination-employment#requirements | [link](https://www.ontario.ca/laws/statute/00e41#BK145) |
| Benefits continue to the end of the statutory notice period, including when pay in lieu is given (ESA s.61(1)(b), s.62) | The employer must keep making 'whatever benefit plan contributions would be required to be made in order to maintain the benefits' for the notice period the employee should have had. - s.62(1) deems the employee actively employed for plan purposes during that period. - Missed contributions are recoverable as unpaid wages (s.62(2)). - The Manual says the obligation includes the employee's share, if any.  With pay in lieu, coverage runs to the Termination Date plus the ESA notice weeks.  Health, dental, life, LTD and STD are all covered. If the insurer won't extend LTD or life coverage after active employment ends, the employer carries the risk (HR Reporter on Egan v. Alcatel, ONCA 2006, and Brito v. Canac, ONCA 2012).  Letters customarily give an end date for each benefit and the life-insurance conversion window, commonly 31 days.  In Russell v. The Brick, health and dental ran to a named date and life cover for 31 days, but LTD, AD&D and the group RRSP/DPSP were not continued. The court found the letter non-compliant.  ?? Whether the employer has a legal duty to tell the employee about conversion rights is unverified. The OCA template asserts it where group life is offered.  Also: - https://www.hrreporter.com/chrr-plus/employment-law/benefits-during-the-notice-period/315968 - https://www.littler.com/news-analysis/asap/ontario-canada-court-awards-employee-25000-moralaggravated-damages-because | [link](https://www.ontario.ca/laws/statute/00e41#BK146) |
| Severance pay (ESA s.64-66): 5+ years of service, plus a $2.5M payroll or a closure severing 50+ | Eligibility, s.64(1): severance is owed if the employee 'was employed by the employer for five years or more' AND either: - (a) the severance is because of a permanent discontinuance of all or part of the business at an establishment, and the employee is one of 50+ employees severed within 6 months as a result, or - (b) 'the employer has a payroll of $2.5 million or more'.  Payroll test, s.64(2): total wages of all employees in the last 4 completed weeks x 13, or in the last or second-last fiscal year. The guide calls it global payroll (Manual: Hawkes v. Max Aicher, 2021 ONSC 4290).  Service: all time with the employer counts, continuous or not, active or not (s.65(2)), plus unworked statutory notice weeks (s.65(4)).  Amount, s.65(1) and (5): regular weekly wages x (completed years + completed months/12), capped at 26 weeks. With no regular work week, use the average over the weeks worked in the 12 weeks before severance (s.65(6)).  Relationship to other pay: - Severance is on top of termination pay (s.65(7)), with only the set-offs listed in s.65(8). - No vacation pay is owed on severance.  Timing, s.66: - Due by the s.11(5) date. - Instalments only with the employee's agreement or the Director's approval, over at most 3 years. - One missed instalment makes the rest due at once.  Achkar says statutory severance is 'frequently missed or understated'.  Also: https://www.ontario.ca/document/your-guide-employment-standards-act-0/severance-pay | [link](https://www.ontario.ca/laws/statute/00e41#BK150) |
| Vacation pay on termination: 4% under 5 years, 6% at 5 or more, owed on termination pay but not on severance | ESA s.35.2: vacation pay is at least 4% of wages (excluding vacation pay) if the period of employment is under 5 years, and 6% at 5 years or more. A contract can give more (s.5(2)).  s.38: accrued vacation pay is paid out on the s.11(5) schedule.  The guide adds: - All unpaid vacation pay is owed, including from earlier years. - 6% applies to all wages in the final partial year if the 5-year mark was reached before or during it. - 'Vacation pay is payable on termination pay but not on severance pay.' - It is due within 7 days or on the next pay day, whichever is later.  The Manual says that when more than the ESA minimum is paid, vacation pay is owed only on the statutory part of the termination pay.  In Russell v. The Brick, a letter that accrued vacation pay only to the termination date fell below the ESA.  Also: https://www.ontario.ca/laws/statute/00e41#BK72 | [link](https://www.ontario.ca/document/your-guide-employment-standards-act-0/vacation) |
| Final-pay deadline (ESA s.11(5)) | Everything owing is due no later than the later of '(a) seven days after the employment ends; and (b) the day that would have been the employee's next pay day'. That covers final regular pay, termination pay, severance pay and vacation pay; under s.1, 'wages' include any payment the Act requires.  The Manual reads (b) as the very next pay day after the end date. Its example: employment ends January 22 and the pay days are January 31 and February 15, so everything is due January 31, not February 15.  The payment date stated in a letter must not be later than this.  Also: - https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-v-payment-wages - https://www.ontario.ca/document/your-guide-employment-standards-act-0/payment-wages | [link](https://www.ontario.ca/laws/statute/00e41#BK24) |
| Written statement of the termination amounts (ESA s.12.1) | On or before the s.11(5) date, the employer 'shall provide the employee with a written statement setting out': - (a) the gross termination or severance pay - (b) the gross vacation pay - (c) how (a) and (b) were calculated, unless the employee gets this some other way - (d)-(f) the pay period, wage rate and gross amount of any other wages, with the calculation - (g) each deduction and its purpose - (h) any room or board amount - (i) the net amount paid  The statement can be part of the letter (a payments table) or a separate final pay statement.  The ministry's employer guide pages don't mention this requirement; the Manual (Part V) does.  Also: https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-v-payment-wages | [link](https://www.ontario.ca/laws/statute/00e41#BK26) |
| ESA minimums can't be waived or made conditional on a release | ESA s.5(1): no one may contract out of or waive an employment standard, and any such waiver 'is void'. Manual Part III cites Lindzon v. Starr (1979), where a signed release was void and pay in lieu was still owed. A greater contractual benefit prevails (s.5(2)).  Cases: - Wilds v. 1959612 Ontario Inc., 2024 ONSC 3452: withholding ESA termination pay until a release came back violated s.54 and supported $10,000 in punitive damages. - Russell v. The Brick Warehouse LP, 2021 ONSC 4822: failing to say that ESA entitlements would be paid even if the offer was declined was a 'serious defect', and the court awarded $25,000 in moral damages.  The guide adds that an employee can't both sue for wrongful dismissal and file an ESA claim for termination or severance pay over the same termination.  In practice, the letter separates what is paid regardless from what depends on the release, and says so. HRPA: asking for a release without offering more than the minimums is wrongful and unenforceable.  Also: - https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-iii-how-act-applies - https://www.mannlawyers.com/resources/to-sign-or-not-to-sign-a-release/ - https://www.littler.com/news-analysis/asap/ontario-canada-court-awards-employee-25000-moralaggravated-damages-because | [link](https://www.ontario.ca/laws/statute/00e41#BK8) |
| No deductions from final pay, and no withholding it, without a specific written authorization (ESA s.13) | Wages can be withheld or deducted only if a statute or court order authorizes it, or with the employee's written authorization (s.13(1)-(3)).  The written authorization doesn't count (s.13(5)) if: - it 'does not refer to a specific amount or provide a formula' - the deduction is for faulty work - the deduction is for a cash shortage or for lost or stolen property that someone else had access to  The Manual says blanket authorizations are invalid.  So a line like 'the cost of unreturned equipment will be deducted from your final pay', or holding the cheque until keys come back, is unlawful without a valid prior authorization. The employer can instead make an above-ESA payment conditional on the property's return (HR Reporter, 2021).  Federal carriers fall under CLC s.254.1. MG Lund Trucking v. Petersen (FC 2008) and Donnelly Farms (2016) reversed deductions for retrieving a truck and for unreturned keys.  Also: - https://www.ontario.ca/laws/statute/00e41 (s.13) - https://www.hrreporter.com/chrr-plus/employment-law/getting-company-equipment-back-from-quitting-employee/356711 | [link](https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-v-payment-wages) |
| Non-compete covenants are void for non-executives (ESA s.67.2) | s.67.2(1): 'No employer shall enter into an employment contract or other agreement with an employee that is, or that includes, a non-compete agreement'. Such an agreement is void (s.67.2(2) and s.5(1)). The ban covers agreements made on or after Oct 25, 2021.  Exceptions: - a seller in a sale of business who becomes the buyer's employee - 'executives': CEO, president, CAO, COO, CFO, CIO, chief legal officer, CHRO, chief corporate development officer, or another chief executive position  Non-solicitation and confidentiality clauses are not caught. A letter can remind a coordinator, supervisor, driver or welder of confidentiality and non-solicitation duties, but not of a non-compete.  Also: https://www.ontario.ca/laws/statute/00e41#BK158 | [link](https://www.ontario.ca/document/your-guide-employment-standards-act-0/non-compete-agreements) |
| No reason is required; keep cause out of a without-cause letter | The guide: 'The ESA does not require an employer to give an employee a reason'. But a termination is a reprisal if any part of the reason is that the employee asked about or exercised ESA rights, including taking an ESA leave (s.74).  Only 'wilful misconduct, disobedience or wilful neglect of duty' that is not trivial and has not been condoned removes notice and termination pay (O. Reg. 288/01 s.2).  In Render v. ThyssenKrupp Elevator, 2022 ONCA 310, just cause was upheld but ESA pay was still owed, because 'careless, thoughtless, heedless, or inadvertent conduct' doesn't meet that standard.  A without-cause letter therefore pays the full ESA amounts and doesn't describe misconduct.  Also: https://www.siskinds.com/ontario-court-of-appeal-clarifies-distinction-termination-for-cause-and-wilful-misconduct-under-esa/ | [link](https://www.ontario.ca/document/your-guide-employment-standards-act-0/termination-employment) |
| Record of Employment: issue it on time, with separation payments shown | EI Regulations s.19(2): every employer must complete an ROE for an insured employee who has an interruption of earnings, meaning a separation followed by 7 or more consecutive days with no work and no earnings (s.14(1)). Service Canada says to issue it whether or not the employee plans to claim EI.  Deadlines: - Electronic ROE, weekly, biweekly or semi-monthly payroll: within 5 calendar days after the end of the pay period in which the interruption occurs. - Electronic ROE, monthly or 13-period payroll: the earlier of 5 calendar days after the period ends or 15 calendar days after the first day of the interruption (s.19(3.1)). - Paper ROE: within 5 calendar days of the later of the first day of the interruption and the day the employer learns of it (s.19(3)). - Salary continuance: 'do not issue an ROE until the end of the salary continuance period'. Block 11 then shows the last day of the continuance.  Separation payments: - Block 17C: 'Pay in lieu of notice' and 'Severance pay', each with its amount. - Block 17A: vacation pay paid because of the separation.  Service Canada asks employers to tell employees that the ROE is filed electronically, that they can view it in My Service Canada Account, and that they should apply for EI promptly.  Late ROEs counted against employers in Wilds (a month late), in Pohl, and in Morison v. Ergo-Industrial (2 months late; part of $50,000 in punitive damages). Fines go up to $2,000 (McCarthy).  Also: - https://www.canada.ca/en/employment-social-development/programs/ei/ei-list/reports/roe-guide.html - https://laws-lois.justice.gc.ca/eng/regulations/SOR-96-332/section-14.html | [link](https://laws-lois.justice.gc.ca/eng/regulations/SOR-96-332/section-19.html) |
| The ROE reason code must tell the same story as the letter | The codes: - Code A, shortage of work: 'Use this code when the employee is laid off'. The guide's non-exhaustive examples include end of contract or season, 'position eliminated/redundant', 'company restructuring', and employer bankruptcy or receivership. - Code M, dismissal or suspension: used 'when the employer initiates the separation from employment for any reason other than layoff'.  'It is a serious offence to misrepresent the reason for issuing an ROE'. Knowingly giving a false reason risks fines or prosecution.  Pairing: - A letter citing position elimination, restructuring or lost contracts fits Code A. - A bare without-cause dismissal, or one with a performance flavour, fits Code M.  Real mismatches: - Pohl: a permanent without-cause termination recorded as 'shortage of work/end of contract or season', with recall unknown. - Simes Law: Code A used for dismissals, and 'terminated for cause' comments on ROEs. - HR Reporter (2026): a code saying shortage of work alongside a comment saying the employee quit.  Also: - https://www.hrreporter.com/chrr-plus/employment-law/hbc-hit-with-moral-punitive-damages-after-bad-faith-treatment-of-employee/370514 - https://www.firstreference.com/blog/common-mistakes-on-a-record-of-employment-roe/ | [link](https://www.canada.ca/en/employment-social-development/programs/ei/ei-list/reports/roe-guide.html) |
| The payroll treatment behind 'less applicable statutory deductions' | CRA treatment by payment type: - Pay in lieu of notice 'is considered employment income': income tax, CPP and EI are withheld. - Severance is a retiring allowance: income tax only, with no CPP or EI. Outside Quebec it is withheld at lump-sum rates of 10% up to $5,000, 20% over $5,000 up to $15,000, and 30% over $15,000. - Vacation pay paid out is not a retiring allowance. - A lump sum that isn't broken down is generally treated entirely as a retiring allowance. That is another reason letters itemise.  RRSP transfers: - The non-eligible part of a retiring allowance can be paid straight into the employee's RRSP, up to their available room, with no tax withheld. - An 'eligible' transfer, which ignores contribution room, exists only for service before 1996.  These are payroll rules, not ESA rules. A letter only needs 'less applicable statutory deductions' and, optionally, a sentence offering to send severance to the employee's RRSP. ROE Block 17C also needs pay in lieu and severance shown separately.  Also: https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/payroll/payroll-deductions-contributions/special-payments/wages-lieu-termination-notice.html | [link](https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/payroll/calculating-deductions/determining-tax-treatment/retiring-allowances.html) |

## How letters differ by employer

**Owner-run small business with no HR (Orchard & Vine Catering Ltd., Burlington; Lakeshore Fabrication Inc., Stoney Creek; the owner signs both).** Form:
- The owner writes and signs it, often adapting a free vendor template (Key Media, Citation, Employment Hero) rather than using a lawyer's.
- Expect 1-2 pages (my inference), the incorporated name on the letterhead, a first-name salutation, and usually no 'Without Prejudice' unless the owner adds an offer.

Severance: usually none.
- It needs 5+ years and, for a single termination, a $2.5M payroll (s.64).
- Both clients are under 5 years anyway: Benoit about 2 years 4 months and Sandhu about 4 years 2 months on their files. The letter omits severance or says it doesn't apply.
- Termination pay, vacation pay (4% for both) and an ROE are always owed.

Benefits:
- A small employer may have no group plan. If there is one, coverage still runs to the end of the statutory notice period.
- If there isn't, the section is dropped (OCA note) or says there is none.

Pay basis:
- Salaried staff (the caterer): annual salary / 52 per week.
- Hourly trades (the welding shop): base hourly rate x regular weekly hours, with overtime excluded (s.1 'regular wages').
- Irregular hours: the 12-week average (s.61(1.1)).
- The letter shows the rate it used, so a rate dispute surfaces in the letter itself. Sandhu: $29.50 on the pay stub and the signed scan, against $31.00 claimed.

Property:
- Welding shop: shop keys or fob, company tools, PPE and uniforms.
- Caterer: keys, uniforms and any company phone.
- The research flags 'unreturned items will be deducted from your final cheque' as a realistic owner-written flaw. It is unlawful under ESA s.13 without a specific prior written authorization.

Documented small-employer failure modes:
- ESA pay withheld until a release is signed, plus a late ROE and no reference (Wilds; the employer was a numbered Ontario company).
- 'For cause, nothing owed' for conduct short of wilful misconduct (Render).
- Deductions for tools, uniforms or cash shortages (s.13).
- A 'temporary layoff' with no right to lay off (Chea).
- Notice by text message, which is not an s.95 method.
- Small-business guidance (Xero) still tells owners to put the end date, pay details, a final-pay breakdown and benefit end dates in writing.

My inference from the research: a realistic owner-written letter can be short, but it is short and wrong in specific, checkable ways, such as no payment date, no vacation pay on the termination pay, benefits ending on the last day, or a deduction threat. It is rarely short and correct, and never as bare as 'your final payment will be processed in the ordinary course'.

Reason: one plain sentence, such as lost corporate contracts or a slowdown in orders. Position elimination pairs with ROE Code A.

No source says how often owner-written letters include a release or recommend independent legal advice.

**Mid-size employer with an HR function (Northwind Logistics Inc., Mississauga; signed by the Director of People).** Form:
- HR adapts a company template, signed by the Director of People or the HR Manager. Expect 2-4 pages (my inference).
- Typical contents:
  - 'Personal & Confidential' and a Re: line
  - numbered or bulleted entitlements with amounts and dates, and a final-pay summary
  - an end date and conversion window for each benefit
  - RRSP/DPSP and bonus treatment
  - an itemised property list with a return method
  - an ROE paragraph, a named HR contact, and enclosures
- If HR wants a release, the letter is two-tier and marked 'Without Prejudice', with a release schedule, a deadline of about a week, a recommendation to get legal advice, and the 'paid regardless' sentence.

The model cases are both HR-run employers:
- Russell v. The Brick: a templated letter, a 3-day deadline, no 'ESA paid regardless' sentence, most benefits not extended, and vacation pay only to the termination date.
- Pohl v. HBC: ESA termination pay paid bi-weekly, an offer conditional on resigning, and a late ROE coded shortage of work with recall unknown.
- Polish doesn't prevent errors. A realistic HR letter can be well formatted and still wrong.

Severance is live: a logistics company will usually clear the $2.5M payroll test, so anyone with 5+ years of total service gets an ESA severance line.

Service traps (rehires and leaves):
- Notice counts only from the latest start date if a gap was longer than 13 weeks (O. Reg. 288/01 s.8).
- Leave counts toward notice (s.59(1)).
- Severance counts all time with the employer (s.65(2)) plus the unworked notice weeks (s.65(4)).
- Okonkwo: a 2016 contract, a prior ROE issued in 2021, rehired March 14, 2022, with prior service recognised 'for vacation entitlement only'.
- ?? Was his 'year out' a separation (the 2021 ROE suggests so) or a leave? That decides his notice. The 2016-2021 stint counts toward severance either way.
- ?? The current draft gives 2 weeks' notice, but 3 years 5 months from March 14, 2022 is 3 weeks under s.57. Keep 2 weeks only as a deliberate seed.

Bonus:
- HR letters say what happens to the bonus (HRPA).
- A discretionary bonus not tied to hours, production or efficiency isn't ESA 'wages' (s.1), so the letter states the plan outcome rather than adding it to termination pay.

Contract clause:
- HR letters cite the termination clause relied on (the Key Media pattern). Here that is the 2022 contract's 'minimum notice required by the ESA'.
- Whether the clause is enforceable is a question for the lawyer (Achkar; HRXconnect on Waksdale; Henderson v. Slavkin).

Property: laptop, access card, phone, keys or fob, corporate card and documents, with a date and a courier or drop-off method. The current draft already names the laptop and access card and gives a date.

**Multi-clinic dental group after a merger (Castleford Dental Group, Oakville; signed by the Practice Manager).** Form:
- Written by the practice manager or group HR, often from a clinic template like the OCA/MaRS one. That template has:
  - a 'Strictly Confidential' marking, plus 'Without Prejudice' if there is an offer
  - a short cover letter
  - a numbered 'Termination Agreement' appendix covering the termination date, notice, severance, vacation, group benefits with life conversion, an additional payment for a release, expenses, the ROE, change of address for the T4, references, return of property, and the release deadline
  - a release
- Modernise its dated parts: 'HRSDC', 'present this form', and 'inclusive of any payments... under the ESA'.

Merger rules:
- Staff who move to a buyer keep their service with the seller for ESA purposes, unless they were hired more than 13 weeks after leaving the seller or after the sale (s.9; the guide's continuity page).
- At common law, prior service is weighed rather than automatically added on (Manthadi v. ASCO).
- Group payroll will probably clear $2.5M, so staff with 5+ years of combined service get ESA severance.
- Whitfield was hired by Castleford itself on January 11, 2021, so s.9 doesn't change her count. Her 4 years 8 months gives 4 weeks' notice, 4% vacation pay and no severance, even with the 4 notice weeks added under s.65(4).

Reason:
- 'The role was duplicated following the merger' is a neutral business reason and pairs with ROE Code A (position eliminated/redundant).
- Don't mention the 2023 lateness warning.

Employer identity:
- The letterhead entity should match payroll and the ROE.
- ?? No source covered multi-entity dental groups (each clinic as its own corporation, trade names) or the ESA s.4 related-employer rule.

Access and property:
- Keys and access cards.
- Removal of access to the practice-management system, email, shared files and remote access, coordinated with the IT provider (CDA Oasis checklist).
- ?? No source found for PHIPA wording in staff termination letters.

Covenants: non-competes are void for patient coordinators, hygienists and assistants (s.67.2). Confidentiality and non-solicitation can be restated.

Contract risk:
- ESA-only termination clauses introduced around acquisitions often fail. Henderson v. Slavkin, 2022 ONSC 2964: a dental receptionist with 30 years' service was owed 18 months.
- Buyers scrutinise staff contracts, and sellers often share termination costs (Oral Health Group).
- There's no implied right to lay off after a merger (Chea v. CIMA).

**Trucking carrier (Bellweather Freight, Hamilton; HR department; long-haul driver paid by the mile).** Jurisdiction comes first (rule 1):
- An extra-provincial carrier is federal (Canada Labour Code). An Ontario-only carrier is provincial (ESA).
- If federal, the letter cites the CLC instead:
  - notice: 5 weeks at 5 years, 6 at 6, the same as the ESA from 3 years up
  - CLC severance: the greater of 2 days' wages per completed year or 5 days' wages
  - the written statement of benefits, due on the termination date when paying in lieu
- A driver letter citing the ESA for an extra-provincial carrier is a realistic mismatch. ?? Fixture decision.

Service:
- He started in 2019 (month unknown) and was terminated July 18, 2025. That gives 5 or 6 weeks' notice depending on the start month, and 6% vacation pay under the ESA once 5 years is reached.
- With no written contract, the employer's letter states its own start date or service figure. That is the fact the intake check compares with the client's 'sometime in 2019'.
- No written contract also means no clause limiting him to ESA minimums, so common-law notice can apply (BrightHR). The ESA amounts are the floor.

Pay basis:
- Mileage is pay 'on a basis other than time'. ESA termination pay, and severance (s.65(6)), therefore use the average regular wages over the weeks worked in the 12 weeks before termination (s.61(1.1)).
- The letter should name the averaging period and the weekly figure.
- ?? I didn't check whether layover pay counts as regular wages or as a travelling allowance, which is excluded from 'wages' (s.1).

Severance: likely owed under the ESA. A carrier with a driver fleet will usually clear $2.5M, and he has 5+ years.

Termination by phone:
- The letter confirms the call ('further to our telephone conversation of July 18, 2025').
- Oral notice doesn't count unless it is longer than the minimum and date-specific, so an immediate termination means pay in lieu.

Property and systems:
- fuel card, deactivated the same day
- toll or weigh-station bypass transponder
- ELD tablet or company phone
- terminal gate fob and yard keys
- hazmat security key, if he holds the endorsement
- uniforms
- tractor and trailer returned to the terminal
- registration and insurance cards
- These items come from US-oriented offboarding checklists (Manifestly; Automotive Fleet). I found no Canadian trucking termination template.
- Offboarding also exports the driver's ELD records of duty status; no source shows letters mentioning it. Ontario has required certified ELDs since June 12, 2022.

Deductions:
- No holding the final cheque until keys come back, and no charges for retrieving the truck, without a valid written authorization (ESA s.13 or CLC s.254.1).
- MG Lund: a $0 final cheque, and a $300 key clause the court called 'a drastic additional penalty'.
- Donnelly Farms: an $831.20 deduction reversed.

Cause:
- The 'conversations about logbook errors' are a cause theme. A without-cause letter shouldn't mention them.
- If the carrier is federal, a driver with 12+ months can complain of unjust dismissal and ask for written reasons.

Records access: his payroll portal access was cut the same day. HRPA's checklist includes continued access to pay statements through an alternate email.

**Large employer or executive, drafted by counsel (not one of the five; use only to calibrate).** The EDGAR letters show the top end:
- Li-Cycle 2024: about 8 pages.
- WW Canada 2024: about 7 pages plus a 3-page release.
- CA Canada 2014: about 5-6 pages.

What they contain:
- defined terms throughout ('Separation Date', 'Working Notice Period', 'Released Parties')
- references to clauses of the employment agreement
- working notice that satisfies the ESA
- salary continuance (Li-Cycle: 18 months, not subject to mitigation)
- RRSP participation ending with the statutory notice period
- lump sums in lieu of benefits and the RRSP match
- bonus and equity treatment
- outplacement and a legal-fee contribution
- an expense deadline
- an ROE 'sent directly to Service Canada'
- confidentiality of terms and non-disparagement
- resignation of directorships
- non-competes, which are lawful for executives under s.67.2
- an indemnity in the release

Don't borrow the executive-only terms for these five letters: directorships, non-disparagement, litigation cooperation, D&O indemnity, clawback, a non-compete appendix, or long salary continuance. Use the structure, never the names or figures.

## Flaws real letters often contain

Useful for deliberately realistic imperfection.

- Payment language with no figures or dates: 'your final payment will be processed in the ordinary course', 'all amounts owing', 'in accordance with the ESA'. Achkar says failing to set out final entitlements accurately is 'one of the most common ESA violations'. ESA s.12.1 requires gross amounts and the calculation in writing by the final-pay date. (https://achkarlaw.com/insights/ontario/how-to-write-a-termination-letter/ ; https://www.ontario.ca/laws/statute/00e41#BK26)
- ESA pay made conditional on the release, e.g. 'the amounts below will be paid on receipt of your signed release'. This breaches ESA s.5 and s.54. Wilds v. 1959612 Ontario Inc., 2024 ONSC 3452: $10,000 in punitive damages, alongside a month-late ROE, unreimbursed expenses and no reference letter. (https://www.mannlawyers.com/resources/to-sign-or-not-to-sign-a-release/ ; https://www.littler.com/news-analysis/asap/ontario-canada-court-finds-termination-provisions-unenforceable-and-awards)
- An offer letter, marked without prejudice, open 3 days and conditional on a release, that never says the ESA amounts will be paid if the offer is declined. Russell v. The Brick Warehouse, 2021 ONSC 4822 called this a 'serious defect' and awarded $25,000 in moral damages. (https://www.littler.com/news-analysis/asap/ontario-canada-court-awards-employee-25000-moralaggravated-damages-because)
- Pressure deadlines: 'sign by Friday', 48 hours, or a signature at the meeting. Employee-side lawyers call them 'a pressure tactic, not a legal ultimatum'. HRXconnect lists an on-the-spot release as a mistake, and Amar-VR recommends at least 5 business days. (https://www.ullaw.ca/resource/fired-ontario-asked-sign-release-deadline ; https://hrxconnect.com/hr-consulting/termination-letter-ontario/)
- Benefits ending on the last day worked even though pay in lieu is paid ('your group benefits will end on your termination date'). This breaches ESA s.61(1)(b), and Achkar and HRXconnect both list it as a common error. ?? HRXconnect's own template also offers ending coverage on the termination date with a cash premium payment. That sits uneasily with s.61(1)(b) and with HRXconnect's own mistakes list, though no source tests it, so avoid it for the statutory period. WW used a premium lump sum only for the contractual period after statutory notice had been worked. (https://achkarlaw.com/insights/ontario/termination-letters/ ; https://hrxconnect.com/hr-consulting/termination-letter-ontario/)
- Partial or undisclosed benefit continuation: health and dental to a date, but LTD, life, AD&D or the group RRSP/DPSP stopped, or benefits extended without telling the employee (Russell). If the insurer refuses to continue LTD or life coverage, the employer carries the risk (Egan v. Alcatel; Brito v. Canac). (https://www.hrreporter.com/chrr-plus/employment-law/benefits-during-the-notice-period/315968 ; https://hrinsider.ca/3-traps-to-avoid-when-writing-a-termination-letter/)
- Vacation pay 'accrued to the date of termination' only, with nothing on the termination pay (Russell). Key Media's May 2025 template words its vacation bullet the same way, so letters built from it repeat the error. (https://www.littler.com/sites/default/files/russell_v_the_brick_warehouse.pdf ; https://cdn-res.keymedia.com/cms/files/ca/126/0394_638847362834755553.pdf)
- Wrong vacation rate or base: 4% after the 5-year mark, vacation pay added to severance, or vacation pay left off the termination pay. (ESA s.35.2; https://www.ontario.ca/document/your-guide-employment-standards-act-0/vacation)
- Notice weeks that don't fit the table, usually because service was counted from the wrong date: a rehire date when the gap was 13 weeks or less, leave left out, or an acquisition date used instead of the original hire date (O. Reg. 288/01 s.8; ESA s.59 and s.9). Achkar lists wrong service length and wrong base rate among the usual errors. (https://achkarlaw.com/insights/ontario/termination-letters/)
- Severance missed or understated: none paid to a 5+ year employee of a $2.5M employer, earlier stints left out (s.65(2)), or unworked notice weeks not added (s.65(4)). In Halloran v. Crown Cork (ONCA 2002), a package described as 'inclusive of all amounts payable under any provincial legislation' left out ESA severance. (https://www.hrreporter.com/chrr-plus/employment-law/employers-must-provide-accurate-information/318942)
- The opposite error: severance, or an inflated 'ESA' figure, for someone not entitled to it. Stowar v. Telehop (2009): the employer offered 5 months 'as per our obligation under the ESA' when 3 weeks was the minimum. The employee signed, and the employer was held to it. (https://www.hrreporter.com/chrr-plus/employment-law/employer-bound-by-payments-outlined-in-termination-letter/319181)
- Termination pay on the wrong base: overtime folded into regular wages, or a flat rate used for a mileage-paid driver or variable-hours worker instead of the 12-week average (ESA s.1, s.61(1.1)). (https://www.ontario.ca/laws/statute/00e41#BK146)
- ESA termination pay paid as salary continuance or bi-weekly instalments, or stopped when the employee finds new work. Pohl v. Hudson's Bay Co., 2022 ONSC 5230 called bi-weekly payment 'entirely unacceptable' and awarded $45,000 moral and $10,000 punitive damages. ESA amounts aren't subject to mitigation. (https://www.grosman.com/blog/employment-law/wrongful-dismissal/court-offers-another-warning-to-employers-to-take-care-when-dismissing-employees-without-cause/ ; https://lawofwork.ca/can-an-employer-pay-severance-pay-by-continuation-of-salary-rather-than-a-lump-sum/)
- A payment date later than ESA s.11(5) allows, e.g. 'paid over the next two pay cycles', or 'with the month-end payroll' when an earlier pay day comes first. HRXconnect lists late final pay as a mistake, and the Manual reads s.11(5) as the very next pay day. (https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-v-payment-wages)
- Cause language in a without-cause letter: citing warnings, lateness, performance or logbook errors (Achkar calls these 'inadvertent admissions'), or 'terminated for cause, nothing is owed' where the conduct isn't wilful misconduct (Render v. ThyssenKrupp, 2022 ONCA 310). HRXconnect also lists claiming cause without meeting the threshold, and being verbose about reasons. (https://achkarlaw.com/insights/ontario/how-to-write-a-termination-letter/ ; https://www.siskinds.com/ontario-court-of-appeal-clarifies-distinction-termination-for-cause-and-wilful-misconduct-under-esa/)
- Mentioning a protected ground or leave, or terminating during or because of a protected leave (HRXconnect mistakes 2 and 10; ESA reprisal, s.74). Where the employee recently disclosed a pregnancy or disability, careful letters say the decision is unrelated (Rudner). (https://hrxconnect.com/hr-consulting/termination-letter-ontario/ ; https://www.hrreporter.com/chrr-plus/employment-law/information-in-termination-letter/317638)
- An ROE that contradicts the letter or arrives late: shortage of work with 'recall unknown' on a permanent termination (Pohl); 'terminated for cause' comments when the letter says without cause (Simes Law); code and comment boxes that disagree (HR Reporter, 2026); or an ROE weeks late (Wilds: a month; Morison: 2 months). (https://www.firstreference.com/blog/common-mistakes-on-a-record-of-employment-roe/ ; https://www.hrreporter.com/focus-areas/payroll/when-the-roe-is-wrong/394706 ; https://www.mccarthy.ca/en/insights/blogs/canadian-employer-advisor/record-of-employment-a-reminder-of-the-need-for-timeliness-and-accuracy)
- Threatening deductions or holding pay for property: 'unreturned equipment will be deducted from your final pay', or the final cheque held until keys come back. This breaches ESA s.13 (CLC s.254.1 for federal employers). In MG Lund Trucking, the carrier issued a $0 final cheque after deducting truck-return costs, and the decision called a $300 key clause 'a drastic additional penalty'. Achkar adds that vague property clauses are hard to enforce. (https://www.hrreporter.com/email-article/6486-contract-can-impose-fees-but-not-wage-deductions-court-says/ ; https://achkarlaw.com/insights/ontario/wage-deductions/)
- A non-compete reminder to a non-executive ('you remain bound by the non-competition covenant in your agreement'). Such covenants are void under ESA s.67.2 for agreements made on or after Oct 25, 2021, and HRXconnect lists the reminder as a mistake. (https://www.ontario.ca/document/your-guide-employment-standards-act-0/non-compete-agreements)
- Paying only ESA minimums on the strength of an 'ESA-only' termination clause that won't hold. Henderson v. Slavkin, 2022 ONSC 2964: a dental receptionist's clause failed because of the contract's confidentiality and conflict-of-interest clauses, and 18 months' notice was owed. HRXconnect warns about clauses not reviewed since Waksdale. (https://hicksmorley.com/2022/08/24/court-finds-esa-only-termination-clause-unenforceable-due-to-wording-of-conflict-of-interest-and-confidential-information-clauses/)
- Notice given only by phone or text, or with no verifiable delivery. ESA s.95 lists in person, verified mail, fax or email, courier, and a sealed envelope; text isn't on the list, and HRXconnect lists text-only or email-only delivery as a mistake. A 2013 view that email never counts is outdated: the current guide accepts email if delivery can be verified. (https://www.ontario.ca/laws/statute/00e41#BK243 ; https://www.ontario.ca/document/your-guide-employment-standards-act-0/termination-employment)
- Template leftovers that date the letter or contradict the law: 'HRSDC'; 'present this form' for the ROE; 'ROE within five days of your last payment'; 'the ROE will note that your employment was terminated without cause' (there is no such code); a package 'inclusive of' ESA amounts with no breakdown. In Russell, obvious template use had 'a multiplying effect' on the letter's flaws. (https://chiropractic.on.ca/wp-content/uploads/Termination-Agreement-Template.doc ; https://cdn-res.keymedia.com/cms/files/ca/126/0394_638847362834755553.pdf ; https://hrinsider.ca/3-traps-to-avoid-when-writing-a-termination-letter/)
- A layoff letter for a permanent job loss ('you are being laid off; no recall date has been set'). A layoff longer than the ESA temporary limit (13 weeks in any 20, s.56(2)) is a termination dated to the first day of the layoff (s.56(5)). There is also no implied right to lay off at common law (Chea v. CIMA, a firm formed by a merger). (https://www.hrreporter.com/chrr-plus/employment-law/no-implied-right-to-or-expectation-of-layoffs-for-ontario-employer/319391)
- Two-tier letters with loose release terms: no deadline or method of acceptance (Vey Willetts says to set out both), no recommendation to get independent legal advice, or letter wording that conflicts with the release (Achkar). (https://hrinsider.ca/tips-on-the-right-way-to-fire-employees-in-ontario/ ; https://achkarlaw.com/insights/ontario/how-to-write-a-termination-letter/)
- An employee signature block on a letter that only pays the minimums. The OCA template says to remove it, and Stowar shows a signed letter can become part of the contract. (https://chiropractic.on.ca/wp-content/uploads/Termination-Agreement-Template.doc)

## Sources

| Source | Used for |
|---|---|
| [Employment Standards Act, 2000, S.O. 2000, c. 41 (e-Laws consolidation from 2026-01-01; last amendment 2025, c. 13)](https://www.ontario.ca/laws/statute/00e41) | Rules 2-15. Sections: s.1 'wages' and 'regular wages', s.5, s.9, s.11(5), s.12.1, s.13, s.35.2, s.38, s.54, s.56, s.57, s.59-62, s.64-66, s.67.2, s.74 and s.95. I re-checked the section text on 2026-10-14 by streaming the e-Laws Word export (https://www.ontario.ca/laws/docs/00e41_e.doc) into memory. The 2025 amendments did not change the sections used. The harness auto-saved one long excerpt of that output to this session's tool-results folder (bz06p5mcj.txt). |
| [O. Reg. 288/01: Termination and Severance of Employment (consolidation from 2025-07-01; last amendment O. Reg. 116/25)](https://www.ontario.ca/laws/regulation/010288) | s.2 exemptions, s.4(1) form and service of notice, s.6, s.7 (vacation inside the notice period) and s.8 (period of employment and the 13-week rule). Re-checked by streaming the e-Laws Word export (https://www.ontario.ca/laws/docs/010288_e.doc) into memory. |
| [Termination of employment / Your guide to the Employment Standards Act (updated 2026-07-23)](https://www.ontario.ca/document/your-guide-employment-standards-act-0/termination-employment) | Notice table, delivery methods, duties during notice, lump-sum termination pay and the $800 example, 12-week averaging, payment deadline, no reason required, wilful misconduct exemption, and how leave and gaps count. Re-checked 2026-10-14. |
| [Severance pay / Your guide to the Employment Standards Act (updated 2026-03-18)](https://www.ontario.ca/document/your-guide-employment-standards-act-0/severance-pay) | Eligibility, including service counted 'whether continuous or not and whether active or not'; global payroll; the formula and 26-week cap; the Alex example, where notice weeks count toward service; deadline; instalments. Re-checked 2026-10-14. |
| [Vacation / Your guide to the Employment Standards Act (updated 2026-02-05)](https://www.ontario.ca/document/your-guide-employment-standards-act-0/vacation) | Vacation pay at 4% or 6%; payable on termination pay but not on severance; all unpaid vacation pay owed; the final-partial-year rule; deadline. |
| [Payment of wages / Your guide to the Employment Standards Act (updated 2024-07-08)](https://www.ontario.ca/document/your-guide-employment-standards-act-0/payment-wages) | Final pay deadline when employment ends; limits on deductions. |
| [Continuity of employment / Your guide to the Employment Standards Act](https://www.ontario.ca/document/your-guide-employment-standards-act-0/continuity-employment) | Sale-of-business service credit and the 13-week exception (dental group merger context). |
| [Non-compete agreements / Your guide to the Employment Standards Act](https://www.ontario.ca/document/your-guide-employment-standards-act-0/non-compete-agreements) | Non-compete ban from Oct 25, 2021; executive and sale-of-business exceptions; non-solicits and NDAs allowed. |
| [ESA Policy and Interpretation Manual: O. Reg. 288/01 (updated 2026-05-06)](https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/ontario-regulation-28801-termination-and-severance-employment) | Program policy that the notice must specify the termination date; when oral notice counts. |
| [ESA Policy and Interpretation Manual: Part XV (updated 2023-04-25)](https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-xv-termination-and-severance-employment) | Benefit contributions include the employee's share; termination pay is not reduced by new earnings; vacation pay is owed only on the statutory part; global payroll (Hawkes v. Max Aicher); scope of the non-compete ban. |
| [ESA Policy and Interpretation Manual: Part V - Payment of wages (updated 2023-04-25)](https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-v-payment-wages) | s.12.1 statement on termination; s.11(5) 'very next pay day' example (Jan 22 / Jan 31); s.13 authorizations must state an amount or formula, and blanket authorizations are invalid. Re-checked 2026-10-14. |
| [ESA Policy and Interpretation Manual: Part III - How this Act applies](https://www.ontario.ca/document/employment-standard-act-policy-and-interpretation-manual/part-iii-how-act-applies) | s.5 no contracting out; Lindzon v. Starr (release void, pay in lieu still owed). |
| [Employers: How to complete the record of employment (ROE) form (Service Canada)](https://www.canada.ca/en/employment-social-development/programs/ei/ei-list/reports/roe-guide.html) | ROE deadlines; Code A and its examples (position eliminated/redundant, company restructuring); Code M; the misrepresentation offence; salary continuance and Block 11; Block 17 separation payments; what to tell employees. Code wording and deadlines re-checked 2026-10-14. |
| [Employment Insurance Regulations, s.19 (Record of Employment)](https://laws-lois.justice.gc.ca/eng/regulations/SOR-96-332/section-19.html) | Duty to issue an ROE; paper and electronic deadlines. |
| [Employment Insurance Regulations, s.14 (interruption of earnings)](https://laws-lois.justice.gc.ca/eng/regulations/SOR-96-332/section-14.html) | Definition of an interruption of earnings: 7+ consecutive days with no work and no earnings. |
| [Payments of wages in lieu of termination notice (CRA)](https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/payroll/payroll-deductions-contributions/special-payments/wages-lieu-termination-notice.html) | Pay in lieu is employment income, with tax, CPP and EI withheld; an undivided lump sum is treated as a retiring allowance. |
| [Payments of retiring allowances (CRA)](https://www.canada.ca/en/revenue-agency/services/tax/businesses/topics/payroll/calculating-deductions/determining-tax-treatment/retiring-allowances.html) | Severance taxed as a retiring allowance at 10/20/30% lump-sum rates; no CPP or EI; RRSP transfers; eligible portion only for pre-1996 service. |
| [List of federally regulated industries and workplaces](https://www.canada.ca/en/services/jobs/workplace/federally-regulated-industries.html) | Interprovincial and international trucking is federally regulated (jurisdiction check for Bellweather). |
| [Termination, layoff or dismissal (federal labour standards)](https://www.canada.ca/en/services/jobs/workplace/federal-labour-standards/termination.html) | CLC notice, severance, statement of benefits, unjust dismissal and written reasons. |
| [Terminating a Federally Regulated Employee? New Requirements (HR Insider / Filion Wakely, 2024)](https://hrinsider.ca/terminating-a-federally-regulated-employee-new-requirements-that-employers-need-to-know/) | CLC graduated notice from Feb 1, 2024; timing of the written statement of entitlements. |
| [Transportation: Operating in Canada's freight, logistics, and transportation sector (Miller Thomson, 2026)](https://www.millerthomson.com/en/insights/publications/doing-business-in-canada/transportation-operating-in-canadas-freight-logistics-and-transportation-sector/) | An Ontario-only carrier is provincial; a carrier crossing borders 'regularly and continuously' is under the CLC. |
| [Canada Labour Code s.254.1](https://laws-lois.justice.gc.ca/eng/acts/L-2/section-254.1.html) | Federal limits on wage deductions (trucking context). |
| [Termination Without Cause Letter Template (unbranded; hosted on Key Media's CDN; file metadata 22 May 2025)](https://cdn-res.keymedia.com/cms/files/ca/126/0394_638847362834755553.pdf) | Read in full. Section order and wording patterns for the anatomy; how a 2025 template frames pay in lieu, benefits to the end of notice, vacation, severance 'if applicable', ROE, the release offer, property, continuing obligations and the close. Its flawed lines ('ROE will note... without cause'; vacation only to the termination date) are listed under flaws. WebFetch auto-cached the PDF in this session's tool-results folder; I extracted the text in memory with PDFKit. |
| [Sample Termination Template (Ontario Chiropractic Association; credited to proLearning innovations)](https://chiropractic.on.ca/wp-content/uploads/Termination-Agreement-Template.doc) | Read in full (streamed into memory). Clinic two-tier structure: cover letter, 12-section agreement, release contents, and the notes to remove severance, benefits or the signature field. Dated wording (HRSDC, 'present this form', 'inclusive of' ESA amounts). |
| [Sample Termination Agreement (MaRS Startup Toolkit, c. 2011)](https://learn.marsdd.com/wp-content/uploads/2011/12/Sample-Termination-Agreement.doc) | Parent of the OCA template; word counts for length calibration (via the research). |
| [How to Write a Termination Letter (With Samples) (Citation Canada, Jan 2024)](https://www.citationcanada.com/blog/article/how-to-write-a-letter-of-termination-with-samples/) | Section order; 'Notwithstanding the foregoing' release paragraph; about a one-week deadline; declining keeps statutory entitlements; ROE, property, belongings, outplacement and contact paragraphs; closing style. Re-checked 2026-10-14. |
| [How to Write a Termination Letter in Ontario: A Complete Employer Guide (HRXconnect, 2025-26)](https://hrxconnect.com/hr-consulting/termination-letter-ontario/) | 11-section template; the date as the key element; 'less is more' on reasons; its list of 10 common mistakes; the benefits premium-payment option flagged under flaws. Re-checked 2026-10-14. |
| [Termination of employment letter template (Employment Hero, Canada)](https://employmenthero.com/en-ca/resources/termination-of-employment-letter/) | The thin floor (a four-row without-cause sample); 31-day life conversion; ROE within 5 days. |
| [How to Write a Termination Letter in Ontario That Will Hold Up If Challenged (Achkar Law)](https://achkarlaw.com/insights/ontario/how-to-write-a-termination-letter/) | Six-part annotated sample; 'inadvertent admissions'; inaccurate entitlements as a common ESA violation; property and contact clauses; enforceable obligations only. |
| [Termination Letter in Ontario: Before You Sign (Achkar Law)](https://achkarlaw.com/insights/ontario/termination-letters/) | Employee-side red flags: ESA pay tied to a release, severance missed, wrong service or rate, benefits cut on the last day, no legal deadline. |
| [Wage Deductions in Ontario (Achkar Law, 2026)](https://achkarlaw.com/insights/ontario/wage-deductions/) | Deductions for tools, uniforms and damaged equipment need a prior written authorization stating the amount. |
| [Termination Without Cause in Ontario: An Employer's Guide (Mayo Law)](https://mayo.law/articles/termination-without-cause-in-ontario/) | The ESA prescribes little letter content beyond the notice; state how each amount was calculated and when it's paid; the ROE as a filing duty. |
| [How to Comply with Ontario's Termination and Severance Rules (AMAR-VR Law, 2025)](https://amarvrlaw.com/how-to-comply-with-ontarios-termination-and-severance-rules/) | Release-linked extras; at least five business days for legal advice. |
| [Are You About to Dismiss an Employee? Here is a Checklist to Review First (Blaney McMurtry)](https://www.blaney.com/articles/are-you-about-to-dismiss-an-employee-here-is-a-checklist-to-review-first) | Bonus, commission, pension, RRSP and loan items; continuance vs lump sum; mitigation; property and reference handling. |
| [With or Without Prejudice? (WeirFoulds, 2017)](https://www.weirfoulds.com/with-or-without-prejudice) | Ramos v. Hewlett-Packard: the label isn't decisive. |
| [A Cautionary Tale for Employers: Russell v The Brick Warehouse LP (WeirFoulds, 2021)](https://www.weirfoulds.com/a-cautionary-tale-for-employers-russell-v-the-brick-warehouse-lp) | Lessons from Russell: state what is paid if the offer is declined, disclose that benefits continue, pay where the employee directs (RRSP). |
| [Ontario Court Awards Employee $25,000 Moral/Aggravated Damages (Littler, 2021)](https://www.littler.com/news-analysis/asap/ontario-canada-court-awards-employee-25000-moralaggravated-damages-because) | Russell v. The Brick facts: 3-day deadline, no ESA-regardless sentence, benefits not extended, vacation only to the termination date, template use. |
| [Russell v. The Brick Warehouse LP, 2021 ONSC 4822 (decision text hosted by Littler)](https://www.littler.com/sites/default/files/russell_v_the_brick_warehouse.pdf) | Letter details: benefit carve-outs, 31-day life conversion, the employee's RRSP and reference requests. |
| [Ontario Court Finds Termination Provisions Unenforceable and Awards Punitive Damages (Littler, 2024)](https://www.littler.com/news-analysis/asap/ontario-canada-court-finds-termination-provisions-unenforceable-and-awards) | Wilds: ESA pay withheld pending a release, ROE a month late, expenses unreimbursed, no reference; $10,000 punitive damages. |
| [Wilds v. 1959612 Ontario Inc. (Cassels, 2024)](https://cassels.com/?p=19609) | Conditioning ESA pay on a release breaches the ESA; termination clauses failed. |
| [To Sign or Not to Sign (a Release)? (Mann Lawyers, 2024)](https://www.mannlawyers.com/resources/to-sign-or-not-to-sign-a-release/) | The quote from Wilds that the ESA obligation isn't contingent on a release (s.54). |
| [Court offers another warning to employers (Pohl v. Hudson's Bay Co., 2022 ONSC 5230)](https://www.grosman.com/blog/employment-law/wrongful-dismissal/court-offers-another-warning-to-employers-to-take-care-when-dismissing-employees-without-cause/) | Bi-weekly ESA termination pay 'entirely unacceptable'; late, wrong ROE; $45k moral and $10k punitive damages. |
| [HBC hit with moral, punitive damages after bad-faith treatment of employee (Canadian HR Reporter, 2022)](https://www.hrreporter.com/chrr-plus/employment-law/hbc-hit-with-moral-punitive-damages-after-bad-faith-treatment-of-employee/370514) | Pohl's ROE coded shortage of work/end of contract or season with recall unknown. |
| [Employers must provide accurate information (Halloran v. Crown Cork, ONCA 2002)](https://www.hrreporter.com/chrr-plus/employment-law/employers-must-provide-accurate-information/318942) | An 'inclusive of all amounts payable under any provincial legislation' package that left out ESA severance. |
| [Employer bound by payments outlined in termination letter (Stowar v. Telehop, 2009)](https://www.hrreporter.com/chrr-plus/employment-law/employer-bound-by-payments-outlined-in-termination-letter/319181) | An overstated 'ESA' figure bound the employer once the employee signed the letter. |
| [Benefits during the notice period (Canadian HR Reporter, 2017)](https://www.hrreporter.com/chrr-plus/employment-law/benefits-during-the-notice-period/315968) | Benefit continuation covers health, dental, life, LTD and STD; the employer is liable if the insurer refuses (Egan; Brito). |
| [Getting company equipment back from quitting employee (Canadian HR Reporter, 2021)](https://www.hrreporter.com/chrr-plus/employment-law/getting-company-equipment-back-from-quitting-employee/356711) | Deductions need specific written authorization; an above-statutory payment can be conditional on returning property. |
| [Contract can impose fees but not wage deductions, court says (MG Lund Trucking v. Petersen, 2008 FC)](https://www.hrreporter.com/email-article/6486-contract-can-impose-fees-but-not-wage-deductions-court-says/) | $0 final cheque; the $300 key-retention clause called 'a drastic additional penalty'. |
| [Employer ordered to pay back money deducted to retrieve company vehicle (Donnelly Farms, 2016)](https://www.hrreporter.com/chrr-plus/employment-law/employer-ordered-to-pay-back-money-deducted-to-retrieve-company-vehicle/315777) | $831.20 truck-retrieval deduction reversed. |
| [No implied right to or expectation of layoffs for Ontario employer (Chea v. CIMA Canada, 2016)](https://www.hrreporter.com/chrr-plus/employment-law/no-implied-right-to-or-expectation-of-layoffs-for-ontario-employer/319391) | A layoff without a contractual right is constructive dismissal; post-merger context. |
| [When the ROE is wrong (Canadian HR Reporter, 2026)](https://www.hrreporter.com/focus-areas/payroll/when-the-roe-is-wrong/394706) | ROE code and comment box contradicting each other. |
| [Information in termination letter (Canadian HR Reporter, Stuart Rudner, 2013)](https://www.hrreporter.com/chrr-plus/employment-law/information-in-termination-letter/317638) | No duty to give reasons; say the decision is unrelated after a pregnancy or disability disclosure. |
| [Common mistakes on a Record of Employment (First Reference / Simes Law, 2024)](https://www.firstreference.com/blog/common-mistakes-on-a-record-of-employment-roe/) | Code A used for terminations; 'for cause' comments; late ROEs. |
| [Record of Employment: A Reminder of the Need for Timeliness and Accuracy (McCarthy Tetrault, 2019)](https://www.mccarthy.ca/en/insights/blogs/canadian-employer-advisor/record-of-employment-a-reminder-of-the-need-for-timeliness-and-accuracy) | ROE fines up to $2,000; Morison v. Ergo-Industrial (late ROE, punitive damages). |
| [Don't Sign: Severance Deadline (UL Lawyers, 2025)](https://www.ullaw.ca/resource/fired-ontario-asked-sign-release-deadline) | Typical deadlines (48 hours, 'sign by Friday', 7 days) called pressure tactics. |
| [Court finds ESA-only termination clause unenforceable (Henderson v. Slavkin, 2022 ONSC 2964) (Hicks Morley)](https://hicksmorley.com/2022/08/24/court-finds-esa-only-termination-clause-unenforceable-due-to-wording-of-conflict-of-interest-and-confidential-information-clauses/) | Dental-office ESA-only clause failed; 18 months' notice owed. |
| [Court of Appeal for Ontario Restates the Common Law of Reasonable Notice Following a Sale of Business (Manthadi v. ASCO) (L&E Global / Filion Wakely)](https://leglobal.law/2020/08/27/canada-court-of-appeal-for-ontario-restates-the-common-law-of-reasonable-notice-following-a-sale-of-business/) | Predecessor service is weighed at common law, not automatically added on. |
| [Ontario Court of Appeal clarifies distinction: termination for cause and wilful misconduct under ESA (Render v. ThyssenKrupp, 2022 ONCA 310) (Siskinds)](https://www.siskinds.com/ontario-court-of-appeal-clarifies-distinction-termination-for-cause-and-wilful-misconduct-under-esa/) | Just cause doesn't remove ESA pay unless the conduct is wilful misconduct. |
| [3 Traps to Avoid When Writing a Termination Letter (HR Insider)](https://hrinsider.ca/3-traps-to-avoid-when-writing-a-termination-letter/) | Russell lessons; template use had 'a multiplying effect'; benefits extended but not disclosed. |
| [Severance Toolkit for Canadian HR Managers (HR Insider, 2025)](https://hrinsider.ca/severance-toolkit-for-canadian-hr-managers/) | HR package items: release, independent legal advice, EAP, outplacement, reference, ROE, no signature required on the day. |
| [Termination Letter (HR Insider)](https://hrinsider.ca/termination-letter/) | Without-cause letters should be 'brief and factual'. |
| [Tips On The Right Way To Fire Employees In Ontario (HR Insider / Vey Willetts, 2018)](https://hrinsider.ca/tips-on-the-right-way-to-fire-employees-in-ontario/) | The timeline and method for accepting a release-linked offer belong in the letter. |
| [HRPA Practice Guideline: Terminations Checklist](https://www.hrpa.ca/wp-content/uploads/2022/09/HRPA-Practice-Guideline-Terminations-Checklist-Accessible.pdf) | Detail everything owed to the end of statutory notice; ROE coding and access; conversion information; releases only for above-minimum offers; references; access to pay statements; belongings. |
| [Termination Checklist (National Payroll Institute)](https://payroll.ca/termination-checklist) | Benefits to the end of statutory notice; tell employees about conversion options and deadlines; ROE on time. |
| [Li-Cycle separation letter (Form 8-K Exhibit 10.1, 2024)](https://www.sec.gov/Archives/edgar/data/1828811/000119312524138800/d826129dex101.htm) | Opening read 2026-10-14 (streamed into memory). Header pattern (letterhead, written-out date, BY HAND, PERSONAL & CONFIDENTIAL, WITHOUT PREJUDICE), 'This letter confirms our recent discussions', expense deadline, ROE sentence, RRSP ending with statutory notice. Structure only; no names or figures used. |
| [WW Canada separation letter (Form 10-K Exhibit 10.26, 2024)](https://www.sec.gov/Archives/edgar/data/105319/000095017025029511/ww-ex10_26.htm) | Opening read 2026-10-14 (streamed into memory). Header pattern (written-out date, DELIVERED BY ELECTRONIC MAIL, CONFIDENTIAL WITHOUT PREJUDICE, Re: Notice of Termination of Employment); 'Further to our discussions'; ESA-compliance sentence; release deadline mechanics; legal-fee contribution; 'only what is required under the ESA' if conditions aren't met. Structure only. |
| [CA Canada termination letter and release (Form 10-Q Exhibit 10.3, 2014)](https://www.sec.gov/Archives/edgar/data/356028/000035602814000120/ca-ex103_2014630xq1.htm) | Executive letter features and length, via the research (calibration only). |
| [Termination pay in Ontario: What employers must pay (Xero Canada, 2026)](https://www.xero.com/ca/guides/termination-pay-ontario/) | Small-business guidance: put the end date, pay details, final-pay breakdown and benefit end dates in writing; ESA compliance doesn't bar a wrongful dismissal claim. |
| [Termination without cause: a guide for Ontario employers (BrightHR Canada)](https://www.brighthr.com/ca/articles/end-of-contract/termination-without-cause-on/) | Common-law notice applies without an enforceable limiting clause (no-contract driver context). |
| [Can Employers Pay out Notice Entitlements in Instalments Rather Than Lump Sum? (The Law of Work, 2011)](https://lawofwork.ca/can-an-employer-pay-severance-pay-by-continuation-of-salary-rather-than-a-lump-sum/) | ESA termination pay is a lump sum; ESA amounts aren't subject to mitigation. |
| [Driver Offboarding Checklist (Manifestly; US-oriented)](https://app.manifest.ly/public/checklists/35a856af4c941caa908c849a4cf7495b) | Driver property and systems items: fuel card, transponder, ELD tablet, gate fob, yard and hazmat keys, tractor and trailer, records of duty status. |
| [How to Handle Vehicle Offboarding (Automotive Fleet, 2026; US-oriented)](https://www.automotive-fleet.com/digital-cover-features/how-to-handle-vehicle-offboarding) | Fleet exit items: fuel cards, toll transponders, telematics, keys, registration and insurance cards. |
| [Cybersecurity Workshop #14: Termination Checklist (Canadian Dental Association, Oasis Discussions, 2023)](https://oasisdiscussions.ca/2023/04/17/cybersecurity-workshop-14-termination-checklist/) | Dental staff exits: remove system, email, file-sharing and remote access; involve the IT provider. |
| [Are Employment Law Cases Ruining Practice Sales? (Oral Health Group, 2021)](https://www.oralhealthgroup.com/features/are-employment-law-cases-ruining-practice-sales-heres-what-you-need-to-know/) | Practice-sale context: staff contracts scrutinised; sellers often share termination costs. |
| [Electronic logging devices for commercial motor vehicles (Government of Ontario)](https://www.ontario.ca/page/electronic-logging-devices-commercial-motor-vehicles) | Certified ELDs required since June 12, 2022 (trucking context). |
| [PS 803-C Sample Letter of Dismissal for Cause (Government of Saskatchewan, 2013)](https://taskroom.saskatchewan.ca/-/media/project/taskroom/documents/resource/803c--samples-letter-of-dismissal-for-cause-inscope-appendix-c.pdf) | Only source for an EAP paragraph and a cc line; 'Personal & Confidential' marking. Non-Ontario and for-cause, so weak support. |

## Full anatomy

The section-by-section structure the drafts followed, as written by the research
workflow.

SCOPE AND BASIS
A without-cause termination of one non-union, non-executive employee by a provincially regulated Ontario employer, dated in 2025. Built from these sources:
- the Key Media 'Termination Without Cause Letter Template' (file dated May 2025; read in full)
- the Ontario Chiropractic Association (OCA) clinic template, a version of the MaRS template (read in full)
- Citation Canada's sample (Jan 2024), HRXconnect's Ontario template (2025-26), Employment Hero's sample and Achkar Law's annotated sample
- the Russell v. The Brick letter (July 2020, as described in the decision)
- the WW Canada (Nov 2024) and Li-Cycle (Mar 2024) separation letters filed on EDGAR (openings read)

Wording patterns are paraphrased. Tags:
- [LAW]: a statute or regulation requires it, or the letter must not contradict it.
- [CUSTOM]: most templates and real letters have it.
- [SOMETIMES]: a minority of letters have it, or only some letter types.

SHAPE, LENGTH, TONE
- The five current fixture letters run 35 to 84 words. Even the thinnest published samples (Employment Hero's four-row table, Achkar's six-part sample, HRXconnect's 11-section template) give all of these:
  - the end date
  - the weeks and dollars of pay in lieu, with a payment date
  - a benefits end date
  - ROE timing
  - how to return property
- Length:
  - Key Media's template (minimums plus an optional offer paragraph) is about 710 words on 2 pages.
  - The OCA/MaRS clinic package is about 1,550 words: a cover letter of about 220, a 12-section 'Termination Agreement' of about 690, and a release of about 640.
  - Counsel-drafted executive letters run 5-8 pages plus a release.
  - No source gives a typical length for an ordinary employee. About 1-2 pages for a minimums-only letter, and 2-4 pages plus a release for a two-tier letter, are my inference.
- Tone:
  - Formal and neutral, in short declarative sentences.
  - 'We regret to inform you' is the stock opener (Key Media, Citation).
  - At most one neutral business reason. No apology or hedging. A one-line thank-you at the end.
  - HR Insider calls for 'brief and factual'. HRXconnect's 'less is more' means few topics and no explanation of reasons; its own template still gives every payment an amount and a date.
- Two tiers:
  - Tier 1 is what is paid or continued regardless: the statutory and contractual entitlements.
  - Tier 2 is an optional enhanced offer, conditional on a signed release.
  - A minimums-only letter is Tier 1, then administration, then the close. It has no release and no acceptance block (OCA says to remove the signature field), and usually no 'Without Prejudice' marking.
- Written from the employer's records. A real letter states the employer's own figures: start date or service, weekly rate, weeks, dollar amounts and dates. ESA s.12.1 requires that breakdown in writing by the final-pay date. The itemisation is therefore where cross-document mismatches naturally show up: rate, service, notice weeks, end date, and the reason versus the ROE code.
- Realism floor, even for a short owner-written letter:
  - a header with the date, delivery line, addressee and Re: line
  - 'without cause' and the effective date
  - pay in lieu as weeks x weekly rate = gross, with a payment date
  - vacation pay: the accrued balance, plus vacation pay on the termination pay
  - a severance line, only if eligible
  - a benefits end date, or a statement that there is no group plan
  - one ROE sentence
  - a property list with a return date and a contact
  - a named contact for questions
  - a signature with name and title

SECTION BY SECTION

1. Letterhead and header [CUSTOM; the delivery rules behind it are LAW]
- The employer's legal name as it appears on payroll and the ROE, with street address and phone.
- The date written out ('August 18, 2025'), as in both EDGAR letters. The fixtures currently use ISO dates.
- A delivery line: 'BY HAND', 'BY EMAIL', 'BY COURIER' or 'BY REGISTERED MAIL'. Li-Cycle uses 'By Hand'; WW uses 'Delivered by Electronic Mail'.
  - Behind it: notice must be in writing, addressed to the employee and served under ESA s.95. That means in person, by mail with verifiable delivery, by fax or email if the person can receive it, by courier, or in a sealed envelope left with someone 16 or older at the last known address. Text message is not on the list.
- A confidentiality marking: 'PERSONAL & CONFIDENTIAL' (Li-Cycle; the Saskatchewan sample) or 'STRICTLY CONFIDENTIAL' (OCA/MaRS).
  - Add 'WITHOUT PREJUDICE' only when the letter carries an offer (Russell, OCA/MaRS, WW, Li-Cycle).
  - Ramos v. Hewlett-Packard, 2017 ONSC 4413, held that the label isn't decisive (WeirFoulds).
  - Newer vendor templates that only confirm minimums omit both markings.
- Addressee block: courtesy title, full name and home address, or the email address if emailed.
- Re: line: 'Termination of Employment', 'Notice of Termination of Employment' (WW) or 'Termination of Employment (Without Cause)' (Key Media).
- Salutation: the first name, even in counsel-drafted letters (both EDGAR letters).

2. Opening: the decision, the date, without cause [LAW: in writing and specifying the date; CUSTOM: the rest]
- If the news was given in a meeting or a call, the letter confirms it. WW: 'Further to our discussions'. Li-Cycle: 'This letter confirms our recent discussions'. OCA refers to the meeting held on a stated date.
- Core sentence: 'your employment with [Employer] is terminated without cause, effective [date]', often with the date as a defined term ('the Termination Date').
  - Ministry policy is that the notice 'must specify when the employment is to be terminated'.
  - HRXconnect calls the date the most important element, because pay, benefits and notice all run from it.
- Say whether it is working notice (the last day of active work, with terms unchanged until then under ESA s.60) or an immediate termination with pay in lieu. WW adds a sentence that the company will comply with all ESA requirements.
- Reason: none, or one neutral business reason, such as restructuring, a position eliminated, lost contracts, or a role duplicated after a merger.
  - It is often followed by 'this is not a reflection of your performance or conduct' (Key Media).
  - Never cite warnings, lateness, logbook issues or performance. Achkar calls these 'inadvertent admissions'.
  - If the employee recently disclosed a pregnancy or disability, say the decision is unrelated (Rudner).
- Optional: name the contract clause relied on, e.g. 'in accordance with section 6 of your Employment Agreement dated [date] and the ESA' (Key Media; WW). Achkar says to check the clause is enforceable first.

3. Entitlements paid regardless [LAW content; CUSTOM layout]
Set these out as bullets or numbered paragraphs, or as a 'Summary of final pay' table. Each item gives the weeks or basis, the gross dollars, 'less applicable statutory deductions' and a payment date. Usual order:
a) Outstanding wages: regular pay to the Termination Date, plus any earned overtime, commission or other wages, on the next regular pay date.
b) ESA termination pay in lieu of notice: X weeks (ESA s.57 table) x $Y regular weekly wages = $Z.
   - Paid as one lump sum by [date], no later than the s.11(5) deadline.
   - For variable or non-time pay (mileage, piece rate, irregular hours), say the weekly figure is the average regular wages for the weeks worked in the 12 weeks before termination (s.61(1.1)).
   - Regular wages exclude overtime, public holiday pay, premium pay and vacation pay (s.1).
c) ESA severance pay, only if eligible (5+ years, plus either a $2.5M payroll or a closure severing 50+ employees).
   - Amount: weekly regular wages x (completed years + completed months/12), up to 26 weeks.
   - It gets its own line and is paid as a lump sum, unless the employee agrees in writing to instalments (s.66).
   - If the employee isn't eligible, omit it or say it doesn't apply (OCA: delete the clause if not needed).
d) Vacation pay: all accrued, unused vacation pay, including any carried over, plus 4% (under 5 years) or 6% (5+ years) on the termination pay.
   - None is owed on severance.
   - In Russell, paying vacation pay only to the termination date fell short of the ESA.
e) Benefits: name each plan (extended health, dental, life, AD&D, STD/LTD, and EAP if the plan has it) with the date coverage ends.
   - With pay in lieu, coverage ends on the Termination Date plus the ESA notice weeks.
   - Say which benefits can't be continued and what the employer does instead.
   - Give the life-insurance conversion window: commonly 31 days (Employment Hero; Russell), or 30 days for life and 90 for health and dental (Li-Cycle).
   - The National Payroll Institute (NPI) checklist says to tell employees their conversion options and deadlines.
   - If there is no group plan, say so or leave the section out (OCA note).
f) Pension, RRSP/DPSP match, bonus, commission, incentives, options, loans or advances: how each is treated up to the end of the statutory notice period (HRPA; Blaney; WW; Li-Cycle).
   - A discretionary bonus not tied to hours, production or efficiency isn't ESA 'wages' (s.1). The letter states the plan outcome instead: prorated, paid if approved, or not payable.
g) The sentence that separates the tiers: these amounts will be paid whether or not you accept the offer below or sign a release.
   - Sources: Key Media; Citation; the OCA/MaRS release; WW, which says that if its conditions aren't met the employer provides only what the ESA requires.
   - Russell called its absence a 'serious defect'. In Wilds, making ESA pay depend on a release breached the ESA.
h) Payment mechanics:
   - direct deposit to the account on file, 'less applicable statutory deductions'
   - a final pay statement (in the letter or enclosed) showing each gross amount, how it was calculated, each deduction and the net (ESA s.12.1)
   - optional: on the employee's request, severance can go straight into their RRSP within their contribution room (CRA). The employee in Russell asked for this.

4. Enhanced offer in exchange for a release [SOMETIMES: only when the employer wants a release]
- Lead-in pattern: 'In addition to the above, and conditional on your signing and returning the enclosed Full and Final Release by [date], [Employer] will provide...' (Key Media; Citation opens 'Notwithstanding the foregoing'; OCA s.6).
- Typical items:
  - extra weeks of base salary, as a lump sum or as salary continuance on regular payroll (the above-ESA part only), sometimes ending on new employment
  - extended benefits
  - outplacement, with a named provider and duration
  - a legal-fee contribution (WW: up to $5,000 plus HST)
  - a confirmation-of-employment letter
  - prorated bonus or commission
- Deadline:
  - Citation suggests about a week.
  - WW required countersignature within 7 days and the signed release no later than 7 days after the separation date.
  - Amar-VR recommends at least 5 business days to get legal advice.
  - Russell's 3 days was criticised.
  - Never require signature at the meeting (HRXconnect).
- Legal advice: 'We encourage you to obtain independent legal advice before signing' (Key Media; Citation).
- Confidentiality: the offer's terms are confidential. They can be disclosed to immediate family and to legal or financial advisers, and a breach ends the offer (OCA/MaRS; WW; Li-Cycle).
- If the offer is declined, Tier 1 is still paid, and nothing more (Key Media; Citation).
- The release is a separate schedule (OCA Appendix B). It contains:
  - a release of all claims and a covenant not to sue
  - a Human Rights Code warranty
  - no admission of liability
  - confidentiality
  - an acknowledgement that statutory money doesn't depend on signing
  - an acknowledgement of independent legal advice (ILA)
  - a witnessed signature
- Salary continuance pushes the ROE back to the end of the continuance (ROE guide).

5. Administration [CUSTOM]
- ROE. Pattern: 'Your Record of Employment will be submitted electronically to Service Canada. You can view it in My Service Canada Account. If you plan to apply for EI, apply as soon as possible.'
  - The ROE guide asks employers to tell employees these three things. Li-Cycle says the ROE is sent directly to Service Canada and can then be viewed online.
  - Mayo Law treats the ROE as a filing duty rather than letter content, but most templates include a sentence on it.
  - Legal deadline for an electronic ROE: 5 calendar days after the end of the pay period containing the interruption of earnings. For monthly or 13-period payroll, it is the earlier of that and 15 days after the interruption. Paper ROEs are due within 5 calendar days. Templates shorten all of this to 'within five days'.
  - If the letter names the reason code, the code must match the letter: A for a position eliminated, restructuring or shortage of work; M for other employer-initiated separations. HRPA suggests explaining the coding.
  - Don't copy 'the ROE will note that you were terminated without cause' (Key Media); there is no such code. Don't copy 'present this form to HRSDC' (OCA/MaRS).
- Expenses: submit claims with receipts by [date] (OCA s.7; Li-Cycle).
- Company property (Achkar; Key Media; Citation; OCA s.11; Blaney):
  - an itemised list: laptop, phone, keys, fobs, access cards, credit or fuel cards, vehicle, documents and confidential information
  - a deadline, a contact and a return method
  - no copies kept
  - Property comes back whether or not the offer is accepted (Li-Cycle).
  - No wage deduction for unreturned items without a specific prior written authorization (ESA s.13). An above-ESA payment can be made conditional on return.
- Personal belongings: pick-up or courier arrangements (Citation; HRPA).
- Access and records: email and systems access ends on the Termination Date. Say how the employee will get pay statements and the T4 (HRPA; OCA s.9 asks to be told of address changes so the T4 arrives).
- References: a confirmation of employment on request, 'according to our usual practices' (OCA s.10). Never promise a positive reference (HRXconnect).
- EAP: thinly sourced for Ontario; only HR Insider's toolkit checklist and a Saskatchewan public-service sample mention it. Include it only if the employer has a plan, and say how long access lasts.

6. Continuing obligations [CUSTOM]
- Confidentiality, intellectual property and non-solicitation obligations in signed agreements continue (Key Media; Citation; OCA; HRXconnect). A copy is often enclosed.
- No non-compete reminder for a non-executive. Those are void under ESA s.67.2 for agreements made on or after October 25, 2021.

7. Close [CUSTOM]
- A named contact (name, title, phone, email) for questions on the pay and benefits calculations (Key Media; Citation; HRXconnect; OCA).
- Thanks for the employee's service, and good wishes (Key Media; Citation).
- 'Yours truly', 'Sincerely' or 'Regards', then signature, name, title and company. The signer is the owner, the Director of People or HR Manager, the Practice Manager, or an operations lead.
- 'Encl.' list (Citation; Key Media; OCA):
  - the release
  - benefits conversion information or the insurer's booklet
  - the final pay statement
  - a copy of the confidentiality agreement
  - outplacement details
- 'cc: personnel file' appears only in the Saskatchewan sample.
- An employee acceptance block only when there is an offer ('I accept the terms in Appendix A in full and final satisfaction...', OCA). Never put one on a minimums-only letter: a signed acknowledgement can bind the employer to whatever figures the letter states (Stowar v. Telehop).

DATE CUES FOR A 2025 LETTER
- Signs of a post-2021 letter:
  - an explicit 'ESA paid regardless' sentence (Russell 2021; Wilds 2024)
  - vacation pay on the notice period
  - per-benefit end dates and carve-outs
  - no non-compete for ordinary staff
  - an electronic ROE and My Service Canada Account
- Dated signs, to use only as a deliberate seed:
  - 'HRSDC'
  - 'present this form' for the ROE
  - a package 'inclusive of' all ESA amounts with no breakdown (OCA/MaRS wording; compare Halloran)
- Not part of a 2025 single-employee letter:
  - the mass-termination Form 1 and the Employment Ontario information sheet (from July 1, 2025)
  - job-seeking leave (from November 27, 2025)
- The 2025 ESA amendments (2025, c. 13) changed the lay-off rules, not the notice, pay, benefits, severance, vacation or final-pay sections used here.

