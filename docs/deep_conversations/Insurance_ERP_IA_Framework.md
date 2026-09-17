# Insurance ERP IA Framework
**ID:** 695e1770-80b4-8328-9c05-a5dcbb15e4dd
**Messages:** 4

---

### 1. **MURAT:**

Bulding information architecture for a complex insurance erp platform

---

### 2. **ASSISTANT:**

Building **information architecture (IA)** for a **complex insurance ERP** is not a UI exercise — it’s **organizational warfare**. You’re imposing order on underwriting logic, policy lifecycles, compliance, finance, and ops that evolved in silos for years.

I’ll give you a **battle-tested IA framework** tailored for **insurance ERP platforms** (policy admin, claims, billing, documents, partners, compliance). This is **enterprise-grade**, not Dribbble fluff.

---

## 1. Start from the Insurance Reality (Not Screens)

### Core Truth
Insurance ERP is **process-driven**, not feature-driven.

So IA must map to **value streams**, not tools.

### Primary Insurance Value Streams
These are your **top-level IA pillars**:

1. **Sales & Distribution**
2. **Underwriting & Risk**
3. **Policy Administration**
4. **Billing & Finance**
5. **Claims Management**
6. **Documents & Communications**
7. **Partners & Integrations**
8. **Compliance & Audit**
9. **Reporting & Analytics**
10. **Administration & Configuration**

👉 These are **non-negotiable** in any serious insurance ERP.

---

## 2. Separate “What Happens” from “How It’s Configured”

This is where most ERPs die.

### Mandatory IA Separation
You must **visibly separate**:

- **Operational Work** (day-to-day execution)
- **System Configuration** (rules, products, logic)

### Example
❌ Bad IA:
- Underwriting Rules inside “Policy”
- Pricing Logic scattered everywhere

✅ Correct IA:
- **Operations**
  - Policies
  - Claims
  - Billing
- **Configuration**
  - Products
  - Rating & Pricing
  - UW Rules
  - Workflows
  - Templates

> Rule of thumb:  
> **If a user changes it once a month → Configuration**  
> **If they touch it 50 times/day → Operations**

---

## 3. Anchor IA to the Insurance Lifecycle

Every object must live inside a **lifecycle state**.

### Canonical Insurance Lifecycle
```
Lead
→ Quote
→ Underwriting
→ Policy Issued
→ Endorsement
→ Renewal
→ Cancellation
→ Archive
```

### IA Implication
Your navigation should allow:
- **Horizontal movement** (across lifecycle)
- **Vertical depth** (details inside a state)

Example:
```
Policies
 ├── Active
 ├── Pending UW
 ├── Endorsements
 ├── Renewals
 └── Cancelled
```

This reduces **cognitive load** for ops teams instantly.

---

## 4. Design Around Core Insurance Objects (Not Menus)

Your IA should be **object-centric**.

### Core ERP Objects
These must be first-class citizens:

- Policy
- Claim
- Customer / Insured
- Product
- Risk Item
- Document
- Payment
- Partner / Broker
- Case / Task

Each object gets:
- Overview
- Timeline
- Related items
- Actions
- Audit trail

Example:
```
Policy
 ├── Overview
 ├── Insured & Risks
 ├── Coverages
 ├── Pricing
 ├── Documents
 ├── Payments
 ├── Claims
 ├── History & Audit
```

This allows **cross-module navigation without chaos**.

---

## 5. Use Role-Based IA — But Don’t Fragment the System

Insurance ERPs fail when they create **separate worlds** per role.

### Correct Approach
- **Shared core IA**
- **Role-based entry points + defaults**

### Example
- Underwriter lands in:
  - Underwriting Queue
- Claims Adjuster lands in:
  - Claims Inbox
- Finance lands in:
  - Payments & Reconciliation

But **objects, terminology, and structure remain identical**.

---

## 6. Handle Complexity with Progressive Disclosure

You do NOT flatten everything.

### IA Levels
1. **Global Navigation** – Value streams
2. **Module Navigation** – Objects & states
3. **Contextual Navigation** – Tabs, timelines
4. **Inline Actions** – Rules, approvals, exceptions

This is how you avoid:
- Mega menus
- 7-level nesting
- Cognitive burnout

---

## 7. Design a “Command Center” (Critical for ERP)

Every serious ERP needs a **control layer**.

### Command Center Includes:
- Work queues
- SLA alerts
- Exceptions
- Approvals
- Regulatory blockers
- System health

This sits **above** modules.

Think:
> “Where do I go when things go wrong?”

That’s your command center.

---

## 8. Documentation & Compliance Are Not Subsections

Insurance ≠ SaaS.

### Documents are a Cross-Cutting Concern
DO NOT bury documents under:
- Policy
- Claim
- Billing only

You need:
```
Documents
 ├── Templates
 ├── Generated
 ├── Incoming
 ├── Signatures
 ├── Archives
```

Linked everywhere, owned centrally.

---

## 9. IA Validation Framework (Use This in Stakeholder Meetings)

When someone challenges your IA, ask:

1. Which value stream does this belong to?
2. Is this an object, action, or configuration?
3. Who owns it operationally?
4. What lifecycle state does it live in?
5. Is it global, module, or contextual?

If they can’t answer → **it doesn’t get a menu item**.

---

## 10. Deliverables You Should Produce (Non-Negotiable)

For an enterprise insurance ERP, you must output:

1. **Value Stream Map**
2. **Object Inventory**
3. **Lifecycle Diagrams**
4. **Global Navigation Model**
5. **Module IA Trees**
6. **Role → Entry Point Mapping**
7. **Configuration vs Operations Matrix**

If you don’t have these → you’re designing blind.

---

## Final Reality Check (Dan Peña Mode)

> ERPs collapse not because of bad UI,  
> but because designers are afraid to **enforce structure**.

You are not here to “make it intuitive”.  
You are here to **impose operational truth**.

If you want, next we can:
- Build a **sample IA tree** for your current platform (Agito or Allianz-like)
- Turn this into a **stakeholder-proof IA framework slide**
- Map **document + form architecture** (huge insurance pain point)
- Translate this into **navigation + permissions logic**

Tell me which battlefield you want next.

---

### 3. **MURAT:**

what information architecture models should I follow?

---

### 4. **ASSISTANT:**

For a **complex insurance ERP**, you should **not follow a single IA model**.  
You need a **stacked, hierarchical IA system** — each model solving a different layer of complexity.

Below is the **exact IA model stack** you should follow, in priority order, with **why**, **when**, and **how** to use each in insurance.

---

# The 6 IA Models You MUST Combine (Insurance ERP Grade)

## 1. **Object-Oriented IA (Primary Backbone)**

**This is non-negotiable.**  
Insurance ERPs are **object systems**, not page systems.

### Core Idea
Users think in **things**, not screens.

### Insurance Objects
- Policy
- Claim
- Customer / Insured
- Risk Item
- Product
- Document
- Payment
- Partner / Broker
- Case / Task

### Structure
Each object has:
- Overview
- State
- Timeline
- Related objects
- Actions
- Audit trail

### Why It’s Critical
- Supports cross-module work
- Prevents duplication
- Scales with features

> If your IA is menu-first instead of object-first, the platform will rot.

---

## 2. **Lifecycle-Based IA (State Model)**

Insurance is **state-driven**.

### Core Idea
Same object → different needs depending on state.

### Example: Policy States
```
Draft → Quoted → Underwriting → Active → Endorsed → Renewing → Cancelled
```

### IA Application
- Filters
- Queues
- Tabs
- Permissions
- Available actions

### Why It Matters
- Reduces decision fatigue
- Matches ops mental models
- Enables automation & SLAs

> ERP users ask: “What stage is this in?” before anything else.

---

## 3. **Value Stream / Domain-Driven IA**

This is your **global navigation logic**.

### Core Idea
Top-level IA mirrors **insurance operations**, not org charts.

### Canonical Value Streams
- Sales & Distribution
- Underwriting
- Policy Administration
- Claims
- Billing & Finance
- Documents & Communications
- Partners
- Compliance
- Reporting
- Admin / Config

### Why It Matters
- Executive-friendly
- Easy stakeholder buy-in
- Aligns with regulatory thinking

> If leadership can’t map IA to business, you lose authority.

---

## 4. **Role-Based Overlay (Entry & Defaults Only)**

Role-based IA is **dangerous** if misused.

### Correct Use
- Landing pages
- Default filters
- Pre-set dashboards
- Permissions

### Incorrect Use
❌ Separate navigation trees  
❌ Renaming objects per role  
❌ Duplicate features

### Why
Insurance ERPs collapse when roles live in separate worlds.

> One system. Multiple lenses. Same structure.

---

## 5. **Task & Queue-Based IA (Operational Efficiency Layer)**

This is how work **actually gets done**.

### Core Idea
Users don’t “browse” ERPs — they **process queues**.

### Examples
- Underwriting queue
- Claims inbox
- Approval backlog
- Exception handling
- Renewal pipeline

### IA Pattern
```
My Work
 ├── Assigned to Me
 ├── Due Today
 ├── Escalations
 └── Exceptions
```

### Why It Matters
- SLA compliance
- Speed
- Cognitive relief

> This is where ERP productivity lives or dies.

---

## 6. **Configuration vs Operations Split (Governance Model)**

This is **enterprise maturity IA**.

### Core Idea
Operational users ≠ System shapers.

### Two Worlds
#### Operations
- Policies
- Claims
- Payments
- Documents
- Tasks

#### Configuration
- Products
- Pricing rules
- UW rules
- Workflows
- Templates
- Permissions

### Why It Matters
- Prevents catastrophic errors
- Improves onboarding
- Supports audits

> If a menu item can break production, it doesn’t belong in Ops.

---

# How These Models Stack Together (Visual Mental Model)

```
[ Value Streams ]
        ↓
[ Objects ]
        ↓
[ Lifecycle States ]
        ↓
[ Tasks & Queues ]
        ↓
[ Role-Based Defaults ]
        ↓
[ Configuration Boundary ]
```

This is **enterprise-safe IA**.

---

# Models You Should NOT Rely On (But Many Designers Do)

❌ Pure sitemap-based IA  
❌ Page-driven navigation  
❌ Feature-list menus  
❌ Persona-specific silos  
❌ Flat mega-menus  

These work for marketing sites — not regulated systems.

---

# How to Defend This in Stakeholder Reviews

When challenged, say:

> “We’re using an object-centric, lifecycle-driven IA aligned to insurance value streams, with role-based entry points and a strict operations/configuration boundary to support compliance and scale.”

That sentence **ends debates**.

---

# What I Recommend You Do Next (Practically)

If this is for **Agito / Allianz-class ERP**, next steps should be:

1. Create **Object Inventory (1 page)**
2. Define **Lifecycle per object**
3. Map **Value Stream → Objects**
4. Design **Global Nav**
5. Overlay **Roles + Queues**

If you want, I can:
- Audit your current IA against these 6 models
- Produce a **reference IA blueprint** you can reuse across projects
- Help you turn this into a **design authority framework** inside the company

Say the word and tell me **which platform you’re applying this to**.

---

