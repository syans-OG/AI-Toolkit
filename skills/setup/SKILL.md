---
name: setup
description: Skill router for opencode. Use when a task crosses multiple domains, when you are unsure which installed skill applies, or when you are writing or installing new skills. Routes a request to the minimal matching skills by scenario and falls back to find-skills when no installed skill covers the domain.
---

# Setup — skill router

Resolve a request to the **minimum set** of applicable skills. Pick by scenario; stop at 1-3 skills. This is a decision tree, not a mandatory pipeline. Do not run a skill checklist before work — only route when the work reaches a mapped domain.

---

## When to use this

- The task spans domains, or you are unsure which skill applies.
- The work is unfamiliar and you want a quick map before acting.
- You are writing or installing new skills.

For a single-domain task where one skill clearly fits, use that skill directly and skip routing.

## Scenario map

Pick the branch that matches the dominant question, then load the listed skill(s).

### Coding — features & fixes

| Scenario | Load |
|---|---|
| New feature, ambiguous scope | `brainstorming` → `lean-build` |
| Debug / incident | `investigate-first` → `systematic-debugging` → `surgical-patch` |
| Writing tests | `tdd`, `lint-and-validate` |
| Reviewing changes | `code-review` |
| Slow code / hot path | `performance-optimizer` |
| Refactor, no behavior change | `safe-refactor` |
| Schema / data / API change | `migration` |
| Module seams / structure | `backend-architect` |
| Terminal ops / CI failure | `terminal-ops` |

### Frontend (web)

| Scenario | Load |
|---|---|
| Build a page / UI from scratch | `anti-ui-slop`, `frontend-design` or `design-taste-frontend`, `pick-ui-library` |
| Explore UI directions before building | `prototype` |
| React / Next.js app | `react-nextjs-development`, `react-patterns` |
| Styling | `tailwind-patterns` |
| Motion | `animate` |
| Vite wiring | `vite-patterns` |
| TypeScript strictness | `typescript-expert` |

### Desktop (Tauri / Windows)

| Scenario | Load |
|---|---|
| Window customization | `customizing-tauri-windows` |
| IPC, capabilities, core | `tauri-v2` |

### Backend / API

| Scenario | Load |
|---|---|
| Routes, services, repositories | `backend-dev-guidelines` |
| API security | `api-security-best-practices`, `backend-security-coder` |
| Distributed / scaling architecture | `backend-architect` |

### Planning & continuity

| Scenario | Load |
|---|---|
| Idea → validated design | `brainstorming`, `domain-modeling` |
| Discussion → spec | `to-spec` |
| Spec → tickets | `to-tickets` |
| Resume work in a new session | `handoff` |

### Skills & agent docs

| Scenario | Load |
|---|---|
| Writing/editing `SKILL.md`, `AGENTS.md`, prompts | `writing-for-agents` |

---

## Working rules

1. **Minimal selection.** At most 1-3 skills per task. More than that invites conflicting instructions, not better output.
2. **Skills are sinks, not a checklist.** Load one when the work reaches its domain; do not front-load unrelated tools.
3. **Consult the environment first.** `package.json`, config files, and `--help` answer what they already state — a skill must not restate them.
4. **Proof of done.** When changes are complete, verify with `verify-and-stop`: run the relevant tests or builds and stop once the criteria are met.
5. **Recursion instead of sprawl.** If no installed skill covers the domain, run `find-skills` and install one specific skill — do not compensate with generic advice.

---

## Fallback discovery

If a task needs specialized domain knowledge with no local skill:

1. Activate `find-skills`.
2. `npx.cmd skills find [topic]` — search for skills.
3. Install the trusted one: `npx.cmd skills add <package> -g -y`.