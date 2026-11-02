# SoccerSessions: notes for agents

A public demo: a scheduling and sales-intake system for a fictional youth soccer
company. Spec and decisions: PLAN.md. Database version plan: docs/accounts-plan.md.

## Rules

- **Fictional data only.** Every company, center, coach, phone number and price is made
  up. Never use real names from the original system it was modeled on; grep before
  pushing.
- **The repo is about the build only** (Mason, 2026-11-02): nothing personal and nothing
  about job searching, in files, comments, commit messages or tags. Personal context and
  private paths go in CLAUDE.local.md (not in git). Private review notes live outside the
  repo.
- **Every change is a version:** CHANGELOG entry, `package.json` version, a tag, then
  `git push && git push --tags`. Restore an old version by committing it again; never
  rewrite history (the one exception was v3.1.1).
- `npm run check` (types, lint, tests) must pass. If the database changed:
  `npm run db:start`, `npm run db:reset`, `npm run test:db`, then `npm run db:stop`
  (its ports are reachable on the home network while it runs).
- Click through the demo in a real browser before calling a version done. Browser tests
  run muted (`--mute-audio`).
- Preview: `npx vite preview --port 10003`; `npm run screenshots` regenerates the README
  images from it. Stop it with `pkill -f "[v]ite preview"` as a command of its own: in a
  command line that also contains the words "vite preview", pkill kills its own shell.
