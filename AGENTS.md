# AGENTS.md

Guidance for AI assistants working on this project.

## Project

This is a household-focused digital security, safety, and privacy guide. It is currently a static HTML/CSS draft, with the likely future direction of becoming a website.

Main files:

- `index.html` - content, navigation, references, glossary, scorecard script.
- `_headers` - basic Cloudflare security headers.
- `robots.txt` - open indexing policy.
- `LICENSE.md` - CC BY-SA 4.0 guide licence note.

## Current Deployment

- The domain `digitalhouseholdsecurity.org` is registered through Cloudflare and is live.
- `https://digitalhouseholdsecurity.org` serves the current static site through a Cloudflare static-assets Worker.
- `https://www.digitalhouseholdsecurity.org` redirects to the root domain.
- The Cloudflare app was created by uploading static files and currently has an auto-generated name: `cold-shape-1996`.
- Next cleanup items:
  - Rename the Cloudflare app to something like `digital-household-security`.
  - Decide whether to connect Git for repeatable deployments instead of manual uploads.
  - Add a simple `robots.txt` after the content structure settles.
  - Consider basic security headers and light bot policy after launch.

## Audience And Voice

- Write for households, not businesses or enterprise IT.
- Prefer `household` over `family` when referring to the audience. Use `family` only when the meaning is literally relatives, family members, or source/product wording.
- Include one-person households in assumptions and examples.
- Keep the tone practical, calm, and non-alarmist. The guide should make readers feel capable, not doomed.
- Avoid turning recommendations into absolutes. Use clear defaults, tradeoffs, and priority language.

## Content Rules

- Keep recommendations household-realistic: high impact, affordable, and maintainable.
- Prioritize account protection, device updates, backups, fraud prevention, and incident preparation over niche or high-effort tools.
- Regionalize legal, financial, telecom, identity, and reporting advice. Do not make US-only mechanisms such as credit freezes sound universal; describe the goal and give country-specific examples.
- When adding tools, prefer cross-platform options unless there is a strong reason not to.
- In Appendix C, keep tool tables in household priority order rather than product-category purity.
- Do not add sponsored-sounding language. Product mentions should read like practical recommendations, not marketing copy.
- Use `trusted-person code word` in recommendations unless quoting or summarizing a source that specifically says family code word.

## Citations And Sources

- Use as many accurate citations as practical for factual claims that readers may doubt.
- Prefer primary or authoritative sources: CISA, NCSC, NIST, FBI/IC3, FTC, CFPB, FCC, GOV.UK, OWASP, EFF, official vendor documentation, and standards/RFCs.
- Reference format should be:
  - Source name
  - Linked title
  - Short relevance note
  - `Accessed 2 June 2026` unless doing a fresh citation pass with a newer access date.
- Multiple links in one reference are encouraged when they support the same claim from different angles.
- If updating current guidance, verify links and dates first. Security guidance and product features can change.

## Editing Rules

- Preserve UTF-8 punctuation and entities. After broad edits, check for mojibake markers such as U+00E2, U+00C3, U+00C2, and U+FFFD showing up as visible text.
- Preserve existing IDs where possible, especially navigation, glossary, footnotes, and JavaScript hooks.
- If changing a heading ID that appears in links or navigation, update all references to it.
- Keep visible references linked. Footnote hover text should stay simple and should not duplicate full citations.
- Use `apply_patch` for manual edits.

## Verification

After content edits, run lightweight checks where relevant:

- Search for accidental test markers such as `XXX`.
- Search for mojibake markers such as U+00E2, U+00C3, U+00C2, and U+FFFD showing up as visible text.
- Check table balance if editing Appendix C:
  - Count `<table class="cmp">`
  - Count `</tbody></table>`
- Check that expected appendix titles and section labels still match the visible navigation.
- For citation changes, search for stale wording such as `reviewed June 2026` or vague old source descriptions.

## Future Automation

Python is not currently installed on the user's machine. Remind the user to install Python only when it becomes useful, such as for:

- Link checking.
- Monitoring official sources and RSS feeds.
- Building a review queue for source updates.
- Automating citation audits.
- Larger HTML validation or normalization tasks.
