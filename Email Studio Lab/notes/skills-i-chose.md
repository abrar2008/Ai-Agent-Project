# Skills I chose

Checked on 9 November 2026. Star and install counts will change over time. Nothing is installed yet.

## Use these

**For writing campaigns: `anthropics/knowledge-work-plugins` (35,248 stars)**
- This is published by Anthropic, the company that makes Claude, and 32 people have contributed to it.
- It covers the job well: `campaign-plan` writes the campaign brief and calendar, `email-sequence` drafts a series of emails with timing, and `draft-content` writes one-off pieces such as newsletters and subject line options.
- All three start by asking you for the details they need. The wider marketing plugin also lists connections to outside services such as HubSpot and Klaviyo, so check what you are turning on if you install the whole plugin.

**For sending email: `resend/resend-skills` (211 stars)**
- This is published by Resend, the email service itself, and Resend's own website links to it. The star count is low, but the publisher matters more here.
- It covers sending single emails and broadcasts to a list, plus managing contacts and domains.
- It needs your Resend API key and can send real email, so keep the key private and test on your own address first.
- One security scanner (Snyk) gives it a medium warning because reading incoming email exposes the AI to text written by strangers. Sending email isn't what the warning is about, but take care if you later use it to read replies.

## Avoid these

**`claude-office-skills/skills@email-marketing` (570 stars, 5.2K installs)**
- The name sounds official, but the account is called "AGI Lab", not Anthropic.
- The account was created the same day as the repository. All 31 commits happened within three days in January 2026, and it has not been updated since.
- The skill relies on an `email-mcp` server that is not in this repository, so part of how it works can't be checked here.
- Its instructions also offer an install that pipes a script from the internet straight into your computer's shell (`curl | bash`), which is a habit to avoid.

**`mbfinotti/sales-skills` (3 stars, about 33K installs per skill)**
- The numbers don't add up: tens of thousands of installs, but only 3 stars, an owner with 3 followers, and a repository about two months old with one contributor.
- I found nothing harmful, and the writing looks careful. I just can't tell where those install numbers come from, so they aren't evidence that people trust it.
- It tells you to install all 27 skills rather than one, and it is built for sales outreach, not email marketing to your own subscribers.

## How I decided

Check these three things before installing any skill:

1. **Who really publishes it?** Look at the exact account name, not the skill's name. Anyone can put "claude" or "resend" in a name. A real company's skill is usually under its own account and linked from its own website.
2. **Do the numbers make sense, and is it still looked after?** Compare stars with installs, then check the last update and the number of contributors. A big gap between stars and installs, or a repository that stopped changing soon after it appeared, is a warning sign.
3. **What does it actually do?** Read its `SKILL.md`, and look for any keys it asks for, scripts it runs, or outside services it depends on. Then read the security audits on its skills.sh page. A pass helps but doesn't settle it: both skills I'm avoiding passed all three audits.
