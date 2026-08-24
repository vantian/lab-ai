# PRODUCT REQUIREMENT DOCUMENT (PRD) — TEMPLATE

> **Purpose:**  
> This PRD defines _what to build_ and _how AI must think while building it_.  
> Sections marked **(LOCKED)** are **non-negotiable** and must not change without explicit approval.

---

## 0. Document Control

- **Product Name:**
- **Version:**
- **Status:** Draft / Approved / Locked
- **Owner:**
- **Target Release:**

---

## 1. Product Overview

### 1.1 Problem Statement

> What problem does this product solve?

```
[Describe the pain point in 2–3 sentences]
```

---

### 1.2 Objectives

> What outcomes are we optimizing for?

- **Primary goal:**
- **Secondary goals:**
- **Non-goals (explicitly out of scope):**

---

### 1.3 Target Users

> Focus on behavior, not demographics. (Role | Frequency of Use | Primary Action)

---

### 1.4 Success Metrics

> How do we know this works?

- **Performance:**
- **Quality:**
- **Adoption / Usability:**

---

## 2. Scope & Milestones

### 2.1 MVP Scope

> What must exist in v1?

- [ ] Core flow implemented
- [ ] Minimal persistence
- [ ] Basic error handling

---

### 2.2 Milestones (Outcome-Based)

| Milestone | Description | Exit Criteria |
| --------- | ----------- | ------------- |
| M1        |             |               |
| M2        |             |               |
| M3        |             |               |

---

## 3. Architecture Constraints **(LOCKED)**

### 3.1 Backend **(LOCKED)**

- **Platform:**
- **Framework & Version:**
- **Architectural Style:**
- **Layering Rules:**
  - API
  - Application
  - Domain
  - Infrastructure
- **Database:**
- **Allowed External Dependencies:**
- **Forbidden Dependencies:**

---

### 3.2 Frontend **(LOCKED)**

- **Framework:**
- **Language:**
- **Architecture Structure:**
  - `domain/`
  - `application/`
  - `infrastructure/`
  - `ui/`
- **Rules:**
  - UI must not call APIs directly
  - DTOs must be mapped to domain entities
  - Use-cases orchestrate logic

---

### 3.3 Cross-Cutting Rules **(LOCKED)**

- **Logging Strategy:**
- **Error Handling Model:**
- **Validation Location:**
- **Timeouts / Retries:**

---

## 4. Functional Requirements

### 4.1 User Stories

```
As a [role]
I want to [action]
So that [outcome]
```

---

### 4.2 Key Features

| Feature | Description | Priority |
| ------- | ----------- | -------- |
|         |             |          |

---

## 5. UI / UX Constraints

### 5.1 Screens

| Screen | Purpose |
| ------ | ------- |
|        |         |

---

### 5.2 UX Rules

- Editable vs derived fields
- Validation timing
- Loading, empty, and error states

---

## 6. API Contract **(LOCKED)**

### 6.1 Endpoints

| Method | Path | Purpose |
| ------ | ---- | ------- |
|        |      |         |

---

### 6.2 Request / Response Samples

```json
{
  "example": "response"
}
```

---

### 6.3 Error Model **(LOCKED)**

```json
{
  "error": {
    "code": "ERROR_CODE",
    "message": "Human-readable message"
  }
}
```

---

## 7. Data Model

### 7.1 Entities

| Entity | Description |
| ------ | ----------- |
|        |             |

---

### 7.2 Data Rules

- **Source of truth:**
- **Mutable vs immutable data:**
- **Retention policy:**

---

## 8. Non-Functional Requirements

### 8.1 Performance

- **SLA:**
- **Max response time:**
- **Concurrency expectations:**

---

### 8.2 Security

- **Authentication:**
- **Authorization:**
- **Sensitive data handling:**
- **SSRF / injection considerations:**

---

### 8.3 Observability

- **Logs:**
- **Metrics:**
- **Tracing:**

---

## 9. Decision Authority **(VERY IMPORTANT)**

### 9.1 AI Can Decide

- Internal refactors
- Code optimization
- Naming (within conventions)

---

### 9.2 AI Must Ask Before

- Adding new services
- Changing architecture
- Introducing new infrastructure or libraries

---

### 9.3 AI Must Never Change

- Locked architecture sections
- API contracts
- Data ownership rules

---

## 10. Open Questions

| Question | Owner | Deadline |
| -------- | ----- | -------- |
|          |       |          |

---

## 11. Reusable Prompt Header

> **Instruction for AI:**  
> Use this PRD as the **single source of truth**.  
> Sections marked **(LOCKED)** are immutable.  
> Do not introduce new frameworks, architectural styles, or services unless explicitly approved.
