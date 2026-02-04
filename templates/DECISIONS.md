# Decision Log

> **Purpose:** Record architectural and technical decisions for future reference.
> **When:** Log decisions on architecture, tech stack, major patterns, or significant trade-offs.

---

## Decisions

<!-- Newest decision at top -->

### [YYYY-MM-DD] - [Decision Title]

**Context:** [Why this decision was needed]

**Options Considered:**
| Option | Pros | Cons |
|--------|------|------|
| A | [Pros] | [Cons] |
| B | [Pros] | [Cons] |

**Decision:** [What was chosen]

**Rationale:** [Why this option was selected]

**Decided By:** [Human name] with AI input

---

### [Example] - Database Selection

**Context:** Need a database for user data and transactions.

**Options Considered:**
| Option | Pros | Cons |
|--------|------|------|
| PostgreSQL | ACID, complex queries, mature | Schema planning needed |
| MongoDB | Flexible schema, scales horizontally | Eventual consistency |

**Decision:** PostgreSQL

**Rationale:** Data has clear relations, ACID needed for transactions.

**Decided By:** @lead with AI input

---

*Template Version: 2.0*