# 02 - Stakeholder Analysis & Personas

## 1. Overview & Stakeholder Taxonomy

CareerSimplify operates primarily as a **direct-to-consumer (B2C)** career preparation, upskilling, and experiential internship platform in its initial phase, with built-in architectural flexibility to scale toward **B2B (Academic Partnerships & Corporate Hiring)** in subsequent phases.

```text
                               CareerSimplify Ecosystem
                                          │
            ┌─────────────────────────────┼─────────────────────────────┐
            ▼                             ▼                             ▼
       Learners                      Instructors                     Admin
   (B2C Core Users)            (Phased Growth Model)          (Operations & Growth)
   • Tier-2/3 Students         • Phase 1: Internal Team       • Content & Cohort Ops
   • Final/Pre-Final Years     • Phase 2: Vetted Mentors      • Certificate Issuance
   • Fresh Graduates           • Phase 3: Open Marketplace    • Analytics & Support
            │                             │                             │
            └─────────────────────────────┼─────────────────────────────┘
                                          ▼
                         Future Expansion Stakeholders
                        • External Employers & Recruiters
                        • College Placement Cells & TPOs (B2B)
```

---

## 2. Detailed Stakeholder Profiles

### 2.1 Primary User: The Learner / Student (Demand Side)

| Attribute | Profile Details |
| :--- | :--- |
| **User Archetypes** | • Engineering / CS undergraduates (2nd to 4th year)<br>• Tier-2 and Tier-3 college students with limited campus placements<br>• Fresh graduates seeking their first software/tech employment<br>• Career switchers & early-career upskillers |
| **Primary Goals** | • Acquire in-demand technical competencies without resource hunting.<br>• Gain verified practical experience via structured workshops & internships.<br>• Earn verifiable certificates recognized by recruiters.<br>• Achieve job readiness and placement confidence. |
| **Core Platform Needs** | • Seamless course enrollment and structured video/text lesson playback.<br>• Workshop & Internship cohort registration (e.g., Winter Internship).<br>• Assignment/project submission portals with status tracking.<br>• Automated, tamper-proof certificate generation & verification.<br>• Accessible on both Web and Mobile (Android / iOS). |
| **Pain Points** | • Cognitive overload from fragmented YouTube/Udemy courses.<br>• Lack of real-world project experience to put on a resume.<br>• Skepticism around paid programs that provide certificates without practical skills. |

---

### 2.2 Content Creator: Instructors & Mentors (Supply Side)

CareerSimplify recognizes that as an early-stage startup, its instructor model must scale through three distinct evolution tiers:

```text
   Phase 1 (Current)                Phase 2 (Growth)                Phase 3 (Scale)
┌───────────────────────┐       ┌───────────────────────┐       ┌───────────────────────┐
│ Internal Core Team    │  ──►  │ Vetted Industry       │  ──►  │ Open Instructor       │
│ & Employees           │       │ Mentors (Curated)     │       │ Marketplace (Rev-Share)│
└───────────────────────┘       └───────────────────────┘       └───────────────────────┘
```

| Phase | Description & Responsibilities |
| :--- | :--- |
| **Phase 1: Internal Core Team** *(Current)* | CareerSimplify founders and internal technical staff author curricula, record courses, conduct live bootcamps, and evaluate student project submissions. |
| **Phase 2: Vetted Industry Mentors** | Invited senior software engineers and domain specialists who lead weekend workshops, guest cohorts, and code-review mentorship sessions. |
| **Phase 3: Open Marketplace** | Scaled model where approved creators can publish courses, host certified cohorts, and receive automated payout distributions. |

**Platform Capabilities Needed for Instructors**:
- Course and module management (video, notes, quizzes).
- Live session scheduling and attendance tracking.
- Project grading, rubric evaluation, and feedback mechanisms.
- Payout tracking and performance analytics (Phases 2 & 3).

---

### 2.3 Experience & Employment Enablers: Internship Providers & Employers

| Horizon | Operating Model |
| :--- | :--- |
| **Phase 1: In-House Experiential Programs** *(Current)* | **CareerSimplify directly designs, operates, and certifies internships** (e.g., 1-week to 4-week Winter/Summer Internships). Learners work on real-world simulated client products, commit code to GitHub, and receive formal evaluation and certificates from CareerSimplify. |
| **Phase 2: Partner Hiring Pipelines** | Corporate partners and startups review portfolios of top-performing CareerSimplify graduates for direct off-campus interview shortlisting. |
| **Phase 3: Direct Employer Portal** | Companies post openings, review verified student skill scores and project repositories, and extend interview invites directly through the platform. |

**What Employers Value**:
- **Proof of Work**: Publicly accessible project repositories and live deployment URLs.
- **Vetted Competence**: Filtered candidates who have cleared milestone assessments rather than inflated resumes.
- **Reduced Time-to-Hire**: Pre-assessed candidates requiring zero on-the-job fundamental training.

---

### 2.4 Internal Operator: Platform Administrator

The CareerSimplify operations and business leadership team responsible for maintaining platform health and user trust.

| Responsibility Area | Specific Operational Tasks |
| :--- | :--- |
| **User & Access Management** | Managing student, instructor, and staff roles; resolving account issues. |
| **Content Moderation & Publishing** | Reviewing course materials, workshop schedules, and resource attachments. |
| **Cohort & Internship Operations** | Setting batch schedules, managing enrollment caps, and tracking student milestone progress. |
| **Certification Governance** | Issuing, revoking, and digitally verifying credential authenticity via unique IDs/QR codes. |
| **Financial & Payment Operations** | Tracking revenue, payment gateway transactions, refund processing, and pricing tiers. |
| **Analytics & Business Intelligence** | Monitoring platform engagement, drop-off rates, placement rates, and active learners. |

---

### 2.5 Future Expansion: Academic Institutions & Placement Cells (B2B)

While the initial focus is strictly **B2C**, the platform architecture will support institutional onboarding in future development phases:

- **Target Persona**: College Training & Placement Officers (TPOs), Department Heads, and Deans.
- **Value Proposition**: Enhancing college placement statistics through plug-and-play industry-aligned upskilling and certified internships for entire student batches.
- **Future Capabilities**: Batch enrollment, institutional dashboards, attendance tracking, and student performance reports.

---

## 3. Stakeholder RACI Matrix

| Functional Area | Learner | Instructor | Admin | Future Employers |
| :--- | :---: | :---: | :---: | :---: |
| **Course Discovery & Enrollment** | **R** | I | **A** | I |
| **Curriculum Creation & Publishing** | I | **R** | **A** | C |
| **Internship / Workshop Delivery** | C | **R** | **A** | I |
| **Assignment & Project Submission** | **R** | C | **A** | I |
| **Project Review & Grading** | I | **R** | **A** | I |
| **Certificate Generation & Verification** | I | C | **A / R** | C |
| **Candidate Shortlisting & Hiring** | C | I | C | **R / A** |
| **Platform Maintenance & Policy** | I | I | **R / A** | I |

*Legend: **R** = Responsible, **A** = Accountable, **C** = Consulted, **I** = Informed*

---

## 4. Key Value Drivers by Stakeholder

- **For Learners**: Clarity of roadmap, practical real-world project skills, verified credentials, and career readiness.
- **For Instructors**: Efficient teaching tools, engaged student cohorts, and monetization channels.
- **For CareerSimplify Operations**: Scalable cohort management, automated certificate delivery, low support overhead, and data-driven insights.
- **For Future Hiring Partners**: Reliable, pre-screened talent pipeline possessing demonstrable engineering capabilities.
