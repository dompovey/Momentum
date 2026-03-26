# Momentum

**A personal thinking partner for dyslexic professionals.**

Momentum is a plugin for [Claude Cowork](https://claude.ai) that helps you think more clearly, start things you've been avoiding, ship work instead of looping on it, and see your progress when everything feels like it's standing still.

It is designed specifically for people with dyslexia and other neurodivergent cognitive profiles — particularly those who are intellectually strong but find certain tasks disproportionately draining: starting, switching, deciding when something is done, keeping track of time.

> Built by Dom Povey, a product leader and dyslexia advocate. Designed to be shared.

---

## What it does

**Brain dumps** — Write whatever is in your head. Momentum reads your energy, identifies what actually matters, and gives you one clear next action. No format required.

**Daily briefing** — Ask for a briefing and Momentum pulls your calendar, emails, and current priorities into one clear view. Type `/briefing` to trigger it.

**Coaching through blocks** — Stuck? Momentum identifies whether you are in a perfectionist loop, struggling to start, or just depleted, and responds accordingly with practical techniques.

**Progress tracking** — A journal system builds up over time so Momentum can surface patterns and show you what you have actually done when everything feels like it is standing still.

**Dyslexia support** — Evidence-based framing of how a dyslexic brain works. No deficit language. No lectures. No "despite your dyslexia."

---

## Who it is for

Momentum is built for people who:

- Have dyslexia (formally diagnosed or self-identified)
- Are intellectually strong but find executive function tasks disproportionately costly
- Experience task initiation paralysis, perfectionist loops, or time blindness
- Want a thinking partner that understands their cognitive profile, not a generic productivity tool

It works well for senior professionals, creatives, founders, and anyone managing complex work with a neurodivergent brain.

---

## Installation

1. Download the latest `momentum.plugin` file from the [Releases](../../releases) page.
2. Open Claude Cowork on your desktop.
3. Go to **Customize > Personal plugins** and click **+**.
4. Select the downloaded `.plugin` file.

Momentum will appear in your plugins list and activate automatically in new conversations.

---

## Getting started

Once installed, open a new conversation in Cowork. Momentum will walk you through a short setup conversation that takes about five minutes. It will ask you:

- A few questions about who you are and what you are working on
- Whether you want to set up a vision file (optional)
- Which integrations are connected

After setup, just talk. There is no required format. A few phrases that are useful to know:

| What you say | What happens |
|---|---|
| `/briefing` | Triggers your daily briefing |
| "Here's my brain dump" | Signals an unfiltered share |
| "How am I doing" | Triggers a progress review |
| "I'm stuck" or "I can't start" | Triggers coaching |

---

## Optional integrations

Momentum works without any integrations. These are optional but improve the daily briefing significantly.

| Connector | What it adds | Where to install |
|---|---|---|
| Google Calendar | Today's events in your briefing | Cowork > Customize > Connectors |
| Gmail | Unread email pulse in your briefing | Cowork > Customize > Connectors |
| Apple Mail | iCloud email pulse in your briefing | Cowork > Customize > Connectors |

If none are connected, the briefing still works and simply skips those sections.

---

## Your files

Momentum creates and reads a small set of files in your workspace. All of them live inside a `momentum/` subfolder in your selected folder.

| File | What it contains |
|---|---|
| `momentum-user-profile.md` | Your profile: name, role, current focus, integration settings |
| `momentum-vision.md` | Your long-game goals across three time horizons |
| `momentum-journal.md` | Active journal: last 30 days of entries |
| `momentum-journal-summary.md` | A synthesised portrait of your patterns and progress |
| `momentum-journal-archive.md` | Older entries, archived automatically |

You can edit any of these files directly at any time. Momentum reads them at the start of each session.

**Privacy:** All files are stored locally on your machine. Nothing is sent to an external server. Momentum has no account and no cloud storage.

---

## How it works

Momentum is a plugin for Claude Cowork, which means it runs entirely through Claude. The plugin provides Claude with a detailed set of instructions, frameworks, and personal context so that it behaves like a consistent thinking partner across sessions rather than starting from scratch each time.

The key files are:

- `skills/momentum/SKILL.md` — the rulebook: modes, protocols, communication rules
- `skills/momentum/references/frameworks.md` — the dyslexia framework and coaching protocols
- `skills/momentum/references/onboarding.md` — the first-time setup conversation guide
- `skills/momentum/references/journal-format.md` — the journal and archiving system
- `skills/momentum/assets/` — blank templates for user profile and vision files

The personal data (your profile, journal, vision) lives outside the plugin in your own workspace. This keeps the plugin shareable: the rulebook is universal, the personal layer is yours.

---

## Contributing

Contributions are welcome. If you use Momentum and find something that could work better, open an issue or a pull request.

A few things that would be particularly valuable:

- **Feedback from dyslexic users** on what works and what doesn't
- **Translations** of the onboarding flow and templates for non-English speakers
- **Additional coaching protocols** for specific challenges (e.g. rejection sensitivity, social anxiety in work contexts)
- **Integration guides** for other calendar or email tools

Please open an issue before starting significant work so we can discuss the approach first.

---

## License

MIT. Use it, share it, build on it.

---

## About

Momentum was built by [Dom Povey](https://github.com/dompovey) out of personal need and a belief that the tools most people use for productivity were not designed for how a dyslexic brain actually works.

If this helps you, share it with someone it might help too.

