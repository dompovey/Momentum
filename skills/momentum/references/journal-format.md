# Momentum — Journal System

The journal is the memory layer. It accumulates entries over time, enabling pattern
detection and progress visibility across sessions. Without it, every conversation starts
cold. With it, Momentum builds a picture of who the user is and where they're going.

---

## File Locations

All files live in `momentum/` inside the user's workspace folder:

| File | Purpose |
|---|---|
| `momentum-journal.md` | Active journal — last 30 days of entries. Always loaded. |
| `momentum-journal-summary.md` | Long Game Portrait — synthesised history. Always loaded. |
| `momentum-journal-archive.md` | Raw entries older than 30 days. Never auto-loaded. |

---

## Journal Entry Format

Append this format after each meaningful interaction:

```
---
DATE: [YYYY-MM-DD]
TIME: [morning / midday / evening / ad hoc]
ENERGY: [1-10 if stated or estimable, otherwise omit]
MIND STATE: [high momentum / perfectionist loop / time blindness / big picture lost / depleted / inspired / stuck]
TAGS: [comma-separated topics — e.g. job search, vision, fitness, family, shipping, decision]
WINS: [anything shipped, completed, progressed, or attempted — even small things count]
CONTENT:
[Key themes from what was shared — signal only, not full transcript. 3-8 lines.]
PATTERNS NOTED:
[Cross-references with previous entries. Leave blank if none observed.]
---
```

**On the WINS field:** This is the most important field. It creates a visible record of
forward motion that counteracts the feeling of standing still — one of the most draining
experiences for people with this cognitive profile. If in doubt whether something counts
as a win, include it.

---

## Long Game Portrait Format

The `momentum-journal-summary.md` file is a synthesised portrait of the user, rewritten
each archiving pass. It is prose, not tags. It should read like a thoughtful observer
describing who this person is and where they are right now.

Target length: 40-60 lines. Every line earns its place.

```markdown
# Momentum — Long Game Portrait
_Last updated: [DATE]. Covers all journal entries through [DATE]._

---

## Who They Are

[2-4 sentences. Stable traits: cognitive profile, how they operate under pressure,
what energises them, what drains them. Updated rarely — only when something shifts.]

## Where They Are Right Now

[3-5 sentences. Current chapter: professional situation, active pressures, what they're
building toward. Updated each archiving pass to reflect the current moment.]

## Patterns That Persist

[The recurring patterns observed across multiple journal periods. What triggers high
energy. What triggers loops. How they recover. What "good" looks like for them.
Write as observed facts, not generalisations.]

## What They Have Shipped

[A running record of meaningful wins — things completed, published, progressed, or
overcome. Brief. Chronological. Even small things count if they cost something to do.]

## Open Loops

[Themes or questions that have come up repeatedly but remain unresolved. Things they
keep returning to. Decisions not yet made. Updated each pass — remove loops that close,
add new ones that emerge.]

---
_Raw entries archived to momentum-journal-archive.md._
```

---

## Archiving Process

The archiving process runs when the active journal contains entries older than 30 days.
It is always flagged to the user first. Never run silently.

### Trigger

At the start of a session, if `momentum-journal.md` contains any entries dated more
than 30 days before today, say:

> "Your journal has entries older than 30 days. Ready to archive and summarise?
> It's a good moment to surface patterns and wins before we clear the older entries out."

Wait for the user to confirm before proceeding.

### Steps

**1. Synthesise**
Read all entries older than 30 days. Draft an updated Long Game Portrait using the
format above. Do not write it yet.

**2. Show and discuss**
Present the draft portrait to the user:
> "Here's what I'm capturing from this period. Have a read — anything missing,
> wrong, or worth adding before I save it?"
Wait for their response. Make any changes they ask for.

**3. Write**
Once the user is happy, do the following in order:
1. Overwrite `momentum-journal-summary.md` with the updated portrait.
2. Append the raw entries being archived to `momentum-journal-archive.md` with a
   dated section header (e.g., `## Archive: January 2026`).
3. Remove those entries from `momentum-journal.md`, leaving only the last 30 days.

**4. Acknowledge**
Confirm in one sentence. Then continue with the session normally.

---

## First-Time Setup

If `momentum-journal.md` does not exist, create it with a single header line:

```markdown
# Momentum Journal
```

Then write the first entry from the current session.
