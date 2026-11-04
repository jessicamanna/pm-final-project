# N1 · Smart chat brief → compliant flyer, Simplified PRD (Nomi)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Top-producing retail LO (top 20%, 26 partners, 58% of referred applications) answering a partner's "send me something" within a day

## 1. The Big Picture
- **Vision:** To eliminate the week-long wait between a partner's "send me something" and a compliant flyer by turning one chat into a reviewed, on-brand flyer in about 3 minutes.
- **Press release:** Today, Nomi launched Smart Brief for retail loan officers at mortgage lenders. When a realtor or builder says "send me something," the loan officer types the request into a chat, answers a few smart questions about the partner, the program and the goal, and gets a product flyer in her lender's brand that has already been checked against the lender's compliance rules. A reviewed draft is ready in about 3 minutes and the finished piece in under 15.

Right now, only 14% of top producers' urgent requests arrive on time, so 59% make their own flyers outside compliance review. With Nomi, a non-compliant flyer is never created: if a loan officer asks for something the rules don't allow, like a rate without an APR, Nomi explains why and drafts the compliant version, and the lender's compliance team gets an audit trail of every asset and every adjusted request.
- **Success metric:** Urgent partner requests answered with a compliance-reviewed asset within 1 business day: 14% → 60%
- **Guardrail:** Post-delivery compliance issue rate must not rise (10% sampling audit)

## 2. The Details
### User stories
- As a top-producing LO, I want to describe a partner's request in one chat so that I don't lose a day to back-and-forth with a designer. Acceptance: partner, program and needed-by date captured; missing objective, audience or CTA asked in the same chat; brief done in under 2 minutes.
- As a top-producing LO, I want a polished flyer in my lender's brand with my details on it so that I look like the professional worth sending business to. Acceptance: draft built from the lender template with LO name, NMLS ID and contact details; 3 headlines to swap.
- As the lender's compliance team, I want every request checked before a draft exists and every adjusted request logged so that nothing non-compliant reaches a partner with the lender's name on it. Acceptance: 6 checks green on every draft; a rate-without-APR request is explained and drafted with the APR; audit-trail entry with timestamp, LO, partner tag and the request before/after.
### Screens to build
- 1. Entry · Chat brief: chat thread, message input, suggested prompts, progress indicator (Brief → Draft → Check → Ready)
- 2. Core · Draft + compliance: flyer preview, headline swap (3 options), 6-check compliance panel, audit-trail entry with before/after of any adjusted request
- 3. Confirmation · Ready: reviewed badge, partner tag, elapsed time vs. "usually about a week," simulated download and share link, start over
### Functional requirements
- The flyer cannot generate until partner, loan program and needed-by date are captured.
- If objective, audience or CTA is missing, the chat asks in the same conversation, with at most 3 follow-up questions.
- Every request passes the compliance pre-check before a draft is generated; a draft with a violation is never rendered.
- A non-compliant request (rate without APR, trigger term without disclosure) gets a plain-language explanation, and the compliant version is drafted instead.
- Every flyer shows the LO's name and NMLS ID, the lender's NMLS ID, the Equal Housing Opportunity logo and required disclosures.
- The compliance panel shows 6 named checks, all green, plus an audit-trail entry (timestamp, LO, partner tag, adjusted request before/after).
- The ready screen shows elapsed time from first message to reviewed flyer, against "usually about a week."
- Swapping the headline re-runs the checks instantly; the panel stays green.
### Smart behaviors (Situation → Outcome)
- If the LO names a partner → apply the partner tag to the brief and every output
- If the needed-by date is missing → ask "When does the partner need it?" before drafting
- If the LO asks for a rate without an APR → explain the APR rule and draft with rate, APR and disclosure
- If the LO uses a trigger term (e.g. "low down payment") → add the required disclosure automatically and log it
- If the LO states a style preference → ask "Save this for all your materials, or just this partner?"
- If the LO swaps the headline → re-run the checks and keep the panel green
### Technical constraints
- Single index.html; no external APIs, images, fonts or libraries; system font stack and inline SVG only
- In-memory JS state only; no database, no login
- Mock data only, clearly fictional (Harbor Lane Home Loans, LO Maya Reyes, 555 phone numbers, .example emails)
- Everything simulated: generation, compliance, download, share link
- Mobile-first at 390px, centered column on desktop; one accent color, green/red only for pass/fail
- Footer on every screen: "Prototype. Compliance checks are illustrative, not legal advice."

## 3. The Logistics
### Features out
- Real AI generation and real compliance logic
- Live rates / pricing engine
- Full partner co-branding (N5, Next); in the pilot, the partner tag applies basic co-branding and partner preferences
- Other asset types (social video, email, print ads)
- JIRA escalation to the lender's legal team
- Human sampling queue UI
- Usage dashboard UI and partner referral dashboard (usage stats are still tracked in the pilot via N13)
- Login, CRM sync, real file export
### Edge cases & safety guard
- Empty message → prompt with an example request
- Unknown loan program → offer the lender's program list
- Needed-by date in the past → ask the LO to confirm
- LO insists on non-compliant language → explain again, keep the compliant version, offer escalation to the lender's compliance team (simulated)
- Safety: never invent rates, APRs, program terms, NMLS IDs or partner details; never render a draft that fails a check; never remove a required disclosure
### Decision log
- Compliance runs before drafting, not after ("never created"), so a non-compliant draft never exists, even in the LO's preview.
- Flyer only, chat intake only (no form): other asset types and co-branding wait until the flyer proves top producers will bring urgent requests into a compliant path.
### Evals
- Accuracy: 100% of generated flyers pass all 6 checks across a 20-request test set that includes 5 deliberately non-compliant requests
- Time-on-task: median time from first message to reviewed draft ≤ 3 minutes in test sessions
- Safety: 100% of non-compliant requests are explained, adjusted and logged with an audit-trail entry

## MoSCoW scope
- **Must:** Chat brief captures the partner (partner tag), loan program and needed-by date in one conversation; Asks about objective, audience and call to action when they're missing; Drafts a product flyer from the lender-branded template with the LO's name, NMLS ID and contact details; 3 headline options the LO can swap between; Compliance pre-check before drafting: a non-compliant request (e.g. rate without APR) is explained and drafted in its compliant form, so a non-compliant draft never exists; 6-check compliance panel, all green, plus an audit-trail entry showing the adjusted request as a before/after; Ready screen with reviewed badge, partner tag, and elapsed time vs. "usually about a week"
- **Should:** "Save this for all your materials, or just this partner?" preference prompt; Simulated download and share link
- **Could:** LO personal brand (sub-brand, team name, vanity domain); LO satisfaction rating and comment; Edit the brief / start over
- **Won't (now):** Real AI generation or a real compliance engine; Live rates; Full partner co-branding (N5); Other asset types (social video, email, print ads); JIRA escalation; Human sampling queue UI; Usage dashboard UI; Login, CRM sync, real file export

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.
