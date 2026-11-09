---
paths:
  - "campaigns/**/emails/*.md"
---

# Email file rules

These rules apply to every email file in any campaign's `emails/` folder. Every email file must follow all of them.

## 1. Subject and preview come first

- **Line 1** must start with `Subject: ` and then the subject line.
- **Line 2** must start with `Preview: ` and then the preview text.
- The subject must be **50 characters or fewer**, and the preview must be **90 characters or fewer**. Count only the text after `Subject: ` or `Preview: `, including spaces.
- Nothing goes above these two lines. No title, no front matter, no blank line.

Example:

```
Subject: The Steep Club is open
Preview: You asked to be first in line. Here's your spot.
```

## 2. Greet the reader by first name

- The greeting must use `{{first_name}}` exactly as written, for example `Hi {{first_name}},`.
- Don't type a real or made-up name in its place, and don't change the spelling or the braces.

## 3. One main link only

- Each email has **exactly one** main link, written like this:

  `[Button text](https://kettlebird.example/steep-club)`

- Change the button text to fit the email, for example `[Join The Steep Club](https://kettlebird.example/steep-club)`. Keep the URL exactly as shown.
- Don't add a second button or a different main link. The unsubscribe link in the footer doesn't count as the main link.

## 4. Sign-off, then footer

- The body ends with this sign-off, written exactly like this, as plain text:

Best regards,

The Kettlebird Tea Team

- Why not the signature in `brand/voice.md`? That guide is for Prime Patchy, so its signature would put the wrong brand on Kettlebird Tea emails. This sign-off uses its default closing line ("Best regards,") and its sender pattern for general emails ("The ... Team"). Don't make up a different one. If a Kettlebird voice guide is added later, use its sign-off and update this rule.
- After the sign-off, end the file with this two-line footer, written as **plain text**, not inside a code block:

You're getting this because you joined the Kettlebird Tea waitlist.
Kettlebird Tea, {{company_address}} · Unsubscribe: {{unsubscribe_url}}

- Copy the footer word for word. Keep `{{company_address}}` and `{{unsubscribe_url}}` as they are. Nothing goes after the footer.

## Quick check before saving

- [ ] Line 1 is `Subject:` and the subject is 50 characters or fewer
- [ ] Line 2 is `Preview:` and the preview is 90 characters or fewer
- [ ] The greeting uses `{{first_name}}`
- [ ] There's exactly one main link, to `https://kettlebird.example/steep-club`
- [ ] The sign-off is "Best regards," then "The Kettlebird Tea Team"
- [ ] The two-line footer is last, in plain text, not in a code block
