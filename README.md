# UX Case Study: Increasing Feature Adoption in an Enterprise SaaS Dashboard

**Role:** Staff UX Researcher & Designer  
**Timeline:** 12 weeks  
**Platform:** Enterprise SaaS — Web Dashboard  
**Status:** Completed  

---

## Table of Contents

1. [Overview](#overview)
2. [The Problem](#the-problem)
3. [Goals & Success Metrics](#goals--success-metrics)
4. [Research Approach](#research-approach)
5. [What We Found](#what-we-found)
6. [Design Process](#design-process)
7. [Key Decisions & Rationale](#key-decisions--rationale)
8. [Outcomes](#outcomes)
9. [What I Learned](#what-i-learned)
10. [Methodology Reference](#methodology-reference)

---

## Overview

**Meridian Analytics** is a fictional enterprise SaaS platform used by operations managers at mid-to-large logistics companies. The platform includes a powerful **Predictive Insights Panel** — a feature that surfaces AI-generated recommendations to help managers optimize route efficiency and reduce operational costs.

Despite being a flagship capability, adoption of the Predictive Insights Panel sat at **11% across active accounts** six months after launch. Leadership flagged it as a critical business risk. This case study documents the end-to-end UX research and design process used to diagnose the adoption gap and deliver a solution.

---

## The Problem

> *"We built a feature our users aren't using. We need to understand why before we build anything else."*  
> — Product Director, Meridian Analytics

### Symptoms observed at project start

- 11% feature adoption rate at 6 months post-launch
- High drop-off at the panel entry point — users clicked in and left within 8 seconds
- Support tickets referencing confusion about what the panel was "for"
- Qualitative signals from account managers: users described the feature as "too complicated" or "not relevant to my job"

### What we did NOT know yet

- Whether the problem was **discoverability**, **comprehension**, **relevance**, or **trust**
- Whether the issue was consistent across user roles or isolated to specific segments
- Whether users had tried the feature and abandoned it, or never tried it at all

---

## Goals & Success Metrics

Before beginning research, the team aligned on what success would look like. Defining this upfront prevented scope creep and kept design decisions anchored to measurable outcomes.

| Goal | Metric | Target |
|---|---|---|
| Increase feature adoption | % of active users engaging with panel | 40%+ within 90 days of redesign |
| Improve comprehension | % of users who can correctly describe the panel's purpose | 80%+ in usability testing |
| Reduce time-to-first-action | Time from panel open to first meaningful interaction | Under 60 seconds |
| Reduce support tickets related to panel | Volume of confusion-related tickets | 30% reduction |

---

## Research Approach

### Methods used

**1. Analytics Review**  
Reviewed session data and funnel drop-off points to understand *where* users were leaving and *how often* the panel was even reached from the main dashboard.

**2. Support Ticket Analysis**  
Categorized 3 months of support tickets mentioning the Predictive Insights Panel. Coded tickets by theme: confusion, relevance, technical error, and feature request.

**3. Stakeholder Interviews (Internal)**  
Spoke with 4 account managers and 2 product managers to gather secondhand user feedback and understand how the feature had been communicated at launch.

**4. User Interviews (External)**  
Conducted 8 moderated remote interviews with active platform users across 3 role types:
- Operations Managers (primary persona)
- Fleet Coordinators (secondary persona)
- Regional Directors (decision-maker persona)

Interview focus areas:
- Current daily workflow and pain points
- How they currently make operational decisions
- What they knew about the Predictive Insights Panel
- What "helpful" would look like in a dashboard feature

**5. Usability Testing (Existing Design)**  
Ran 5 unmoderated usability sessions using the current panel design. Participants were asked to complete a defined task using the panel with no instruction.

---

## What We Found

### Finding 1 — Discoverability was not the primary issue
Users could physically locate the panel. The entry point in the navigation was seen by 74% of users in session recordings. The problem was not that they couldn't find it — it was that they didn't know what they would find when they opened it.

### Finding 2 — The panel spoke the wrong language
The panel used data science terminology — "confidence intervals," "predictive variance," "weighted optimization scores" — that was unfamiliar and anxiety-inducing for operations managers who think in terms of routes, drivers, and delivery windows.

> *"I clicked on it once and saw a bunch of numbers I didn't understand. I figured it wasn't for me."*  
> — Operations Manager, Interview Participant 4

### Finding 3 — Trust was the hidden barrier
Users did not trust AI-generated recommendations enough to act on them without understanding the reasoning behind them. The panel surfaced *what* to do with no explanation of *why*.

> *"If I'm going to change a driver's route based on something the system told me, I need to know why it's telling me that."*  
> — Fleet Coordinator, Interview Participant 7

### Finding 4 — Role relevance varied significantly
Regional Directors found the panel highly relevant — it gave them portfolio-level visibility. Operations Managers found it overwhelming — they needed action-level specificity, not aggregate trends. The panel had been designed for one mental model and deployed across three.

### Synthesis — Root cause
The adoption gap was caused by a combination of **comprehension failure** and **trust deficit**, compounded by a **one-size-fits-all information architecture** that served no single role particularly well.

---

## Design Process

### Phase 1 — Define & Align
Synthesized research findings into a single problem statement presented to the full cross-functional team:

> *"Operations managers avoid the Predictive Insights Panel because they don't understand what it's recommending, don't trust the source of the recommendation, and can't connect it to the actions they take in their daily workflow."*

This framing shifted the team's mental model from "adoption problem" to "comprehension and trust problem" — a meaningful reframe that changed what solutions were considered.

### Phase 2 — Ideation Workshop
Facilitated a 2-hour cross-functional workshop with product, engineering, and customer success. Used structured prompts to generate ideas across three problem areas:

- How might we make recommendations understandable without requiring data science knowledge?
- How might we show users why a recommendation was made?
- How might we tailor the panel experience to different role needs?

Generated 34 ideas. Prioritized using an impact/effort matrix down to 6 concepts for prototyping.

### Phase 3 — Concept Development
Developed 3 low-fidelity concept directions in Figma:

**Concept A — Plain Language Recommendations**  
Rewrote all panel content in operational language. Replaced "confidence interval: 0.87" with "High confidence — based on 14 similar routes this quarter."

**Concept B — Recommendation Cards with Reasoning**  
Introduced expandable "Why is this recommended?" cards that showed the 3 key factors driving each recommendation in plain language.

**Concept C — Role-Based Panel Views**  
Created distinct panel configurations for Operations Managers (action-level) and Regional Directors (portfolio-level) with a shared data layer underneath.

### Phase 4 — Usability Testing (Concepts)
Tested all 3 concepts with 6 participants across role types. Key findings:

- Concept A alone was insufficient — users appreciated the language but still wanted reasoning
- Concept B had the highest comprehension scores and highest trust ratings
- Concept C was logistically complex and created confusion during switching
- **Winning direction:** Concept B with plain language from Concept A integrated throughout

### Phase 5 — High-Fidelity Design & Iteration
Built high-fidelity mockups in Figma incorporating:
- Plain language throughout
- Expandable reasoning cards ("Why this recommendation?")
- Contextual glossary tooltips for any retained technical terms
- A confidence indicator redesigned as a visual signal (not a number)
- Onboarding overlay for first-time panel visitors

Ran 2 rounds of design critique with engineering and product before finalizing specifications.

### Phase 6 — Developer Handoff
Delivered annotated Figma files with:
- Component specifications and spacing documentation
- Interaction notes for expand/collapse behavior
- Accessibility annotations (color contrast, screen reader labels, focus order)
- Edge case documentation for empty states and loading states

---

## Key Decisions & Rationale

### Decision 1 — Lead with action, not data
**What:** Restructured the panel to lead with a recommended action, followed by supporting data — not the reverse.  
**Why:** Users think in terms of what to do, not what the data says. Leading with data required them to do interpretive work before understanding relevance.

### Decision 2 — Make reasoning visible but optional
**What:** "Why this recommendation?" is a progressive disclosure element — collapsed by default, expandable on demand.  
**Why:** Novice users needed reassurance that reasoning existed. Expert users wanted access to it. Making it always-visible added cognitive load for users who had already built trust. Progressive disclosure served both.

### Decision 3 — Retire role-based views for this release
**What:** Chose not to implement role-based panel configurations despite user research supporting the concept.  
**Why:** Engineering complexity and timeline risk outweighed the benefit for this release. Flagged as Phase 2 opportunity with supporting research documentation handed off to the product team.

### Decision 4 — Confidence as signal, not score
**What:** Replaced the numerical confidence score (0.87) with a three-state visual indicator: High / Medium / Low confidence.  
**Why:** Usability testing showed the numerical score created more anxiety than trust. The simplified signal communicated the same meaning without triggering statistical interpretation.

---

## Outcomes

Results measured 90 days post-launch of the redesigned panel:

| Metric | Baseline | Post-Launch | Change |
|---|---|---|---|
| Feature adoption rate | 11% | 47% | **+36 points** |
| Comprehension (usability testing) | 32% | 88% | **+56 points** |
| Time to first meaningful action | 4m 12s | 48 seconds | **−74%** |
| Confusion-related support tickets | 42/month | 19/month | **−55%** |

---

## What I Learned

**Research reframes the problem.** The team believed this was a discoverability problem. Research revealed it was a trust and comprehension problem. Without that reframe, the proposed solution would have been to make the panel more prominent — which would have driven more users to an experience that still didn't work.

**Trust is a design material.** Transparency about reasoning is not a nice-to-have in enterprise AI products. It is a prerequisite for adoption. Users will not act on recommendations they cannot interrogate.

**Saying no is a design decision.** Choosing not to implement role-based views in this release — and documenting why — was as important as any design choice made. Scope discipline protected the team and delivered a better focused outcome.

**Plain language is a design system issue.** The terminology problem was not isolated to this panel. It was a content design gap across the platform. This case study became the evidence used to advocate for a content design standard added to the design system.

---

## Methodology Reference

This case study applies the following UX research and design methods. Use this as a reference for your own practice.

| Method | Purpose | When to use |
|---|---|---|
| Analytics review | Understand *where* and *how often* problems occur | Early discovery — before talking to users |
| Support ticket analysis | Identify recurring pain points at scale | Early discovery — efficient signal gathering |
| Stakeholder interviews | Gather secondhand user knowledge, align on context | Before external research |
| User interviews | Understand mental models, motivations, and language | Discovery and definition phases |
| Usability testing (existing) | Diagnose specific interaction failures | Before redesigning anything |
| Ideation workshop | Generate diverse solutions collaboratively | After problem definition |
| Low-fidelity prototyping | Test concepts quickly before investing in detail | Early design phase |
| Usability testing (concepts) | Validate direction before high-fidelity investment | Mid design phase |
| High-fidelity prototyping | Communicate final design intent | Before developer handoff |
| Annotated handoff | Ensure design intent survives implementation | End of design phase |

---

## How to Use This Repository

This case study is a **methodology template**. To create your own:

1. Replace the fictional company and product with your own context
2. Keep the structure — Problem → Research → Findings → Process → Decisions → Outcomes
3. Lead with a quantified outcome in your Overview — it earns the reader's attention
4. Document your *decisions and rationale*, not just your deliverables — this is what separates designers who think from designers who execute
5. Be honest about what didn't make it in and why — scope discipline is a professional strength

---

## Support This Work

If this framework has been useful for your GovCon pursuits, consider buying me a coffee. It helps me keep building open source tools for the design and GovCon community.

<a href="https://buymeacoffee.com/teamdesignstudios" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-black.png" 
  alt="Buy Me A Coffee" width="200">
</a>

---

*Created by Susan E. Aldridge | [LinkedIn](https://www.linkedin.com/in/susanealdridge/) | [Portfolio](https://docsend.com/view/s/9bzhycnqab7k92nq)*
