# 001 — UK SIA / Private Security Intelligence MVP

Throwaway MVP for a **UK private-security compliance intelligence** product focused on SIA-related change monitoring.

## What it does

- Monitors a curated set of GOV.UK / SIA-related sources
- Fetches and parses the page title, update date, summary, and headline snippets
- Stores snapshots in SQLite
- Diffs against the last stored snapshot
- Scores items against a sample operator profile
- Emits:
  - `out/latest_report.md`
  - `out/latest_report.json`
  - `out/latest_changes.md`
  - `out/latest_alert.txt`

## Why this is a good wedge

This targets a boring, recurring, underbuilt pain point:
- SIA licence renewals
- training rule changes
- licence-checking workflows
- close-protection refresher requirements

A real private-security operator can buy this as a low-touch subscription feed.

## Files

- `main.py` — runner / parser / diff engine
- `watchdog.py` — script-friendly entrypoint, silent when no changes exist
- `sources.json` — monitored sources
- `state/sia_monitor.db` — SQLite snapshots (created on first run)
- `out/latest_report.md` — human-readable report
- `out/latest_report.json` — machine-readable output
- `out/latest_changes.md` — change-only human-readable report
- `out/latest_alert.txt` — outbound alert text for messaging delivery

## Run

```bash
cd spikes/001-uk-sia-intel-mvp
python3 main.py run
```

Only changed sources:

```bash
python3 main.py run --changed-only
```

Silent watchdog mode:

```bash
python3 watchdog.py
```

Status:

```bash
python3 main.py status
```

List sources:

```bash
python3 main.py sources
```

## MVP output shape

Each source is turned into:
- status (`new-source`, `changed`, `unchanged`)
- page update date if found
- summary
- extracted key lines
- tags
- priority score for the target operator profile

In `watch` / `watchdog.py` mode, the process prints **nothing** when there are no material changes, which makes it suitable for cron-style automation.

## Next logical steps

- Add entity-level profiles for multiple customers
- Add evidence snapshots / archived HTML
- Add PDF parsing for attached notices
- Add richer customer-specific risk scoring
- Add a small web dashboard
- Add Stripe / auth / customer provisioning
- Expand to Companies House / procurement / other UK compliance surfaces

## Verdict: VALIDATED

### What worked
- The core monitor loop is viable with only Python stdlib
- GOV.UK pages are easy enough to fetch and parse for a first pass
- A recurring compliance-intel report can be generated without human intervention
- SQLite snapshotting and diffing are enough for an MVP
- Silent-no-change watchdog mode works for autonomous delivery

### What didn't
- Parsing is intentionally simple and not layout-robust yet
- No auth, billing, multi-tenant UI, or live notifications beyond scheduled delivery
- No PDF / attachment extraction in this version

### Surprises
- The best first MVP is more like a monitored feed engine than a traditional app
- SIA source coverage is already enough to demonstrate real value

### Recommendation for the real build
- Keep the first commercial version narrow: SIA / private security only
- Sell alerts + archive + entity matching, not broad "AI compliance"
- Add delivery integrations before adding fancy UI
