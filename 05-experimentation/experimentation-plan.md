# Experimentation Plan

> **Module 5 · ★ Deliverable 5.** Repo file `05-experimentation/experimentation-plan.md` — part of your submission.
> Do the lab in the **Module 5 · Exercise Guide** (linked from the Module 5 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Experimentation Plan** slide of your Module 6 final deck.

## Overview

_A high-level validation strategy to test your hypothesis before full-scale development._

We will validate the hypothesis with a 90-day A/B test at one lender, splitting the lender's 30 top-producing loan officers 50/50 between Nomi and today's process for urgent partner requests for product flyers. Before launch we lock the primary metric, the guardrail and its boundary, the smallest lift worth shipping, and a fixed read date, so the go/no-go call follows a rule written now, not how the results look later. Nomi is the only difference between the groups: the lender's request queue, the weekly LO check-in, brand templates, the partner CRM, and LO compensation stay the same for both.

## What you're testing

| Element | Detail |
|---|---|
| Hypothesis under test | I believe that giving top-producing loan officers Nomi (chat brief → draft → compliance check → ready-to-send product flyer) for urgent partner requests will move those requests back into a compliant path, as measured by an increase from 14% to 60% in urgent partner requests answered with a reviewed asset within 1 business day within 90 days. We will protect the post-delivery compliance issue rate throughout the test. |
| Experiment design (A/B, etc.) | 50/50 A/B test behind a feature flag: the lender's 30 top producers are randomly split into 15 who get Nomi (variant) and 15 who keep today's process (control) for 90 days. We randomize by LO, not by request, so each LO's experience stays consistent. We considered two other designs. A pre/post pilot with all 30 LOs has no control group, so a change in the lender's queue staffing or the market during the pilot could not be separated from Nomi's effect (losing two production staff alone moved urgent on-time delivery from 34% to 19%). A staggered rollout in three waves leaves a shrinking control group, about 70 control requests over 90 days, too few to read once each LO's requests are counted together. The 50/50 split gives each group about 100 urgent requests (15 LOs × about 2.3 a month × 3 months). Sample: 48 requests per arm at a 14% baseline and a +25 pt minimum lift (power 80%, significance 5%), or about 77 once each LO's requests are treated as related, so about 100 per arm covers it. Limitation: with 30 LOs, the test can confirm a large lift but not a small one. Control LOs get Nomi at the read date if it ships. |
| Primary metric | % of urgent partner requests (all channels: Nomi briefs, lender queue tickets, weekly LO check-in) answered with a compliance-reviewed asset within 1 business day, compared between the Nomi and control groups. Baseline 14%, target 60%, minimum worth shipping +25 pts (39%). Referral revenue is not the primary metric because it can't be read inside the test: the P90 time from lead to funding for a purchase loan is 164 days, well past the 90-day read date. It is also too rare to test at pilot scale: only a fraction of flyers lead to a referral, and only about 7% of referrals close and fund, so a significant difference in funded loans would take far more assets than 30 LOs send in 90 days. Referred applications and funded loans from partners tagged in the brief remain the lagging North Star, tracked for both groups and reviewed after the test. |
| Guardrail metric | Post-delivery compliance issue rate, from a 10% sampling audit of delivered assets with rates or trigger terms. Boundary: no higher in the Nomi group than for the control group's approved assets. Because the lender's compliance team holds the veto, a breach at any point pauses Nomi through the feature flag; this is a safety stop, not an early read of the primary metric. |
| Decision rule (ship / kill / pivot) | Ship if the Nomi group's rate beats the control by at least 25 pts at p < 0.05 and the compliance issue rate stays within its boundary at day 90: roll out to all of the lender's top producers, with new LOs next. Iterate if the Nomi group is ahead but by less than 25 pts: sharpen the chat brief or templates, or add a second lender for more sample, and re-run. Investigate if the lift clears 25 pts but the guardrail breaks, or results get worse for one branch or partner type: find who was harmed before any rollout. Kill if the Nomi group shows no improvement over the control or does worse. The read date is fixed at day 90, and no results are reviewed before then. |

## Findings & decision _(after running it)_

Not run yet. The test is planned with one lender: 30 top producers randomized 15/15 on day 0, with the read on day 90.
