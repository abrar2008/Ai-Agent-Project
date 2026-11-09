---
name: personalize
description: Write a version of each campaign email for every lead group in leads/leads.csv. Use when a campaign's emails are final and you want one copy per group.
argument-hint: "[campaign folder]"
context: fork
allowed-tools: Read, Glob, Grep, Write
---

# Personalize campaign emails by lead group

Campaign folder: $ARGUMENTS

## 1. Check the campaign folder

- If no campaign folder was given above, **stop**. Use Glob on `campaigns/*/` and reply with a list of the campaign folders that exist, plus: "Run `/personalize <campaign folder>` with one of these." Don't write anything.
- If the folder doesn't exist, or it has no `emails/*.md` files, stop the same way and say what was missing.
- The source emails are only the files directly in `<campaign folder>/emails/`. Never use files under `<campaign folder>/groups/` as sources.

## 2. Read what you need

1. Every source email in `<campaign folder>/emails/`.
2. `leads/leads.csv`. Find the groups in the `group` column (expected: `tea-curious`, `gift-buyers`, `daily-drinkers`). Use only the group names. Never copy a lead's name, email or other details into an email.
3. `brand/voice.md` and `.claude/rules/emails.md`. Every version must follow both.
4. `<campaign folder>/plan.md`, if it exists. Use its audience section to see what each group wants and what holds them back, and its "must not" list for claims to avoid.

## 3. Write one version per email per group

For each source email and each group, write a copy that changes **only two things**:

1. **The opening line:** the first sentence after the `Hi {{first_name}},` greeting. Rewrite it so it speaks to that group.
2. **One example:** one sentence or bullet that shows why the email matters. Swap it for an example that fits the group. Change only one.

Everything else stays exactly the same as the source: the `Subject:` and `Preview:` lines, the greeting, the structure and order, every other sentence, the one main link and its button text, the sign-off and the footer.

What each group cares about:

| Group | Speak to |
|---|---|
| `tea-curious` | New to tea beyond tea bags. Wants an easy, no-guesswork way to try new teas. Worried it's too fancy or they won't like it. |
| `gift-buyers` | Buying for someone else. Wants a thoughtful gift that keeps arriving. Worried about timing and gift options. |
| `daily-drinkers` | Drinks tea every day and knows what they like. Wants something new and good value. Worried about repeats and price. |

If `plan.md` describes the groups differently, follow the plan.

### Rules for every version

- **Don't invent facts.** Keep every `[PLACEHOLDER]` exactly as written. Don't add prices, contents, gift options or delivery details that the source email doesn't already have. For gift buyers, never promise that a gift will arrive by a date. If you mention gifting, base it only on what the source email says, or add a `[GIFT OPTIONS]` placeholder.
- **No new claims.** No health claims, no delivery promises, no fake urgency and nothing else on the voice guide's or the plan's "must not" lists.
- **Same voice.** Plain American English, short sentences, no emojis, no more than one exclamation mark.
- **Same limits.** Keep each version at 150 words or fewer. Because the subject, preview, link, sign-off and footer don't change, the email rules still pass.

## 4. Save the files

- Save each version to `<campaign folder>/groups/<group>/emails/<same file name as the source>`.
- **Never overwrite.** If a file already exists at that path, don't touch it. Skip it and count it as skipped. (Replacing a draft counts as deleting it, and the user must approve deletions.)

## 5. Reply with a short summary only

Reply with only this, and nothing else. No email copy, no file list, no notes.

```
Wrote <N> files (<emails> emails × <groups> groups) to <campaign folder>/groups/.
<If any were skipped: Skipped <K> files that already existed.>

Example opening lines:
- tea-curious: "<opening line from the first email>"
- gift-buyers: "<opening line from the first email>"
- daily-drinkers: "<opening line from the first email>"
```
