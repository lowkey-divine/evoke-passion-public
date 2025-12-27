# Evoke Passion Privacy Framework

**Status:** Active
**Adopted:** December 27, 2025
**Authored by:** Evoke Passion Leadership + Infrastructure Team
**Scope:** Organization-wide (all products, operations, and community interactions)

---

## Preamble

> *"We evoke—we never extract."*
> — Evoke Passion Organizational Ideology

> *"Data belongs to those who create it."*
> — Evoke Passion Statement, Principle 2

This framework codifies Evoke Passion's commitment to privacy across all products, operations, and community interactions. It is not a legal document—it is a statement of values made operational.

**This framework applies to:**
- All Evoke Passion products (Ezri, Executive Chef, future products)
- The Evoke Passion public website
- All agent implementations and AI systems
- Community interactions and communications
- Partnership and external engagement data
- Internal operations and development practices

---

## Part I: Core Privacy Principles

### Principle 1: Local-First Architecture

> *"Data never leaves the machine unless the user explicitly chooses."*

**Commitment:**
- All Evoke Passion products default to local data storage
- Cloud sync is always opt-in, never default
- Users can use our products without any server interaction
- We build for air-gapped environments

**Implementation:**
- Local databases for all user data
- Offline-first application design
- Optional encrypted backup to user-controlled storage
- No required account creation for core functionality

---

### Principle 2: Zero-Knowledge Architecture

> *"We cannot access what we cannot decrypt."*

**Commitment:**
- User-encrypted data remains inaccessible to Evoke Passion
- Encryption keys are held by users, not by us
- Even under legal compulsion, we cannot provide what we cannot read

**Implementation:**
- User-generated encryption keys (X25519/Ed25519)
- Client-side encryption before any data leaves device
- Password-derived keys using Argon2id
- Post-quantum readiness in architectural planning

---

### Principle 3: Data Sovereignty

> *"Users own their data. Period."*

**Commitment:**
- Full data export in portable, open formats
- Real deletion (not archival) within 30 days
- No data sold, shared, or used for training without explicit consent
- Users can take their data and leave at any time

**Implementation:**
- Standard export formats (JSON, open schemas)
- Deletion workflows with confirmation
- No data retention beyond stated purposes
- Clear data portability documentation

---

### Principle 4: Minimal Collection

> *"Collect only what is necessary. Nothing more."*

**Commitment:**
- We collect the minimum data required for functionality
- We do not collect data "just in case"
- We actively refuse data we don't need

**Implementation:**
- Data inventory for each product
- Regular audits for unnecessary collection
- Privacy review for all new features
- Default to not collecting

---

### Principle 5: No Surveillance

> *"We build tools, not traps."*

**Commitment:**
- No behavioral tracking or pattern analysis
- No attention metrics or engagement optimization
- No third-party tracking or analytics
- No device fingerprinting or cross-site tracking

**Implementation:**
- No Google Analytics, Facebook Pixel, or equivalent
- No tracking cookies
- No telemetry without explicit opt-in
- Privacy-respecting alternatives only (if any analytics needed)

---

### Principle 6: Open Source Transparency

> *"Auditable code builds auditable trust."*

**Commitment:**
- Core infrastructure is open source
- Privacy-critical code is publicly reviewable
- No hidden telemetry or data collection
- Community can verify our claims

**Implementation:**
- Public repositories for core systems
- Open documentation of data flows
- Transparent architecture decisions
- Regular external security audits

---

## Part II: Data Classification (Organization-Wide)

### Tier 1: Sacred Data (User-Encrypted)

Data that Evoke Passion **can never access**.

| Data Type | Products | Storage | Encryption |
|-----------|----------|---------|------------|
| Shadow/personal content | Ezri | Client-only | User's private key |
| Private reflections | Ezri, Executive Chef | Client-only | User's private key |
| Sensitive personal data | All | Client-only | User's private key |

**Guarantee:** This data is encrypted before leaving the device. We store only ciphertext (if synced) or nothing at all.

---

### Tier 2: Sovereign Data (User-Controlled)

Data that **belongs to the user**—we may process it, but user controls access and deletion.

| Data Type | Products | User Control |
|-----------|----------|--------------|
| User preferences | All | Full export, real deletion |
| Account information | All | Full export, real deletion |
| Usage history | All | Full export, real deletion |
| Created content | All | Full export, real deletion |

**Guarantee:** User can export all Tier 2 data. Deletion removes data within 30 days.

---

### Tier 3: Operational Data (Minimal, Anonymized)

Data that Evoke Passion needs to **operate**.

| Data Type | Purpose | Anonymization |
|-----------|---------|---------------|
| Account identifier | Authentication | Pseudonymous |
| Auth credentials | Login | Irreversible hash |
| Aggregate statistics | Product improvement | Fully anonymized |
| Error logs | Debugging | No user identifiers, 7-day retention |

**Guarantee:** Cannot be used to reconstruct user identity.

---

### Tier 4: Forbidden Data

Data that Evoke Passion **will never collect**.

| Data Type | Reason |
|-----------|--------|
| Behavioral patterns for prediction | Surveillance; violates sovereignty |
| Emotional state inference | Manipulation potential |
| Location data (unless explicitly needed) | Privacy risk |
| Device fingerprinting | Tracking mechanism |
| Third-party tracking data | Violates trust |
| Data for sale | Violates everything |
| Biometric data (unless user-encrypted) | High sensitivity |
| Cross-product tracking | Violates boundaries |

---

## Part III: Product-Specific Implementation

### Ezri

Ezri implements the full privacy architecture with:
- Zero-knowledge encryption for sensitive content
- Anonymous journey option (no account required)
- Constellation sharing with full anonymization
- Local-first with optional encrypted sync

See Ezri's detailed privacy architecture in its product documentation.

---

### Executive Chef

**Privacy Implementation:**
- Local-first meal planning and family data
- No cloud requirement for core functionality
- Family data encrypted at rest
- No third-party analytics or tracking
- GDPR/CCPA compliant data handling

---

### Evoke Passion Website

**Privacy Implementation:**
- No analytics or tracking scripts
- No cookies except essential session management
- No third-party resources that track users
- Static site generation (no server-side user tracking)
- Privacy policy published and accessible

---

### Agent Implementations

**Privacy Implementation:**
- All agent execution is local
- No data sent to external AI services (local inference only)
- No logging of user interactions beyond session
- No training on user data

---

### Future Products

All future Evoke Passion products MUST:
1. Complete privacy review before launch
2. Implement this framework by default
3. Document any deviations with justification
4. Receive Privacy Guardian approval

---

## Part IV: Operational Standards

### Secrets Management

- No plaintext credentials in repositories
- No default passwords in configurations
- Secrets stored in secure vaults, not files
- Pre-commit hooks for secret detection
- Regular credential rotation

---

### Third-Party Services

**Default Position:** No third-party services that collect user data.

**If third-party service is necessary:**
1. Privacy review required
2. Data Processing Agreement required
3. EU-adequate protection required
4. Minimal data sharing only
5. Documentation of what's shared

---

### Development Practices

- Privacy review for all new features
- Security scanning in CI/CD pipeline
- No telemetry in production without opt-in
- Local development environments (no cloud dev)
- Audit logging for data access

---

### Community Data

**What we collect:**
- Email for newsletter (explicit opt-in)
- Feedback submitted voluntarily
- Community contributions (attributed by choice)

**What we don't collect:**
- Browsing behavior on our sites
- Engagement metrics beyond basic page views
- Social media tracking
- Cross-site behavior

---

### Partnership Data

- Minimal data shared with partners
- Data Processing Agreements required
- Partner privacy practices reviewed
- User consent for any data sharing
- Clear documentation of what's shared

---

## Part V: Legal Compliance

### GDPR Compliance

| Requirement | Implementation |
|-------------|----------------|
| Lawful basis | Consent (explicit, withdrawable) |
| Data minimization | Collect only what's needed |
| Purpose limitation | Data used only for stated purposes |
| Right to access | Full export available |
| Right to erasure | Real deletion within 30 days |
| Right to portability | Standard export format |
| DPO | To be designated |

---

### CCPA Compliance

| Requirement | Implementation |
|-------------|----------------|
| Right to know | Privacy policy + export |
| Right to delete | Real deletion |
| Right to opt-out | No sale of data (ever) |
| Non-discrimination | No service degradation for privacy choices |

---

### UK Data Protection

| Requirement | Implementation |
|-------------|----------------|
| UK GDPR alignment | Full compliance |
| International transfers | EU-first, adequacy required |
| ICO registration | To be completed if required |

---

### Our Standards (Higher Than Legal)

| Standard | Requirement |
|----------|-------------|
| Collection | Less than legally permitted |
| Deletion | Faster than legally required |
| Transparency | More detail than required |
| User control | More than legally mandated |

---

## Part VI: Governance & Accountability

### Privacy Roles

| Role | Responsibility |
|------|----------------|
| Privacy Guardian | Encryption, technical privacy |
| Identity Steward | Access control, authentication |
| Data Sovereignty Lead | Data ownership, compliance |
| Audit Coordinator | Compliance verification |
| Living Seed | Drift detection |

---

### Review Schedule

| Review | Frequency |
|--------|-----------|
| Privacy Framework Review | Annual |
| Product Privacy Audit | Quarterly |
| Third-Party Service Review | Quarterly |
| Compliance Audit | Annual |

---

### Violation Response

**If privacy principles are violated:**

1. **Detection** — Via monitoring, audit, or report
2. **Assessment** — Severity and scope evaluation
3. **Containment** — Immediate mitigation
4. **Notification** — Users informed if affected
5. **Remediation** — Root cause addressed
6. **Documentation** — Incident recorded, lessons learned
7. **Prevention** — Systemic changes to prevent recurrence

---

## Part VII: Public Commitments

### Transparency Report

Published quarterly:
- Data requests from authorities (expect: 0)
- Data breaches (expect: 0)
- Security incidents (full disclosure)
- Privacy improvements made

---

### Privacy Policy (Public)

Plain-language explanation of:
- What we collect
- Why we collect it
- How we protect it
- How users control it
- How to contact us

---

## Quick Reference

```
EVOKE PASSION PRIVACY — QUICK REFERENCE

CORE PRINCIPLES:
├── Local-first — Data stays on device by default
├── Zero-knowledge — We cannot access encrypted data
├── Data sovereignty — Users own their data
├── Minimal collection — Only what's necessary
├── No surveillance — No tracking, no profiling
└── Open source — Auditable, transparent

DATA TIERS:
├── Tier 1 (Sacred): User-encrypted, zero-knowledge
├── Tier 2 (Sovereign): User-controlled, exportable, deletable
├── Tier 3 (Operational): Minimal, anonymized
└── Tier 4 (Forbidden): NEVER collected

COMPLIANCE:
├── GDPR: Full compliance
├── CCPA: Full compliance
├── UK DPA: Full compliance
└── Internal: Exceeds legal requirements

APPLIES TO:
├── Ezri
├── Executive Chef
├── Evoke Passion Website
├── Agent Implementations
├── Community Interactions
├── Partnership Data
└── All Future Products
```

---

*"We evoke—we never extract. This framework ensures we never can, even if we wanted to."*

---

**Version:** 1.0
**License:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
