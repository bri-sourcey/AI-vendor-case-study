# AI Voice Agent Platform Evaluation: A Business Case Study

## Executive Summary

Engaged as a Business Analyst for [Client], a high-volume outbound sales organization processing 200,000+ customer contacts monthly. The organization faced significant regulatory exposure due to call abandonment rates substantially exceeding the 3% FCC compliance threshold, while simultaneously losing potential revenue from dropped customer connections.

Conducted end-to-end vendor evaluation for AI-powered voice agent platforms, analyzing build vs. buy vs. replace strategies. Developed cost projection models, gathered and analyzed operational data across 56 agents and 480+ concurrent call lines, and delivered a vendor recommendation based on pricing structure, implementation timeline, and scalability requirements.

Currently leading implementation of the selected solution, with a phased rollout strategy including AI-assisted call handling (Phase 1) and intelligent call routing optimization (Phase 2).

---

## Business Problem & Context

### Situation

[Client] operated a high-volume outbound sales center with 56 agents handling warranty and service contracts. Despite strong sales performance, the organization faced critical operational challenges stemming from legacy dialing infrastructure.

### Operational Snapshot

Through independent data gathering and analysis, I identified the following baseline metrics:

- **Daily call volume:** 214,000+ calls (95.6% outbound)
- **Peak concurrent calls:** 480+
- **Active agents:** 56
- **Average hold time before abandonment:** 8 seconds
- **Call abandonment rate:** Substantially above FCC's 3% compliance threshold

### The Problem

The core issue was twofold:

**1. Regulatory Exposure**
FCC regulations limit outbound call abandonment to 3%. [Client]'s rates far exceeded this threshold, creating significant compliance risk and potential liability.

**2. Revenue Leakage**
Dropped calls represented missed customer connections. With an average deal profit of ~$2,800 and weekly revenue exceeding $300,000, even marginal improvements in connection rates translated to substantial revenue opportunity.

### The Ask

Leadership engaged me to evaluate AI-powered voice agent solutions that could bridge the gap between customer pickup and agent availability—reducing abandonment rates while maintaining (or improving) sales performance.

---

## Evaluation Methodology

### Strategic Approaches Considered

I evaluated three distinct approaches to solving the call abandonment problem:

**Approach 1: DIY Build**
- Platforms: Twilio, ReDial
- Concept: Build custom AI voice solution in-house

**Approach 2: Managed Service**
- Platforms: [AI Platform Provider], Genesys
- Concept: Implement turnkey AI voice platform with vendor support

**Approach 3: Full System Replacement**
- Platforms: Dialpad, Kore.ai
- Concept: Replace entire telephony infrastructure

### Elimination Rationale

**DIY Build — Eliminated**
- Would have required me to serve as both developer AND analyst, despite limited software engineering background
- Estimated 500+ hours of solo development
- Ongoing maintenance burden (10+ hours/week indefinitely)
- No additional technical resources available for support
- High technical risk: building mission-critical compliance infrastructure without dedicated engineering expertise
- Timeline incompatible with urgency of compliance exposure

**Full System Replacement — Eliminated**
- Extended implementation timeline (months vs. weeks)
- Significant operational disruption during transition
- Higher cost and complexity beyond immediate scope
- Compliance issue required faster resolution

**Managed Service — Selected**
- Fastest path to compliance (72 hours to 1 week soft launch)
- Vendor handles backend maintenance and updates
- Purpose-built for high-volume outbound operations
- Scalable to 50,000+ concurrent calls

### Evaluation Criteria

For the managed service options, I assessed vendors against the following:

| Category | Criteria |
|----------|----------|
| Pricing | Model structure (per-minute vs. per-call), voicemail handling costs, setup fees |
| Technical | Latency, LLM backbone, concurrency ceiling, CRM integration |
| Implementation | Timeline to soft launch, onboarding support, contract flexibility |
| Compliance | Call recording, audit trails, abandonment rate management |

---

## Cost Analysis

### The Pricing Model Insight

A critical finding during vendor evaluation was the impact of pricing structure on total cost of ownership. Most AI voice platforms charge per minute of call time ($0.11 - $0.16/min industry average). [AI Platform Provider] offered a per-call model, which proved more cost-effective at [Client]'s volume.

### Vendor Pricing Structure

| Factor | [AI Platform Provider] |
|--------|------------------------|
| Pricing Model | Per connected call |
| Setup/Onboarding | $3,000 - $5,000 |
| Per Connected Call | $0.16 |
| Per Voicemail | $0.01 |
| Contract Terms | Month-to-month |
| Concurrency Ceiling | 50,000+ |

### Projected Monthly Cost by Implementation Scope

To help leadership visualize costs at different adoption levels, I developed the following projections based on ~7,600 daily dropped calls:

| AI Coverage | Calls Handled/Day | Monthly Cost Range |
|-------------|-------------------|-------------------|
| 10% | ~760 | $5,675 - $7,675 |
| 50% | ~3,800 | $16,736 - $18,376 |
| 100% | ~7,600 | $29,752 - $31,752 |

---

## Technical Evaluation

### Demo & Discovery

During vendor demonstrations, I leveraged prior experience training conversational AI models to evaluate technical capabilities beyond surface-level features.

Key areas of inquiry included:

- **LLM Backbone:** What model powers the conversational AI? ([AI Platform Provider] uses GPT-4o Mini)
- **Latency:** Response time between customer speech and AI reply — critical for natural conversation flow
- **Token Usage:** How the platform handles context windows and conversation memory
- **Concurrency:** Can the system handle 480+ simultaneous calls at peak?

### Technical Requirements Matrix

| Requirement | [AI Platform Provider] Capability |
|-------------|-----------------------------------|
| LLM | GPT-4o Mini |
| Hosting | In-house (not third-party cloud) |
| Latency | ~300ms response time |
| VICIdial Integration | Yes |
| CRM Integration | Yes |
| Voicemail Detection | Yes |
| Call Transcription | Yes |
| Conversation Summary | Yes (GPT-4o Mini) |
| Concurrency Ceiling | 50,000+ |
| Smart Routing | Phase 2/3 |
| AI Whisper (Agent Assist) | Phase 2/3 |

### The 8-Second Question

The core technical question I posed to [AI Platform Provider]: 

*"Our average hold time before abandonment is 8 seconds. Can your AI answer and engage the customer within that window?"*

With ~300ms latency from their in-house infrastructure, the platform could respond well within the critical window. Their system was designed specifically for this use case — AI "hold agents" that pick up immediately, collect preliminary information, and warm-transfer to the next available human agent.

---

## Compliance & Regulatory Considerations

As part of the implementation planning, I researched applicable telecommunications regulations to ensure the AI solution and associated call scripts would meet compliance requirements.

Key areas reviewed:

- **TCPA (Telephone Consumer Protection Act):** Verified call scripts adhered to disclosure and consent requirements
- **Call Recording Disclosure:** Ensured proper notification at call initiation (required under California two-party consent law)
- **DNC Compliance:** Confirmed processes for honoring Do Not Call registry requests
- **RND (Reassigned Numbers Database):** Reviewed requirements for checking reassigned phone numbers to avoid contacting wrong parties

*Note: This research was conducted for due diligence purposes to inform implementation planning, not as legal counsel.*

---

## Additional Insights: Sales & Compliance Analysis

Beyond the AI vendor evaluation, I developed Python scripts to analyze sales performance and compliance metrics across the organization. This analysis surfaced insights that extended beyond the original project scope.

📁 **Code Repository:** [Business Intelligence Analytics Suite](https://github.com/bri-sourcey/Business-Intelligence-Analytics-Suite)

### Data Analyzed

- Weekly sales performance (4-day sample)
- Individual rep conversion rates
- Down payment compliance by rep (3% minimum internal requirement)
- Day-over-day compliance trends

### Key Findings

**Overall Performance:**
- Total Revenue: $326,843
- Total Gross Profit: $240,589
- Average Deal Profit: $2,797
- Total Deals Closed: 86
- Overall Compliance: $41,641 collected vs $9,805 required

However, only 62.8% of individual deals met the 3% down payment minimum — indicating potential risk at the deal level despite strong aggregate numbers.

### Compliance Trends by Rep

| Rep | Compliance Trend | Flag |
|-----|------------------|------|
| Rep A | 100% | Consistent performer |
| Rep B | 100% → 78% | Declining |
| Rep C | 88% → 69% | Declining |
| Rep D | 58% → 78% | Improving |
| Rep E | 73% → 53% | Top earner, low compliance |
| Rep F | 50% | Top earner, low compliance |
| Rep G | 0% | Below threshold |

### Flags Raised to Leadership

1. **Top earners with lowest compliance:** Reps E and F drove significant revenue but may have been cutting deals on down payments to close sales — creating potential risk exposure.

2. **Declining compliance mid-week:** Multiple reps showed declining compliance rates over the sample period, suggesting a pattern worth monitoring.

3. **Consistent underperformance:** One rep collected below the 3% minimum requirement across all deals.

### Relevance to AI Implementation

This analysis directly informed the Phase 2 recommendation for intelligent call routing. By identifying high-performing AND compliant reps, the AI system could prioritize routing calls to agents most likely to close quality deals — not just any deals.

---

## Implementation Roadmap

Based on vendor capabilities and organizational needs, I proposed a phased implementation strategy to minimize disruption while addressing the compliance issue quickly.

### Phase 1: AI Hold Agents (Immediate Priority)

**Objective:** Reduce call abandonment rate to FCC compliance threshold

**Solution:** Deploy AI agents to answer calls within the 8-second window when human agents are unavailable. The AI:
- Greets the customer immediately
- Collects preliminary information
- Warm-transfers to next available human agent

**Timeline:** 72 hours to 1 week soft launch

**Expected Outcome:** Significant reduction in dropped calls, improved regulatory posture

### Phase 2: Intelligent Call Routing

**Objective:** Optimize call distribution for quality AND compliance

**Solution:** Route inbound transfers to top-performing, high-compliance reps based on performance data analysis (see Section 6)

**Expected Outcome:** Higher close rates on compliant deals, reduced risk exposure from low-compliance closers

### Phase 3: AI Whisper (Agent Assist)

**Objective:** Improve agent performance and customer experience

**Solution:** AI provides real-time information to agents via webhook before/during calls:
- Customer history
- Vehicle information
- Relevant account details

**Expected Outcome:** Faster call resolution, more informed conversations, improved customer satisfaction

### Current Status

Implementation is currently in progress. Call scripts and rebuttal examples have been submitted to [AI Platform Provider], and soft launch coordination is underway. Project documentation has been transitioned to ensure continuity.

---

## Key Takeaways

**Pricing Structure as Strategic Differentiator**
At high volume, the pricing model (per-call vs per-minute) had greater impact on total cost of ownership than the rate itself. Vendor evaluation must account for operational scale.

**Quantified Business Cases Drive Decisions**
Converting operational issues into financial impact — projected revenue loss, cost scenarios by adoption level — enabled faster executive buy-in than qualitative assessments alone.

**Build vs. Buy Requires Honest Assessment**
Evaluating internal capabilities objectively (timeline, expertise, maintenance burden) prevented costly overcommitment to a custom solution the organization wasn't equipped to support.

**Data Analysis Surfaces Adjacent Risks**
Compliance tracking by rep revealed performance patterns outside the original project scope, informing future optimization strategies (Phase 2 intelligent routing).

**Regulatory Due Diligence is Foundational**
Researching TCPA, consent requirements, and DNC compliance during planning ensured the solution addressed existing risk without introducing new exposure.

**Scope Flexibility Within Structure**
Project requirements evolved significantly from initial research to full implementation leadership. Documenting decisions and maintaining clear deliverables allowed adaptation without loss of direction.

---

## Conclusion

This engagement demonstrates the value of structured analysis in technology vendor evaluation. By quantifying operational challenges, assessing multiple strategic approaches, and conducting thorough technical and regulatory due diligence, I delivered a recommendation that addressed both immediate compliance risk and long-term scalability.

The phased implementation strategy — beginning with AI hold agents and expanding to intelligent routing and agent assist capabilities — provides [Client] a path to regulatory compliance while optimizing sales performance.

Project documentation and analysis tools have been transitioned to ensure implementation continuity.

---

## Author

**Brianna Savoy**  
Data Analyst | MBA Candidate (2027)

**Repository:** [Business Intelligence Analytics Suite](https://github.com/bri-sourcey/Business-Intelligence-Analytics-Suite)
