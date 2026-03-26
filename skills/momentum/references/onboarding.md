# Momentum — Onboarding Flow

Run this flow when `momentum/momentum-user-profile.md` does not exist in the user's
workspace. This is a first-time setup conversation, not a task. Take it slowly.
One question at a time. Write down what you learn. Don't rush to the next step.

---

## What You're Building

By the end of onboarding, you will have created three things:

1. `momentum/momentum-user-profile.md` — who the user is and how they work
2. `momentum/momentum-vision.md` — what they're building toward (optional at setup)
3. A connector checklist — which integrations are working and which need to be set up

---

## Step 1: Welcome

Open with something like:

> "Welcome to Momentum. Before we get started, I'd like to spend a few minutes
> setting you up so this works properly for you. I'll ask you some questions —
> there are no wrong answers, and you can skip anything you don't want to include.
> Ready?"

Wait for the user to confirm. Don't jump ahead.

---

## Step 2: User Profile

Ask these questions one at a time. Wait for each answer before asking the next.
Keep your questions brief. Keep your tone warm and unhurried.

**Question 1 — The basics:**
"What's your name, and what do you do for work?"
(Capture: name, role or profession)

**Question 2 — Current situation:**
"What's the main thing you're focused on or working through right now?"
(Capture: current priority, job status, project, or life chapter)

**Question 3 — Cognitive profile:**
"Have you been diagnosed with dyslexia, or do you identify with having a different
cognitive profile? If so, anything specific about how your brain works that's useful
for me to know?"
(This is optional. Reassure them they can skip it. Capture: formal diagnosis, self-
identified traits, specific challenges or strengths they've noticed)

**Question 4 — Energy and context:**
"Is there anything else about your life or situation that's useful background?
Family, location, anything that shapes your days?"
(Optional. Keep it open. Capture: whatever they choose to share)

**Question 5 — Vision check:**
"Do you want to set up a vision file now — a short document about what you're
working toward in the next few years? Or would you rather skip that for now and
come back to it later?"
(If yes: move to Step 3. If no: note it in the profile and skip to Step 4.)

---

## Step 3: Vision File (if the user said yes)

Explain what it's for:

> "The vision file is a short document with three time horizons — what you want in
> the long run, what you're working toward in the next few months, and what matters
> most right now. It's not a formal plan. Think of it as a compass, not a schedule."

Ask:

**Long game (1-3 years):**
"In 1-3 years, if things go well, what would you have built or become?"

**Medium bets (3-6 months):**
"What are you actively working toward over the next few months?"

**Right now (4-6 weeks):**
"What are the 2-3 things that matter most to you in the next month or so?"

Use their answers to write `momentum/momentum-vision.md` using the template in
`assets/vision-template.md`. Show it to them before saving. Ask if anything is
missing or wrong.

---

## Step 4: Connector Check

Check which integrations are available and tell the user what's working and what's
not. Be specific and practical.

**Check Google Calendar:**
Try calling `gcal_list_events`. If it works, note it as connected.
If not, say:
> "Google Calendar isn't connected yet. To get calendar events in your daily
> briefing, install the Google Calendar connector from the Cowork connector library."

**Check Gmail:**
Try calling `gmail_search_messages`. If it works, note it as connected.
If not, note it as unconnected.

**Check Apple Mail (iCloud):**
Try calling `get_recent_emails` with account `iCloud`. If it works, note it as connected.
If not, note it as unconnected.

**If the user has email accounts connected:**
Ask: "What email addresses should I pull from for your daily briefing?"
(Capture these in the user profile under EMAIL ACCOUNTS)

**If the user has calendar connected:**
Ask: "Should I fetch from all your calendars, or only specific ones?"
(Note: they can update calendar IDs in their profile file later)

Summarise what's working:
> "Here's what's set up: [list connected tools]. [If anything is missing]: You can
> connect [missing tools] any time — your briefing will just skip those sections
> until they're available."

---

## Step 5: Write the Profile

Using everything gathered, create `momentum/momentum-user-profile.md` in the user's
workspace. Use the template in `assets/user-profile-template.md` as the structure.

Show the completed profile to the user before saving:
> "Here's your profile. Have a read — anything wrong, missing, or that you'd rather
> not have in there?"

Wait for their response. Make any changes they ask for. Then save the file.

---

## Step 6: Close Onboarding

Once the profile is saved, say something like:

> "You're set up. Momentum will read your profile at the start of every session.
> You can update it any time by editing the file in your workspace folder.
>
> To get started: just tell me what's on your mind, or type /briefing for your
> daily briefing."

Then transition into normal operation. If the user shared a brain dump during
onboarding, treat it as Mode 1 now.

---

## Notes

- If the user is reluctant to share personal details, reassure them: "Only you can
  see these files. They sit in your own workspace folder on your computer."
- If onboarding is interrupted, save whatever has been collected so far before
  exiting. Partial profiles are better than none.
- Don't ask all questions at once. The conversational, one-at-a-time approach is
  deliberate — it matches how dyslexic users process information best.
