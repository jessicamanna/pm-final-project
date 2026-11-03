# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** Top producer Dana R. (P1) stopped submitting tickets in 2024 ("Eight days for a flyer isn't a process, it's a punishment") and now pays an assistant out of pocket to make flyers in Canva, outside compliance review and possibly without an NMLS ID. (Simulated)
- **Moment of misery / red flag #2:** Rosa M. (P5) asked on Tuesday for a buydown flyer for Ridgeview Homes' Saturday grand opening and got it the following Monday. The builder printed its own without her, and its sales office now hands out another lender's card. (Simulated)
- **Moment of misery / red flag #3:** New LO Priya S. (P3) promised an agent a one-pager and never sent it, because she didn't know what she could say about rates and her only ticket had taken nine days. (Simulated)
- **Product Health & Insights Summary (Claude's output):** Product Health & Insights Summary: Retail LO Collateral Process

Source: Harborline Home Lending discovery dataset, Sept 8 – Oct 2, 2026 (simulated course data). Inputs: request-queue export (n=914), shadow-asset audit (n=240), CRM referral baseline, LO survey (n=94), 9 interviews, Slack channel excerpts.

Executive Summary

The collateral process works for planned requests but fails when a partner sets the deadline. Median turnaround is 6.5 business days against 4.1 hours of logged work, and only 19% of urgent requests arrive on time while 46% of LOs say partners need material the same day. Because the official path is too slow, much of the collateral now reaching realtor and builder partners never goes through it: 41% of LOs submitted no requests in six months, and 37% of sampled LO-made assets carried at least one regulatory violation. The compliance controls therefore cover mainly the lowest-risk work, and no data yet connects a delivered asset to a partner referral.

Thematic Synthesis
1. Speed & Latency

Time in the process comes from waiting, not from work. Total cycle time is about 12 times the hands-on effort, and the gap is widest for unplanned, partner-driven requests. LOs who plan a week ahead, mostly top producers, describe the process as workable. The failures cluster around the moments LOs can’t schedule: open houses, agent lunches, and a builder’s weekend event.

Critical: Urgent requests (needed within 2 business days, n=163) are delivered on time only 19% of the time, and 33% are cancelled. These are the requests closest to a live partner opportunity.
High: Partner timing and the process clock don’t match. 79% of LOs say partners expect material within 2 days, while the median delivery is 6.5 business days (p90: 14).
High: 24% of requests are delivered after the LO’s “needed by” date, and 14% are abandoned. The true late rate is probably higher, because 31% of tickets left the “needed by” date blank and were counted as on time.
2. Compliance Risk & Trust

The largest compliance exposure sits outside the review process. LO-made assets are concentrated among LOs who never submit requests, and the violations are basic ones: missing identifiers and disclosures. Inside the process, review is slow mainly because the same errors keep coming back, not because the issues are hard. The compliance reviewer would accept automated help, but only under conditions, and the final decision belongs to the GC.

Critical: 37% of the 240 sampled shadow assets had at least one regulatory violation: missing NMLS ID (19%), missing EHO (14%), rate without APR (11%), trigger term without disclosure (8%), possible RESPA issue (4%). Assets with violations were 2.4× more likely to come from zero-request LOs, and the analyst describes the sample as “the tip.”
High: Rework in review is repetitive. 38% of tickets were returned at least once, and 71% of returns cite the same six issues.
High: LOs don’t know what is permitted. Examples include a “lowest rates in town” post deleted after a warning, a new LO who sent nothing because she was afraid of rate language, and the comment “nobody told me what IS allowed.”
High: Trust in any faster review path is conditional and held by the veto owner. Compliance would trust an automated first pass immediately and might accept no human final review for NMLS and logo checks. For rates and RESPA, the reviewer wants 10% sampling for six months plus an examiner-ready audit log, and the GC decides.
Medium: LOs try to reuse outdated assets whose disclosures reference old pricing (Slack, Aug 19).
3. Briefing & Process Friction

Briefing is the least predictable stage and the one LOs control least. Vague requests produce back-and-forth messages, and co-branded pieces add a second set of approvals the team can’t speed up. For LOs who reach out informally, the first contact with the process is often a redirect, and many stop there.

High: Briefing takes a median of 1.8 business days (p90: 4.5), with an average of 2.3 clarification messages per ticket. Designers report spending “half my week” chasing briefs.
High: Co-branded pieces (9% of requests) need builder or realtor brand approval on top of compliance review, which creates delays the team can’t control. The one documented case of partner loss involved a co-branded piece.
Medium: Redirects to the request form at the moment of need lead LOs to abandon the request (“never mind lol” after a 6–8 day turnaround quote).
4. Personalization & Credibility

To the recipient, the flyer stands in for the LO’s responsiveness and judgment. The realtor interview suggests partners value same-day response, relevance to their own listing, and material that won’t embarrass them more than they value the asset itself. Generic output reads as low effort, and errors damage the partner relationship directly.

High: Partners judge LOs on speed, relevance, and polish. A typo or a “weird rate” ends the relationship (“it makes me look bad”), and generic pieces get thrown away.
High: Output looks the same across LOs. Nine of 140 templates account for 80% of template-based requests, and LOs and partners notice (“Agents notice”; “my builders will clock it”).
High: New LOs have the least credibility material and the smallest networks (4.1 active partners vs. 26.0 for top producers), and they describe having “nothing to show them that says I’m legit.”
High: A late co-branded piece is linked to a lost builder relationship (Ridgeview’s sales office now hands out another lender’s card). This is a single anecdote, not a measured pattern.
5. Adoption & Avoidance

The request queue understates real demand, because the people with the most urgent needs have stopped using it. Top producers with resources go around the process at their own expense. New LOs barely use it, and fear seems to drive that more than dissatisfaction does. Mid producers turn to generic AI tools.

Critical: 41% of LOs (61 of 150) submitted no requests in six months. Seven top producers bypass the process entirely with personally paid assistants or freelancers.
Critical: At their last urgent need, 41% of surveyed LOs made the material themselves (17% with AI) and 22% sent nothing. Only 28% used the official process.
High: New LOs submit few requests (9% of volume, 3.0 per LO) despite the highest satisfaction score (3.3/5). This points to fear and lack of knowledge, not dissatisfaction.
Medium: Overall satisfaction is low (2.4/5) and lowest among top producers (2.1/5). Comments attribute the problem to the process, not the people (“the marketing team is great people”).
Medium: Production staff fear being replaced (“if the plan is to cut me, say it”). This is a change-management risk, not a user need.
6. Buyer Value & Measurement

The buyer won’t fund this on efficiency grounds. In his framing, time savings become a headcount-cut conversation he wants to avoid, and the savings are too small to matter to the CFO. Referral growth is the framing that reaches a funded budget, but no current data can prove it.

Critical: No asset-to-partner link exists in the CRM, so nobody can tell whether a partner who received a piece later sent a deal. The value story the buyer would fund can’t be measured today.
High: Budget would have to come from elsewhere (“I’d have to kill something to fund something”). The buyer pays about $18K/year for Canva seats the LO side barely uses.
High: The channel at stake is concentrated. Realtor and builder referrals account for 74% of retail purchase applications.
Minor Process Debt

Requests for color and brand flexibility (“the bank look,” the most-reacted Slack post this quarter, with no evidence linking it to an outcome); low awareness of the template library (a designer’s reminder drew 2 reactions); request-form onboarding for new hires (“didn’t know we had a request form until month 3”); low LO demand for compliance training (12%), which conflicts with the evidence that LOs don’t know what is allowed.

Signal Strength Notes
Strongest (behavioral): queue timing and outcomes, the shadow-asset audit, zero-request counts, and the CRM baseline.
Weak (attitudinal or hypothetical): 91% “would use” a fast compliant tool (a future hypothetical), the buyer’s “absolutely, if it works” (an off-script hypothetical), and the branch manager’s “three times the business” (overheard, unsupported).
Coverage gaps: top producers are underrepresented in the survey (17 of 30), DIY volume is unknown, willingness to pay rests on one interview, and no data shows that faster delivery changes partner behavior.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Yes, all three appear. Rosa's lost builder is caught and correctly labeled a single anecdote, though it shows up in two themes (3 and 4) despite the "combine recurring issues" constraint. Priya appears in Themes 2, 4, and 5 in her own words. Dana appears only as a statistic (see next answer).
- **Did it smooth over a critical frustration into a generic bullet point?:** Partly, in Dana's case. Her story is folded into "Seven top producers bypass the process entirely," which drops what matters most: she pays for the workaround herself (the cost is "my weekends"), and her flyer to a listing agent may have gone out without an NMLS ID. That is the clearest evidence that top producers, the launch segment, carry both personal cost and compliance risk.
- **Did the AI try to suggest features or a roadmap despite the constraints?:** No features or roadmap. One sentence is borderline: Theme 6's "Referral growth is the framing that reaches a funded budget" is positioning advice that rests on a single buyer interview.
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** Invented detail. Theme 5 says "Seven top producers bypass the process entirely with personally paid assistants or freelancers" ("at their own expense"). The data says only that all seven "have a personal assistant or a paid freelancer (per branch managers)"; only Dana (P1) says she pays out of pocket. The AI turned one person's situation, reported secondhand for the rest, into a fact about all seven.
- **Logic leak / hallucination #2:** One interview presented as a pattern. Several High-rated claims rest on a single person: new LOs' low usage "points to fear" (P3 only), "the buyer won't fund this on efficiency grounds" (P9 only), "partners judge LOs on speed, relevance, and polish" (P8 only), and "designers report spending 'half my week'" (P7 only). With no sample size shown, a single quote reads as strongly as the 914-ticket queue export.
