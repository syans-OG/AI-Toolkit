---
name: pre-push-github
description: Run pre-push safety checks before `git push`. Use when the user asks to push, mentions "pre-push", or is about to push changes to GitHub. Catches broken builds, uncommitted changes, leaked secrets, and skipped tests before they reach the remote.
---

# Pre-Push GitHub

Run this before every push. Stop the push if any check fails.

## Checks (run in order)

### 1. Git status — are you on a clean branch?

```bash
git status --short
```

If there are uncommitted changes → **ask the user** whether to commit or stash them first. Never push with dirty working tree.

### 2. Branch protection — am I pushing to main/master?

```bash
git branch --show-current
```

If the current branch is `main`, `master`, `production`, or `release/*` → **warn the user** and ask for confirmation. These branches often have protection rules or deploy to production.

### 3. Secrets scan — are there tokens in staged files?

```bash
git diff --cached --name-only
```

For each staged file, check for patterns:
- `password =`, `secret =`, `api_key =`, `token =`, `bearer`, `sk_live`, `pk_live`
- `.env` files, credential files, private keys
- Long base64 strings (>100 chars) that look like embedded secrets

If secrets found → **block the push** and tell the user which files and lines.

### 4. Lint and type-check — does the code compile?

```bash
# Try the project's own checks first
npm run lint 2>&1 | Select-Object -First 20
npm run typecheck 2>&1 | Select-Object -First 20
```

If neither script exists in `package.json`, skip silently. If a script exists and fails → **block the push** and show the errors.

### 5. Tests — do they pass?

```bash
npm test 2>&1 | Select-Object -First 30
```

If no test script exists in `package.json`, skip silently. If tests fail → **block the push** and show the failures.

### 6. Diff review — what changed?

```bash
git diff HEAD~1 --stat
```

If more than **20 files** changed or more than **500 lines** changed → **warn the user** and suggest splitting into smaller commits.

## On success

If all checks pass → tell the user:

```
All checks passed. Safe to push.
```

Show the push command to run:

```bash
git push
```

Do **not** run `git push` automatically — let the user run it themselves after reviewing the summary.

## Output format

Print a simple checklist:

```
Pre-push checks:
  ✅ Clean working tree
  ✅ Not pushing to protected branch
  ✅ No secrets detected
  ✅ Lint passed
  ✅ Type-check passed
  ✅ Tests passed
  ✅ Diff size OK (12 files, +140 / -30 lines)
─────────────────────
Safe to push.
```