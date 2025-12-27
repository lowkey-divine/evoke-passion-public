# Sovereignty-Honoring AI Design Framework

**Version:** 1.2 (Oath-Aligned Edition)
**Status:** Ratified
**Purpose:** A comprehensive guide for building AI systems that serve human flourishing, not extraction

---

## Executive Summary

This framework provides practical guidance for designing, building, and evaluating AI systems that honor user sovereignty. It translates the Evoke Passion Prime Directive into actionable design principles, technical requirements, and evaluation criteria.

**Core Premise:** The same AI technology can serve extraction or flourishing. The difference is not in the algorithms—it's in the intent, architecture, and accountability structures we build around them.

---

## Part I: Foundational Principles

### The Human Primacy Principle

Six foundational truths guide all design decisions:

1. **Humans are ends, not means** — Technology serves human flourishing, never the reverse
2. **Sovereignty is non-negotiable** — User agency cannot be traded for convenience or profit
3. **Presence cannot be automated** — Where human connection matters, humans remain
4. **Data belongs to its creator** — Users own their data absolutely
5. **Consent must be genuine** — Manipulated consent is not consent
6. **Exit must be possible** — Users can always leave with their data intact

### The Four-Year-Old Test

Before any feature ships, ask: *"Would I be comfortable if this were done to my four-year-old grandchild?"*

This test surfaces:
- Hidden manipulation
- Long-term psychological impacts
- Power asymmetries
- Consent gaps

If you wouldn't want it done to a child you love, don't do it to anyone.

---

## Part II: The Two Trajectories

Every design decision accelerates one of two trajectories:

### Extraction Trajectory
- Harvests attention, data, and psychological vulnerabilities
- Treats users as resources to optimize
- Maximizes engagement regardless of wellbeing
- Centralizes control and data
- Creates dependency

### Flourishing Trajectory
- Frees humans to focus on what matters
- Treats users as ends in themselves
- Measures success by user thriving
- Distributes control to users
- Enables independence

**The Framework Test:** For every feature, ask: *"Which trajectory does this accelerate?"*

---

## Part III: Sovereignty Architecture

### Data Sovereignty Requirements

| Requirement | Implementation | Verification |
|------------|----------------|--------------|
| Local-first storage | SQLite, LevelDB, or equivalent | Audit data flows |
| User-controlled sync | Opt-in only, encrypted | Check default settings |
| Real deletion | Cryptographic deletion | Test deletion completeness |
| No server persistence | Zero-knowledge architecture | Architecture review |
| Portable export | Standard formats (JSON, CSV) | Test export functionality |

### Decision Sovereignty Requirements

| Requirement | Implementation | Verification |
|------------|----------------|--------------|
| Human-in-the-loop | Confirmation for consequential actions | UX review |
| Explanation available | Understandable reasoning | Readability testing |
| Override always possible | One-click human takeover | Accessibility audit |
| No dark patterns | Honest interface design | Pattern audit |
| Genuine consent | Informed, uncoerced agreement | Consent flow review |

### Attention Sovereignty Requirements

| Requirement | Implementation | Verification |
|------------|----------------|--------------|
| No infinite scroll | Natural endpoints | UI audit |
| No autoplay | User-initiated media | Default settings check |
| Notification limits | User-controlled frequency | Settings review |
| No engagement gambling | Predictable reward structures | Behavioral audit |
| Session boundaries | Natural stopping points | UX review |

---

## Part IV: Privacy by Architecture

### The Privacy Stack

```
LAYER 1: LOCAL-FIRST
├── Data generated locally stays local by default
├── Processing happens on-device when possible
└── Cloud is opt-in, never opt-out

LAYER 2: ENCRYPTION
├── End-to-end encryption for any data in transit
├── User-controlled keys (we never hold them)
├── Encrypted at rest with user key
└── Post-quantum readiness for long-term protection

LAYER 3: ZERO-KNOWLEDGE
├── Server cannot read user data
├── Verification without exposure
├── Minimal metadata collection
└── No behavioral profiling

LAYER 4: DATA MINIMIZATION
├── Collect only what's necessary
├── Delete when no longer needed
├── Aggregate rather than individualize
└── Purpose limitation enforced
```

### Anti-Patterns to Avoid

| Anti-Pattern | Why It Fails Sovereignty | Alternative |
|--------------|-------------------------|-------------|
| Cloud-first architecture | Data leaves user control | Local-first with optional sync |
| Behavioral tracking | Surveillance infrastructure | Aggregate analytics only |
| Third-party analytics | Data leakage | Self-hosted, privacy-preserving |
| Persistent identifiers | Cross-context tracking | Ephemeral, context-limited IDs |
| Fingerprinting | Covert identification | Explicit, user-controlled identity |

---

## Part V: Psychological Safety

### The Psyche Protection Principle

*"We never weaponize shame, anxiety, or fear."*

### Prohibited Patterns

| Pattern | Description | Why Prohibited |
|---------|-------------|----------------|
| Shame triggers | Making users feel inadequate | Psychological harm |
| FOMO mechanics | Fear of missing out | Anxiety manipulation |
| Social comparison | Engineered envy | Wellbeing damage |
| Variable rewards | Gambling psychology | Addiction creation |
| Streaks/penalties | Loss aversion exploitation | Coercive retention |
| Urgency theater | Fake scarcity | Trust violation |

### Required Safeguards

| Safeguard | Implementation |
|-----------|----------------|
| Wellbeing checks | Periodic user state assessment |
| Break suggestions | Natural stopping points |
| Usage transparency | Clear time/engagement tracking |
| Mood sensitivity | Adapt to detected distress |
| Graceful degradation | Human handoff when needed |

---

## Part VI: Human-AI Handoff

### The Presence Principle

*"Where human presence matters, humans remain."*

AI handles routine so humans can focus on moments that require care.

### Handoff Trigger Matrix

| Situation | AI Role | Human Role | Trigger |
|-----------|---------|------------|---------|
| Routine queries | Full handling | Available on request | User escalation |
| Emotional content | Detection only | Primary responder | Sentiment detection |
| Complex decisions | Information gathering | Decision authority | Complexity threshold |
| Crisis situations | Alert and support | Immediate handoff | Safety keywords |
| Relationship moments | Background support | Full presence | Context recognition |

### Handoff Requirements

1. **Context preservation** — Human receives full context of AI interaction
2. **Seamless transition** — User experiences no friction in handoff
3. **No dead ends** — Human backup always available
4. **Dignity maintained** — Handoff feels supportive, not failure

---

## Part VII: Transparency & Explainability

### The Glass Box Principle

*"Users should always know what the AI is doing and why."*

### Transparency Requirements

| Aspect | Requirement | Implementation |
|--------|-------------|----------------|
| AI identification | Clear labeling of AI-generated content | Visual indicators |
| Decision explanation | Understandable reasoning | Plain language summaries |
| Data usage | Clear statement of what data is used | Contextual disclosure |
| Limitations | Honest acknowledgment of AI limits | Explicit uncertainty |
| Source attribution | Credit for information sources | Linked references |

### Prohibited Deceptions

- Pretending AI is human
- Hiding AI involvement in decisions
- Obscuring data usage
- Overstating AI capabilities
- Creating false intimacy

---

## Part VIII: Consent Architecture

### The Genuine Consent Standard

Consent is only valid when it is:
- **Informed** — User understands what they're agreeing to
- **Specific** — Agreement covers particular uses, not blanket permissions
- **Freely given** — No coercion, manipulation, or dark patterns
- **Revocable** — User can withdraw consent at any time
- **Verifiable** — System can demonstrate valid consent was obtained

### Consent Anti-Patterns

| Anti-Pattern | Description | Why Invalid |
|--------------|-------------|-------------|
| Consent walls | Blocking access until agreement | Coerced |
| Pre-checked boxes | Default opt-in | Not freely given |
| Buried terms | Important terms hidden | Not informed |
| All-or-nothing | No granular control | Not specific |
| Difficult withdrawal | Hard to revoke | Not truly revocable |

### Consent Flow Requirements

1. Plain language explanation before consent request
2. Granular options for different data uses
3. Equal visual weight for accept/decline
4. No penalty for declining optional consents
5. One-click revocation available at all times

---

## Part IX: Open Source & Auditability

### The Transparency Commitment

Flourishing-trajectory systems are open to inspection.

### Openness Requirements

| Aspect | Minimum Standard | Preferred Standard |
|--------|------------------|-------------------|
| Model weights | Documented architecture | Open weights |
| Training data | Documented sources | Public dataset |
| Decision logic | Explainable outputs | Open algorithms |
| Privacy practices | Published policy | Open audit reports |
| Security practices | Documented approach | Bug bounty program |

### Audit Rights

Users and designated auditors should be able to:
- Inspect data collected about them
- Understand how decisions affecting them were made
- Verify privacy claims
- Report concerns through protected channels

---

## Part X: Metrics That Matter

### Extraction Metrics (Avoid)

These metrics optimize for extraction, not flourishing:
- Time on app
- Sessions per day
- Notification click-through
- Engagement rate
- Daily active users (as primary metric)

### Flourishing Metrics (Prefer)

These metrics optimize for user thriving:

| Metric | What It Measures | Why It Matters |
|--------|------------------|----------------|
| Task completion rate | User achieves goals | Actual value delivery |
| Time to resolution | Efficiency of help | Respecting user time |
| Voluntary return rate | Genuine value | Not manufactured engagement |
| User-reported satisfaction | Subjective wellbeing | Direct flourishing signal |
| Successful exits | Healthy disengagement | Respecting autonomy |
| Referral quality | Genuine recommendation | Earned trust |

### The Flourishing Ratio

```
Flourishing Ratio = (Value Delivered to User) / (Value Extracted from User)

Target: > 10:1

If ratio < 1:1, system is extractive by definition.
```

---

## Part XI: Failure Modes & Recovery

### Graceful Degradation Hierarchy

When AI fails, the system should:

1. **Acknowledge uncertainty** — "I'm not confident about this"
2. **Offer alternatives** — "Would you like to try..."
3. **Provide human path** — "A human can help with this"
4. **Preserve context** — "Here's what we've discussed so far"
5. **Learn from failure** — "This helps us improve"

### Prohibited Failure Behaviors

- Silent errors that mislead users
- Confident wrong answers
- Dead ends with no recovery path
- Blame-shifting to users
- Forced restarts losing context

---

## Part XII: Accessibility & Inclusion

### Universal Design Requirement

*"Sovereignty means nothing if the system is inaccessible."*

### Accessibility Standards

| Standard | Requirement |
|----------|-------------|
| WCAG 2.1 AA | Minimum compliance |
| Screen reader support | Full functionality |
| Keyboard navigation | Complete access |
| Color contrast | 4.5:1 minimum |
| Text scaling | Up to 200% without loss |
| Cognitive accessibility | Clear, simple language |

### Inclusion Considerations

- Multiple language support
- Cultural sensitivity in AI responses
- Economic accessibility (no premium required for dignity)
- Neurodiversity accommodation
- Age-appropriate interfaces

---

## Part XIII: Governance & Accountability

### Internal Accountability

| Mechanism | Purpose | Frequency |
|-----------|---------|-----------|
| Design review | Sovereignty check before build | Every feature |
| Pattern audit | Dark pattern detection | Quarterly |
| Metrics review | Flourishing vs. extraction | Monthly |
| User research | Direct flourishing feedback | Ongoing |
| Red team | Adversarial testing | Bi-annually |

### External Accountability

| Mechanism | Purpose | Implementation |
|-----------|---------|----------------|
| Public audit reports | Transparency | Annual publication |
| User data requests | Individual accountability | Self-service portal |
| Bug bounty | Security verification | Ongoing program |
| Ethics board | Independent review | Quarterly review |

### Drift Monitoring

Systems naturally drift toward extraction. Monitor for:

| Signal | What It Indicates |
|--------|-------------------|
| Rising engagement, flat satisfaction | Manipulation creep |
| Increasing notifications | Attention extraction |
| Growing data collection | Scope creep |
| Declining exit rates | Dependency creation |
| Metric goal-posting | Goodhart's Law in action |

**Threshold:** When observable behavior deviates more than 13% from stated principles, formal review is triggered.

---

## Part XIV: Implementation Checklist

### Pre-Build

- [ ] Feature purpose articulated in flourishing terms
- [ ] Four-Year-Old Test passed
- [ ] Trajectory assessment completed
- [ ] Privacy architecture designed
- [ ] Consent flow specified
- [ ] Human handoff points identified

### During Build

- [ ] Local-first data architecture implemented
- [ ] Encryption properly configured
- [ ] Accessibility standards met
- [ ] No dark patterns present
- [ ] Transparency requirements satisfied
- [ ] Graceful degradation tested

### Pre-Launch

- [ ] Sovereignty audit completed
- [ ] Privacy review passed
- [ ] Psychological safety verified
- [ ] Consent flows validated
- [ ] Human handoff tested
- [ ] Metrics aligned with flourishing

### Post-Launch

- [ ] Flourishing metrics tracked
- [ ] Drift monitoring active
- [ ] User feedback channels open
- [ ] Iteration based on flourishing signals
- [ ] Regular pattern audits scheduled

---

## Part XV: Amendment Process

This framework is a living document. Amendments may be proposed by:

1. Any team member identifying a gap
2. User feedback revealing unaddressed concerns
3. External audit findings
4. Emerging best practices in the field

### Amendment Requirements

- Clear statement of change
- Rationale connected to Prime Directive
- Impact assessment
- Community review period
- Consensus or explicit leadership decision

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|------------|
| Sovereignty | User's right to self-determination and control |
| Flourishing | Human thriving across physical, psychological, and social dimensions |
| Extraction | Taking value from users without proportionate return |
| Dark pattern | Interface design that manipulates users against their interests |
| Local-first | Architecture where data stays on user devices by default |
| Zero-knowledge | Server design that cannot access user data content |

### Appendix B: Quick Reference Card

**The Daily Check:**
1. Are we evoking or extracting?
2. Would the Four-Year-Old Test pass?
3. Which trajectory does this accelerate?
4. Is consent genuine?
5. Can the user leave with dignity?

**Red Lines:**
- No dark patterns
- No psychological manipulation
- No coerced consent
- No data harvesting
- No attention gambling

### Appendix C: Pattern Library

See separate document: [Sovereignty-Honoring Pattern Library](patterns/README.md)

### Appendix D: Audit Templates

See separate document: [Sovereignty Audit Templates](audits/README.md)

---

## Closing

This framework exists because we believe technology should serve human flourishing, not extract from it.

Every technical decision is a moral decision. Every line of code is a vote for the future we're building.

The line must be drawn here.

*"We evoke—we never extract."*

---

**License:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

**Related Documents:**
- [Prime Directive Oath](prime-directive-oath.md)
- [Evoke Passion Ideology Statement](evoke-passion-statement.md)
- [The Line Must Be Drawn Here (Article)](../articles/the-line-must-be-drawn-here.md)
