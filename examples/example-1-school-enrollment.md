# Example: School Enrollment Process Analysis

🌐 **Language / Sprache:** [English](example-1-school-enrollment.md) | [Deutsch](example-1-schulanmeldungen.de.md)

## Starting Situation

The City of Zurich School Department receives approximately 3,500 school enrollments for 1st grade annually. The current process comprises 12 steps and takes an average of 6 weeks from receipt to confirmation.

**Current Process (simplified):**

1. Parents download PDF form from website
2. Parents fill out form by hand
3. Parents send form by mail or scan and send by email
4. Office receives and sorts enrollments
5. Office manually enters data into Excel
6. Office forwards Excel to school district coordination
7. School district coordination checks residential jurisdiction
8. School district coordination creates class assignment proposal
9. School principal approves class assignment
10. School district coordination enters final assignment into SchoolDB
11. Office creates confirmation letter (Word template)
12. Office prints and sends letter by mail

**Problem:** High manual effort, many media breaks, long wait times.

---

## Analysis Using the 5-Step Algorithm

### Step 1: Question the Requirements

| # | Requirement | Author | Problem Solved | Legal Basis? | Rating | Data Quality |
|---|---|---|---|---|---|---|
| 1.1 | PDF form | IT department (2012) | "Uniform layout" | No | 🔴 | 🔵 Verified: IT documentation available |
| 1.2 | Handwritten completion | Unknown ("always been this way") | No clear one | No | 🔴 | ⚪ Estimate: No author identified |
| 1.3 | Mail/email receipt | Data protection policy (2015) | Avoiding cloud tools | Yes (Zurich DPA) | 🟢 | 🔵 Verified: Legal opinion available |
| 1.4 | Manual Excel entry | Office staff | "For further processing" | No | 🔴 | 🔵 Verified: Process documented |
| 1.5 | Residential check | District coordination | Correct school assignment | Yes (Education Act §5) | 🟢 | 🔵 Verified: Legal text |
| 1.6 | Class assignment proposal | District coordination | Pedagogical balance | No | 🟡 | ⚪ Estimate: Benefit unclear |
| 1.7 | Principal approval | Org. regulations (2018) | "Four-eyes principle" | No | 🟡 | 🔵 Verified: Regulations available |
| 1.8 | Entry into SchoolDB | IT department | Data management for school year | Yes (Admin Regulation §12) | 🟢 | 🔵 Verified: Regulation |
| 1.9 | Word template for letter | Communications (2010) | "Corporate design" | No | 🟡 | 🔵 Verified: CD guidelines |
| 1.10 | Printing and mailing | Communications | "Official character" | No | 🔴 | ⚪ Estimate: No documentation |

**Findings:**
- 🟢 **3 valid requirements** (legally anchored)
- 🟡 **3 questionable requirements** (internal origin, benefit unclear)
- 🔴 **4 deletion candidates** (no clear author or obsolete)

---

### Step 2: Delete

#### Stakeholder Analysis

| Deletion Candidate | Affected Stakeholders | Type of Impact | Involvement Required? | Communication Measure |
|---|---|---|---|---|
| 1.1 PDF form | Parents, IT | Parents must use new system | Yes | Information via newsletter, website update |
| 1.2 Handwritten | Parents | None — digital input is easier | No | - |
| 1.4 Excel entry | Office staff | Workload is reduced | Yes | Training for new solution |
| 1.6 Class assignment proposal | District coordination | Decision authority shifts | Yes | Workshop with coordination |
| 1.10 Mailing | Parents, office | Parents receive email instead of letter | Yes | Offer opt-in for postal delivery |

**Deletions with Justification:**

- ✂️ **PDF form** → Replaced by online form (directly into SchoolDB)
- ✂️ **Handwritten completion** → Digital is more efficient and less error-prone
- ✂️ **Manual Excel entry** → Direct database entry
- ✂️ **Postal delivery** → Email delivery (opt-in for mail remains as exception)

**Retained (with justification):**

- ✅ **Residential check** — Legally required
- ✅ **SchoolDB entry** — Legally required
- ⚠️ **Principal approval** — Retained, but process simplified (see Step 3)

**Reversibility Plan:**
- PDF form: Reactivation possible within 1 week (archived on server)
- Excel entry: Can be reactivated at any time as backup (template available)

---

### Step 3: Simplify

#### Before-and-After Comparison

| Before (12 Steps) | After (5 Steps) |
|---|---|
| 1. Download PDF<br>2. Fill out by hand<br>3. Scan/mail<br>4. Office sorts<br>5. Excel entry<br>6. Forward to coordination<br>7. Residential check<br>8. Class assignment<br>9. Principal approval<br>10. SchoolDB entry<br>11. Create letter<br>12. Print/mail | 1. **Fill out online form** (with address autocomplete)<br>2. **Automatic residential check** (Geo API)<br>3. **Automatic class assignment** (algorithm with principal review)<br>4. **Automatic email confirmation**<br>5. **(Optional) Principal reviews exceptions** |

**Simplification Measures:**

1. **Media break eliminated**: Paper → Online form directly into database
2. **Roles consolidated**: Office + district coordination → System (with exception handling)
3. **Approval cascade shortened**: Principal now only approves exceptions (e.g., out-of-district children), not all assignments
4. **Data entry redundancy eliminated**: 1x entry by parents, no manual re-entry

---

### Step 4: Accelerate

**Wait Time Analysis (Before):**

| Step | Wait Time | Reason |
|---|---|---|
| Mail receipt | 1–3 days | Postal transit time |
| Office data entry | 2–5 days | Batch processing (weekly) |
| District check | 1–2 weeks | Waiting for coordination meeting |
| Principal approval | 1 week | Waiting for principal meeting |
| Letter mailing | 1–3 days | Postal transit time |

**Total cycle time:** 3–6 weeks

**Acceleration Measures:**

1. **Parallelization**: Residential check + class assignment happen automatically when form is submitted
2. **Real-time feedback**: Parents receive immediate confirmation instead of waiting 6 weeks
3. **Batch elimination**: No more weekly processing, continuous instead
4. **Meeting reduction**: Principal only reviews exceptions (asynchronously, as needed)

**New cycle time:** < 24 hours (for standard cases)

---

### Step 5: Automate

**Automation Plan:**

| Step | Tool/Technology | Priority | Effort | Justification |
|---|---|---|---|---|
| Online form | Webflow / TypeForm | 🟢 Quick Win | 2–3 days | Easy to implement |
| Address autocomplete | Google Places API | 🟡 Strategic | 1 week | Reduces typos |
| Residential check (Geo) | OpenStreetMap API | 🟢 Quick Win | 3–5 days | Eliminates manual checking |
| Class assignment algorithm | Python script (class capacity + geo) | 🟡 Strategic | 2–3 weeks | Complex but high value |
| Email confirmation | SendGrid / Postmark | 🟢 Quick Win | 1 day | Standard integration |
| SchoolDB integration | API integration | 🟡 Strategic | 2–4 weeks | Depends on DB architecture |

**Warning:** Only automate the class assignment algorithm after the manual process has run stably for 1 school year (Step 5 rule).

---

### Summary

**Expected Impact:**

- **Time savings (office staff):** ~80% (from 40h/year to 8h/year for exceptions)
- **Time savings (parents):** 6 weeks waiting → 24 hours
- **Error reduction:** ~90% (no manual data entry)
- **Cost reduction:** ~CHF 12,000/year (printing, postage, labor)

**Risks:**

- Technical risk: Online form outage → Solution: PDF backup remains available
- Acceptance risk: Parents without internet access → Solution: Opt-in for paper enrollment

---

### Quick-Win Matrix

```
                       High Impact
       ┌────────────────────┬────────────────────┐
       │  STRATEGIC         │   QUICK WINS       │
       │                    │                    │
       │  • Class assignment│  • Online form     │
       │    algorithm       │  • Email delivery  │
       │  • SchoolDB        │  • Geo check       │
       │    integration     │                    │
High ──┼────────────────────┼────────────────────┼── Low
Effort │  AVOID             │   NICE-TO-HAVE     │  Effort
       │                    │                    │
       │  • Comprehensive   │  • Address         │
       │    process         │    autocomplete    │
       │    redesign        │                    │
       │                    │                    │
       └────────────────────┴────────────────────┘
                       Low Impact
```

**Recommended Implementation Order:**

1. **Immediately (1–2 weeks):** Online form + email confirmation + geo check
2. **Medium-term (3–6 months):** SchoolDB integration + address autocomplete
3. **Long-term (1–2 years):** Class assignment algorithm (only after manual process proves stable)

---

**Next Steps:**

1. Executive decision: Approve quick wins (budget: ~CHF 5,000 for Webflow + APIs)
2. Stakeholder communication: Newsletter to parents (February 2026)
3. Pilot: 1 school district tests new process (March 2026)
4. Rollout: All school districts (school year 2026/27)
