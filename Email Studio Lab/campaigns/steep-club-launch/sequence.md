# The Steep Club Launch: 4-Email Sequence

The email copy is in `emails/`. This file covers timing, who gets each email, subject line options and what to track.

**Goal:** 300 waitlist members start a paid subscription by Sunday, January 3, 2027.
**Who gets it:** Everyone on the waitlist (about 2,000 people) who hasn't joined yet.
**Story across the 4 emails:** It's open → here's what you get → your questions answered → the offer ends tomorrow.

## Overview

| # | File | Send date | Purpose | Main button | Who gets it |
|---|---|---|---|---|---|
| 1 | `01-doors-open.md` | Mon, Dec 7 | Tell the waitlist it's open, with the price and how it works | Join The Steep Club | Whole waitlist |
| 2 | `02-inside-the-box.md` | Mon, Dec 14 | Show the real first box and brewing card | See What's in the Box | Not yet joined |
| 3 | `03-questions-answered.md` | Thu, Dec 17 | Answer the questions that stop people joining | Join The Steep Club | Not yet joined |
| 4 | `04-last-call.md` | Sat, Jan 2 | Final reminder before the offer ends | Join Before Sunday | Not yet joined |

All four go to every group. The plan's group-specific and holiday emails (2b, 5, 5b, 6, 6g) aren't in this 4-email version. To add them later, the Dec 21 and Dec 29 slots are still free.

## Subject line options

The subject line in each file is option A.

| # | A (in file) | B | C |
|---|---|---|---|
| 1 | The Steep Club is open | You're first in line, {{first_name}} | Doors are open at The Steep Club |
| 2 | Take a look inside the first box | Here's what's in your first box | Meet the teas in box one |
| 3 | Your Steep Club questions, answered | Price, delivery and cancelling, answered | Before you join: the short FAQ |
| 4 | Our founding member offer ends tomorrow | Last day for founding members | One day left to join as a founder |

## Flow

```
[Mon Dec 7] Email 1 (whole waitlist)
      |
  Joined? --Yes--> [EXIT: welcome email takes over]
      | No
[Mon Dec 14] Email 2
      |
  Joined? --Yes--> [EXIT]
      | No
[Thu Dec 17] Email 3
      |
  Joined? --Yes--> [EXIT]
      | No
   (Dec 21-27: no send. Spare slot for an extra
    reminder if we're behind on Dec 14.)
      |
[Sat Jan 2] Email 4
      |
[EXIT: sequence complete]
```

## Rules for sending

- **Exit:** Anyone who starts a paid subscription leaves the sequence right away. The welcome email takes over.
- **Unfinished checkout:** Anyone who starts checkout but doesn't finish gets the automatic reminder 24 hours later. It's separate from this sequence.
- **Don't send to:** People who unsubscribed, people who already joined, or anyone on a spam complaint list.
- **No re-entry:** Nobody gets the sequence twice. People who don't join get a decision on Jan 4 (for example, a gentle follow-up in February).
- **No sends** on Christmas Eve, Christmas Day or New Year's Day. No more than 2 emails a week.
- **Drafts only.** The owner loads and sends these in their own email tool. Claude never sends, schedules or test-sends.

## A/B tests

1. **Email 1 subject line:** A ("The Steep Club is open") vs. B ("You're first in line, {{first_name}}"). Split 50/50, or test on 20% and send the winner to the rest. The winner is the one with more clicks, not just more opens.
2. **Email 4 subject line:** A ("...ends tomorrow") vs. B ("Last day for founding members"). Same method. Measure by sign-ups within 48 hours.
3. **Email 2 button text** (if there's time): "See What's in the Box" vs. "Join The Steep Club". Measure by sign-ups, not clicks.

## What to track

Targets come from the plan (section 7). They're our own goals, not industry benchmarks.

| Measure | Target |
|---|---|
| Open rate per email | 40% or higher |
| Click rate per email | 5% or higher |
| Unsubscribes per email | Under 0.5% |
| Spam complaints per email | Under 0.1% |
| Sign-ups | 120 by Dec 13, 195 by Dec 20, 300 by Jan 3 |

Check every Monday. If we're under 100 sign-ups on Dec 14, use the spare slot. Low clicks mean the email is the problem. Good clicks but low sign-ups mean the page or price is the problem.

## Before these go into the email tool

Each email has placeholders in square brackets. Fill in and confirm every one:

- [ ] `[PRICE]`, `[NUMBER]` of teas, `[BOX CONTENTS]` and box photo
- [ ] `[CANCELLATION POLICY]`, copied word for word
- [ ] `[SHIPPING COST AND AREAS]`
- [ ] `[GIFT OPTIONS]`, or delete that question from Email 3
- [ ] How teas are picked (Email 3) and what brewing kit is needed (Email 2)
- [ ] Founding member offer: `[OFFER]`, `[OFFER PERIOD]`, `[END TIME]`. **If the owner says no offer, Email 4 must be rewritten.** Without a real deadline we can't say "ends tomorrow."
- [ ] Sign-off: the emails use "Best regards, The Kettlebird Tea Team". This follows the pattern in `brand/voice.md`, but that guide is written for Prime Patchy. Confirm it, or replace it once a Kettlebird voice guide exists.
- [ ] Check each email against the "must not" list in the plan (section 3).

## Setup checklist (any email tool)

1. Make a list or segment of waitlist members who haven't subscribed.
2. Create 4 one-off sends with the dates above. These are fixed dates, not a timed drip.
3. Before each send, remove anyone who has joined since the last one.
4. Set up the welcome email and the unfinished checkout reminder as automations.
5. Turn on click and sign-up tracking. Tag sign-ups by group (`tea-curious`, `gift-buyers`, `daily-drinkers`) so we can see which group joins most.
