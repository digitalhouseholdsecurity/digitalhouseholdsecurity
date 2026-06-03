# Next Session

Last updated: 3 June 2026

## Project State

- The guide is now framed as **The Household Guide to Digital Security, Safety & Privacy**.
- The public domain is live at `https://digitalhouseholdsecurity.org`.
- `https://www.digitalhouseholdsecurity.org` redirects to the root domain.
- The current deployment is a Git-backed Cloudflare static-assets Worker named `digitalhouseholdsecurity`.
- The GitHub repo is `https://github.com/digitalhouseholdsecurity/digitalhouseholdsecurity`.
- The deployable web files now live in `public/`; `wrangler.jsonc` points Cloudflare Workers static assets at that folder.
- The old manual-upload Worker `cold-shape-1996` no longer owns the root custom domain.

## Current Files

- `public/index.html` - main guide content, navigation, references, glossary, scorecard script.
- `public/_headers` - basic Cloudflare security headers for the static-assets Worker.
- `public/robots.txt` - open indexing policy.
- `wrangler.jsonc` - Cloudflare Workers static-assets deployment config.
- `LICENSE.md` - CC BY-SA 4.0 guide licence note.
- `README.md` - public project summary for GitHub.
- `AGENTS.md` - standing project guidance for future AI assistants.
- `NEXT_SESSION.md` - current-session state and next-step notes.

## Recent Content Work

- Removed test `XXX` markers and repaired encoding/mojibake issues.
- Fixed appendix ordering and labels.
- Converted references to linked source-title format with access dates.
- Expanded Appendix C tool tables and reordered them by household importance/usage.
- Added Posteo, ONLYOFFICE, Ente Auth, backups, private storage, notes/local transfer, and cross-platform everyday tools.
- Reworked the higher-profile households section and added GrapheneOS wording as `GrapheneOS on supported Android Pixel phones`.
- Added a new Part 4 section: `11. Supporting children, teens & older relatives`.
- Renumbered later sections so the implementation roadmap is now section 18.
- Added citations for child/teen risks, older-adult scams, pause/verify guidance, and stalkerware/coercive-control risks.
- Regionalised the old `credit freeze` language into `new-account fraud protection`, with US, UK, and France examples.
- Replaced continuous section numbering with Part-local numbering such as `1.1`, `2.3`, and `4.4`.
- Promoted `Higher-profile households` to Part 6 and `Implementation roadmap` to Part 7, with internal numbering `6.x` and `7.x`.
- Removed the old `Interactive tools` sidebar divider because there is only one interactive appendix/tool.
- Added `robots.txt` with an open indexing policy.
- Added a small `Last updated: 3 June 2026` line under the sidebar tagline.
- Added a root `_headers` file with conservative browser security headers.
- Added an `About this guide` credibility section to the introduction, covering independence, sources, limits, regional variation, and update freshness.
- Added Part 5.3 `Scam playbook`, with practical household scam-response rules and FTC/NCSC/FBI citations.
- Renumbered Part 5 travel, incident response, and legacy sections to 5.4, 5.5, and 5.6.
- Added a CC BY-SA 4.0 footer note and `LICENSE.md`.
- Moved deployable website files into `public/` so Cloudflare Git deployments do not publish project notes.
- Added `README.md` for the GitHub repository.
- Added `wrangler.jsonc` for Cloudflare Workers Git deployment using `npx wrangler deploy`.
- Connected the GitHub repo to Cloudflare Workers; root and `www` domains now resolve to the new Git-backed deployment.

## Tone Decisions

- Prefer `household` over `family` unless the meaning is literally relatives or source/product wording.
- Keep the tone adult, calm, practical, and humane.
- Do not make the guide sound corporate, alarmist, or dumbed down.
- Treat children, teenagers, older relatives, less technical adults, disabled people, carers, guests, and people under stress as people with agency.

## Deployment Cleanup To Do

- Decide whether to delete the old `cold-shape-1996` Worker after a short settling period.
- Decide on a light bot policy after launch; do not block useful search/indexing bots by default.

## Verification Habits

- After content edits, search for `XXX`.
- Search for mojibake markers: `â`, `Ã`, `Â`, and `�`.
- If editing Appendix C, confirm `<table class="cmp">` and `</tbody></table>` counts match.
- If changing headings or section numbers, check ToC links and internal references.
- For citation edits, prefer official/primary sources and verify links.

## Automation Note

Python is not installed on the user's machine. Remind the user to install it when it becomes useful for link checking, citation audits, or monitoring related security/privacy news that may change the guide.
