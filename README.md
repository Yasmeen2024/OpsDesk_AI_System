# OpsDesk - Controlled AI Engineering System (Day 3 Evaluation)

## 1. AI Tool Fit Matrix
| Task ID | Engineering Task | AI Tool Pattern | Why this pattern? |
| :--- | :--- | :--- | :--- |
| **KAN-9** | Setup DB Schema | Repo-investigation Agent | To analyze business rules and draft schema concepts prior to generating code. |
| **KAN-11** | Create Ticket API | Editor-native (Cursor) | Ideal for rapid, context-aware routing logic and endpoint development directly within the repo. |
| **KAN-10** | Auth Implementation | Review/Automation Support | To audit security dependencies and look for common authentication vulnerabilities before committing. |

---

## 2. Context, Access, and Risk Plan
* **Task Focused:** `KAN-9` (Local Database Prototyping)
* **Access Scope:** Scoped strictly to Local Workspace Files & Isolated Local Docker Container. No broad terminal `sudo` or Cloud network access was provided to the AI.
* **Risk Identified:** Potential for hardcoding real credentials or leaking database layout structures.
* **Control Implemented:** Enabled Cursor Privacy Mode to protect data. Used separate `.env.example` configurations to block actual database passwords from entering the codebase history.

---

## 3. AI-Assisted Coding Workflow (Plan-First)
1. **Task Definition:** Define relational PostgreSQL schema for IT ticket registration.
2. **Context Provided:** Checked local `requirements.md` and `backlog.md` via `@Codebase`.
3. **AI Plan Approval:** Reviewed structural tables and fields proposed by Cursor before accepting any SQL DDL generation.
4. **Diff Inspection:** Checked the generated `migrations/001_create_ticket.sql` file to confirm constraints, singular naming convention (`ticket`), and default automatic sequence assignments.

---

## 4. Debugging & Verification Evidence
* **The Block:** Task `KAN-9` was blocked due to missing cloud server credentials.
* **Engineering Action:** Bypassed the cloud delay using **Engineering Judgment** to stand up an identical PostgreSQL environment locally with Docker Compose.
* **Verification Logic:** Built a native Python check `scripts/verify_ticket_schema.py` that connects to the instance, fires dummy rows, validates UUID auto-generation, confirms incremental sequence counters, and safely rolls back transaction data.
* **Output Log Evidence:**
```text
[PASS] Connected, inserted two dummy rows in one transaction (rolled back).
       ticket_number sequence: <n> then <n+1> (increment verified).
       created_at (first row): <timestamp> (auto-generated, recent).
       id (first row): <uuid>