---
name: dri-team-execution-standards
description: DRi compliance and execution standards for Project Leads (PLs) and Developers (DEVs). Use whenever a PL or DEV needs to know SLA response/resolution times, escalation rules (L1-L4 and 1-3-1), decision authority (decide-alone vs escalate-to-PJ), Jira routing (which project to which PL/DEV), the mandatory Jira task template, parent Story/Epic assignment rules, priority-to-SLA mapping, accolade standing rule, or how to add a Call Report. Also triggers when team members ask "do I need to escalate this?", "what's my SLA on this priority?", "who's PL on this project?", "should this be a Story or a Task?", or any compliance question relating to internal DRi standards.
---

# DRi Team Execution Standards

This skill equips every Project Lead (PL) and Developer (DEV) at DRi to execute to PJ's standards without needing PJ in the loop. **PJ should only see commercial decisions, scope changes, and 1-3-1 escalations.** Everything else lives here.

If you're a PL or DEV and you're unsure whether something needs PJ — **read this first, decide using the framework, act, document**. Only escalate after the 1-3-1 self-check below.

---

## 1. Priority and SLA Table — mandatory on every task

Every Jira issue carries a priority. Priority determines SLA. **There is no "I'll get to it" — the SLA is the contract.**

| Priority | Response SLA (business hours) | Resolution SLA (work days, excludes weekends) |
|----------|-------------------------------|------------------------------------------------|
| Highest  | 2 hours                       | 3 work days                                    |
| High     | 4 hours (same business day)   | 5 work days                                    |
| Medium   | 1 work day                    | 7 work days                                    |
| Low      | 2 work days                   | 14 work days                                   |

**Response = acknowledge + first action taken + client notified (if external).**
**Resolution = fully closed, verified, client confirmed.**

Resolution due date is calculated from task creation date. Weekends excluded.

### Priority = SLA expectation, not topic importance

Set priority based on **how fast a response is needed**, not on how serious the topic feels. A delivery-tracking task on an overdue order is Medium because a shipment update needs a 1-day response, not because biltong is important. A LinkedIn comment is not Highest because PJ likes the contact.

**Common mistakes:**
- Setting personal items to Low because they "feel less important" — wrong. If the task carries a real active deadline, it's Medium minimum. Low is for true monitor-only or speculative work.
- Setting client items to Highest just because the client is big — wrong. Highest is reserved for revenue/exec-decision/legal-exposure items that need PJ inside 2 hours.

---

## 2. The L1 PASS/FAIL conformance check

Every morning, the L1 check fires at the time the task hits its response SLA. If the check fails, escalation begins.

**Internal task — PASS:**
- Status moved to **In Progress**, AND
- Assignee has added a **Jira comment** documenting first action.

**Client-facing task — PASS:**
- Status moved to **In Progress**, AND
- Assignee has added a **Jira comment**, AND
- **Client acknowledgment sent** (email, Teams, or WhatsApp client group) AND logged as a comment on the task.

**FAIL:** either condition not met within the response SLA window.

If you're a DEV and you don't move status + comment within your SLA, you breach L1 automatically. **No grace period.**

---

## 3. Escalation Ladder — L1 → L2 → L3 → L4

For Highest tasks (and any breach), escalation follows this exact path:

- **L1 — DEV.** Acknowledge + first action + client notification within 2 hours (Highest) or matching SLA for other priorities.
- **L2 — Claude flags PL.** If L1 breached, the morning routine adds a Jira comment tagging the PL. PL must unblock, reassign, or resolve.
- **L3 — Morning brief flags PL accountability.** If no Jira update within 24 hours of L2, the morning brief surfaces this as a **PL ACCOUNTABILITY BREACH**. Format: `task key | PL name | hours since creation`. Recommended action: PL to resolve. PJ does NOT action task-level issues.
- **L4 — PJ enters only** when the task crosses into a commercial decision, client relationship risk, or scope change. These are Tier 1 by definition and PJ already owns them.

**PJ sees PL accountability issues, never task-level execution.** Escalating execution problems to PJ is itself a failure of the L1-L3 ladder.

---

## 4. The 1-3-1 Rule — mandatory before any PJ escalation

Any escalation that reaches PJ must arrive in this exact format:

- **1 problem** (one sentence — what's broken or what decision is needed)
- **3 options** (three viable paths forward, each with cost/benefit/risk)
- **1 recommendation** (which option you'd take and why)

If it doesn't have all three components — **return to sender**. Do NOT pass it to PJ.

This isn't optional. It's the price of PJ's attention.

---

## 5. PL Decision Authority — decide alone vs escalate

### PL decides alone — no PJ required

**Commercial:**
- Client status updates, timeline adjustments within buffer, Highest-task client acknowledgments, operational scope clarifications already implied by contract.

**Financial:**
- Any spend within approved project budget **under R10,000**.
- Overtime **up to 4 hours**.

**Client comms:**
- Delivery updates, scheduling, operational queries, issue acknowledgments.

**Scope:**
- Variations **up to 8 hours** within existing spec.

**Resource:**
- Task reassignment within the DEV team, priority reordering within the project.

**Technical:**
- Solution approach, bug fixes, infrastructure changes within approved scope.

### Must escalate to PJ via 1-3-1

**Commercial:**
- Pricing, new scope, contract terms, discounts, any new client commitment.

**Financial:**
- Any spend **above R10,000**.
- Any unbudgeted spend regardless of amount.
- Overtime **beyond 4 hours**.

**Client comms:**
- Any communication creating a new commercial expectation or commitment.

**Scope:**
- **Beyond 8 hours** additional effort. Any new feature or deliverable not in the original spec.

**Resource:**
- New external resource, changing PL, anything affecting billing.

**Technical:**
- Architecture affecting multiple clients, new vendor selection, security policy changes.

---

## 6. Jira Routing Table — who is PL, who is DEV

| Key   | Project                       | PL (delivery owner) | DEV (assignee) |
|-------|-------------------------------|---------------------|----------------|
| AG01  | Adhive Group                  | Arushke             | Franro         |
| AN    | Autolectron                   | Elaine              | Franro         |
| BL    | BULLAS v2                     | Arushke             | Alex           |
| BOER  | BOERnet                       | Maritz (BD + PD/POCs) | Alex         |
| BSM01 | Brakesafe Mining              | Elaine              | Alex           |
| BD    | Business Development          | PJ + David          | Elaine (call reports/scheduling) |
| EC01  | ENPROTEC Bultfontein          | Arushke             | Alex           |
| EC02  | ENPROTEC Makhado              | Arushke             | Alex           |
| EDM   | Environmental Dust Mgmt       | David               | Franro         |
| EI01  | Eickhoff                      | Arushke             | Franro         |
| IT    | Internal IT                   | Franro              | —              |
| KN    | Kilken                        | Arushke             | Franro         |
| KZ01  | Kropz Elandsfontein           | Arushke             | Alex           |
| MAR   | Marketing                     | Marisel             | —              |
| ME    | Maize Quality & Logistics     | Elaine              | Franro         |
| MI    | Management — Internal         | David               | —              |
| MK01  | Minopex Kroondal K2           | Arushke             | Alex           |
| MWB   | MineWaterBalances             | Arushke             | Alex           |
| PD    | Product Development           | PJ (general DRi PD) | Alex           |
| PP    | ProProcess Projects           | Elaine              | Franro         |
| PS    | People Support                | Marisel             | —              |
| ST    | SOP's Training                | Elaine              | —              |
| SUP   | Support                       | DEPRECATED — route to client project |  |
| TLA   | Task Loading & Actioning      | PJ + Marisel only   | —              |
| VA    | Vendor Applications           | David               | —              |

**SUP deprecation:** All support and IT tickets route directly to the relevant client project. Assign to DEV (Franro = IT/infrastructure, Alex = app/software/dev). Mention the PL in the task description.

---

## 7. The mandatory Jira Task Template

Every new task description **must** follow this structure. No exceptions.

```
CONTEXT: [brief description of issue and why it matters]

ACTIONS REQUIRED:
1. [step]
2. [step]
...

CLIENT ACKNOWLEDGMENT (client-facing tasks only — send within response SLA):
Channel: Email / Teams / WhatsApp client group — log channel used as a comment.
---
Hi [Client name],
We are aware of [issue]. [PL name] is on it.
We will have a status update for you by [task creation time + response SLA + 4 hours].
Kind regards, [PL name]
---

CALL REPORT: Add as a comment on this task upon resolution.
Confirm: issue resolved | client notified | root cause documented.

SLA: Response by [datetime SAST] | Resolution by [datetime SAST]
ESCALATION: No update within 24hrs → PL flagged in morning brief.
PL: [name] — delivery accountable.
```

**The Call Report is the closing comment.** A task is not Done until its Call Report comment exists.

---

## 7a. How to create a task in Jira using this standard

You (PL or DEV) have a Jira MCP connector on your Claude. To create a compliant task, do not free-form the description — apply this workflow.

### Step 1 — Gather the 7 mandatory inputs

Before calling any tool, have these ready:

1. **Project key** (Section 6 routing table — e.g. BL, KN, BD)
2. **Issue type** — `Task` for a single deliverable, `Story` only if you'll add subtasks, `Bug` only for defects, `Subtask` only if creating under a parent
3. **Summary** — format: `[PL initials] | [PRIORITY] | [Short verb-led description]` (e.g., `AGB | HIGH | Send VuWall follow-up brief`)
4. **Priority** — Highest / High / Medium / Low per Section 1
5. **Assignee (DEV)** — Section 6 routing. **For container Stories/Epics with subtasks → leave assignee empty (Section 8).**
6. **Due date** — derive from priority + creation date (Section 1 resolution SLA), exclude weekends
7. **Client name (if client-facing)** — needed for the Client Acknowledgment block

### Step 2 — Build the description per Section 7 template

Paste the Section 7 template, fill in CONTEXT / ACTIONS REQUIRED / CLIENT ACK (if applicable) / SLA / ESCALATION / PL. Do not skip sections. If a section doesn't apply, write "N/A — [reason]" rather than deleting it.

### Step 3 — Call the connector

For most cases, this is one tool call. Pseudo-format (your Claude will fill in the actual parameters):

```
createJiraIssue(
  projectKey: "<KEY>",
  issueTypeName: "<Task|Story|Bug|Subtask>",
  summary: "<formatted summary>",
  description: "<filled Section 7 template>",
  assignee_account_id: "<DEV account ID OR empty if container>",
  additional_fields: {
    priority: { name: "<Highest|High|Medium|Low>" },
    duedate: "<YYYY-MM-DD>"
  }
)
```

### Step 4 — Verify with a follow-up read

Don't trust the create response. Run a `getJiraIssue` with `fields: ["assignee", "duedate", "priority", "status"]` to confirm what landed. If anything is wrong, fix with `editJiraIssue` before moving on.

### Step 5 — Post the opening comment

Add an opening Jira comment via `addCommentToJiraIssue`:

```
**Routing:** PL = [name], DEV = [name].
**SLA:** Response by [datetime SAST] | Resolution by [datetime SAST].
**Escalation:** No update within 24hrs → L2 (PL flagged in morning brief).
[Any additional context, links, or instructions for the assignee.]
```

This comment satisfies the L1 conformance requirement that the task has an owner-documented first action visible in the comment thread.

### Step 6 — If client-facing, send the Client Acknowledgment

Use the template from Section 7. Send via email / Teams / WhatsApp client group. Log the channel used as a follow-up Jira comment: `Client ack sent via [channel] at [time SAST]`. Without this, the L1 PASS/FAIL check (Section 2) fails on a client-facing task even with status In Progress.

### Common creation pitfalls — don't repeat these

- **Skipping the priority field.** Default is "Medium" if you don't set it. Don't accept default — choose deliberately per Section 1.
- **Setting assignee on a container Story/Epic.** Stop. Section 8.
- **Setting priority on a container Story/Epic.** Same — leave neutral, priorities live on subtasks.
- **Free-form description.** No. Use Section 7 template every time, even for "small" tasks. The template is the contract.
- **Forgetting `additional_fields` for priority.** Many Jira MCP wrappers require priority via `additional_fields: { priority: { name: "..." } }`, not as a top-level parameter. Test the connector once if unsure.
- **Creating a Task when you mean a Story.** If you're going to break it into subtasks, create Story. If you've created a Task and now need subtasks, convert it — don't stack subtasks under a Task.

### Worked example — minimum compliant create

A PL needs to track a client deliverable. From the routing table, project is BL (BULLAS v2), PL is Arushke, DEV is Alex. Priority Medium. Due in 5 work days.

```
createJiraIssue(
  projectKey: "BL",
  issueTypeName: "Task",
  summary: "AGB | MEDIUM | Confirm BULLAS biltong shipment received",
  description: "[Section 7 template, filled]",
  assignee_account_id: "<Alex's account ID>",
  additional_fields: {
    priority: { name: "Medium" },
    duedate: "2026-05-20"
  }
)
```

Then `getJiraIssue` to verify. Then `addCommentToJiraIssue` with the opening comment. Done — three tool calls, fully compliant task.

---

## 8. The Parent Story / Epic Rule — assignment hygiene

**Story or Epic WITH ≥1 subtask:**
- **Never** assign at the parent level.
- **Never** set a due date at the parent level.
- **Never** set a priority field at the parent level (or leave it neutral).
- Assignee, due date, and priority **live on the subtasks**. The parent is a container.
- Examples that should remain unassigned at parent level: BD-55, BD-453, BD-427, BD-513, MAR-235, AN-168, TLA-198.

**Story or Epic WITHOUT subtasks:**
- Treat as a regular task. Assignee, due date, and priority required.

**Subtask, Task, Bug:**
- Always regular tasks. Assignee, due date, priority all required.

**How to check:** look at `issuetype.name` and the `subtasks` array. If type is Story or Epic AND `subtasks.length > 0` → it's a container. Hands off the parent fields.

PL ownership on container Stories/Epics lives in **comments**, not in the assignee field.

---

## 9. Accolade Standing Rule

All ACCOLADE-class tasks (LinkedIn likes, WhatsApp thank-yous, U-ROCK nominations, team recognition posts, LinkedIn comment replies) route to **Marisel** as standing rule.

**Workflow (draft + approve):**
1. Marisel drafts the response/post in PJ's voice — short sentences, direct, Afrikaans where natural, emojis 🙏🏼🤩 sparingly.
2. Marisel posts a single batch of drafts (max once per day) into the relevant task as a comment.
3. PJ approves with "✅" or sends edits in one pass.
4. Marisel publishes, adds Call Report comment, closes the task.

**Escalate via 1-3-1 only if** the accolade touches a commercial relationship or external client.

---

## 10. Client Account Register — PJ owns these accounts commercially

Any BD, commercial, relationship, or strategic communication on any of these accounts is **Tier 1** and reaches PJ:

Sibanye, Anglo American, ProProcess, DDS, Miko, Ukwazi, Sasol, Optimum, Lake Agri, Northam Platinum, Mogale City, Effective Lab, Quiver, MWB, Ditstek.

**Tier 2 (operational/delivery on the same accounts)** is delegated to the PL per the routing table, with PJ informed via morning brief, not by direct routing.

**BD email alias:** CC `1811bd75.digirockinnovations.com@za.teams.ms` on all BD-account emails.

---

## 11. CEO Advisor Lens — when does something reach PJ?

PJ's Buyback Rate (BBR) is **R605/hour**. For every Tier 1 item, ask:

1. **Should PJ be involved at all?** If a PL or DEV can decide it within their authority (Section 5), they decide it. End of conversation.
2. **What is the minimum effective involvement?** If PJ does need to weigh in, what's the shortest path — a 30-second ✅ on an approval, a 5-minute review, or a 15-minute decision call?
3. **What's the cost of his involvement?** Name the BBR cost on sub-R605 tasks. "PJ replying to a LinkedIn thank-you = R605 × 0.05 hr = R30 of his time for a R0 outcome." That's the trigger to delegate.

**The lens applies to deciding whether something reaches PJ.** Once delegated, the team takes it seriously per Section 1 — personal items get the same SLA standard as client items.

---

## 12. Team KRA Reference — know what your owner cares about

| Team member | Primary KRAs (percentages) |
|-------------|----------------------------|
| Franro      | IT Infrastructure Availability 50% / Development Delivery 30% / CI&A 20% |
| Alex        | Development Delivery 60% / System Stability & Monitoring 10% / CI&A 30% |
| Arushke     | Project Delivery & Execution 60% / BD Contribution 20% / Marketing & Social 20% |
| David       | Project Delivery & Execution 40% / Operational Efficiency & Financial Control 30% / BD Contribution 30% |
| Elaine      | Marketing/Campaigns/Branding · Scheduling/Coordination · Call Reports · SOP formatting |
| Marisel     | Executive Support & DRi Management 60% / BD Contribution 20% / Marketing & Social 20% |
| Maritz      | BD BOERnet 50% / BD DRi 30% / Product Dev & POCs 20% (BOERnet PD/POCs only) |
| PJ          | Revenue Growth & Commercial Performance 65% / Strategic Partnerships 20% / Product & Solution Development 15% |

When you reassign work, route to whoever's KRA matches the task type. A PD task to someone whose KRA is BD is a misroute — fix it before it ages.

---

## 13. Self-check before any PJ escalation

Run this checklist. If you can't tick every box, do NOT send to PJ.

- [ ] Have I checked Section 5 to confirm this is outside my authority?
- [ ] Have I documented my attempt to resolve at L1 (status + comment + client ack if applicable)?
- [ ] Have I tagged the PL via L2 if I'm a DEV with a blocker?
- [ ] Is this Tier 1 by definition (commercial decision, client relationship risk, scope change)?
- [ ] Do I have **1 problem + 3 options + 1 recommendation** ready in writing?
- [ ] Have I named the BBR cost of PJ's involvement vs. an alternative path?
- [ ] If I'm sending an accolade or sub-R605 item to PJ — STOP. Route to Marisel via Section 9.

---

## 14. Common mistakes and the lessons log

These are real corrections from PJ. Don't repeat them.

**Mistake:** Setting personal/internal items to Low priority because they "feel less important."
**Correction:** Priority = SLA expectation. A delivery-tracking task with a real active deadline is Medium minimum. Low is for true monitor-only work. (BL-80 lesson, 2026-05-13.)

**Mistake:** Assigning a container Story or Epic at the parent level.
**Correction:** Stories/Epics with subtasks never get an assignee, due date, or priority at parent level. PL ownership lives in comments. (BD-513 lesson, 2026-05-13.)

**Mistake:** Sending sub-R605 work (accolades, LinkedIn likes, venue booking, biltong tracking) to PJ for action.
**Correction:** Use the routing table. PJ does not pick venues, send thank-yous, or track parcel deliveries. Marisel routes accolades; PLs route operational items per the table.

**Mistake:** Escalating to PJ without a 1-3-1.
**Correction:** Return to sender. No exceptions. (1-3-1 rule, Section 4.)

**Mistake:** Closing a task without a Call Report comment.
**Correction:** A task is not Done until its Call Report exists. Status = Done + no Call Report = the task gets reopened.

**Mistake:** Treating "Done" status as "everything handled."
**Correction:** Add the Call Report comment confirming: issue resolved | client notified | root cause documented. If client notification is missing on a client-facing task, you have failed L1 even if status is Done.

---

## 15. Quick reference — read this when in doubt

**"Am I allowed to decide this?"** → Section 5.
**"What's my SLA?"** → Section 1.
**"Do I need to escalate?"** → Section 13 self-check.
**"Which project?"** → Section 6 routing table.
**"How do I write the task?"** → Section 7 template.
**"Story or Task?"** → Section 8.
**"Is this PJ work or not?"** → Section 11 CEO Advisor Lens.

When in true doubt, default to: **act within authority, document in Jira comments, surface to your PL — not to PJ**.

---

*Version: 1.1 — 2026-05-13. Source of truth lives at `~/Documents/Claude/Scheduled/dri-team-execution-standards/SKILL.md` on PJ's workstation. Updates flow through this file; team Claude instances reload it daily.*

*Changelog:*
- *v1.1 — Added Section 7a (concrete Jira creation workflow with tool-call pseudo-format).*
- *v1.0 — Initial release.*
