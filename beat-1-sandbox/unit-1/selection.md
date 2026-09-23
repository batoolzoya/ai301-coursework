Unit 1 — Issue Selection

Path: beat-1-sandbox/unit-1/selection.md
Record of the issue carried into Unit 2, and of the evaluation runs that produced eval-run.txt. This file is graded at the path above; a copy kept anywhere else in the repository is not read.
Complete every labelled field below. Each is graded on its own; content placed under the wrong label is not graded.

Selected issue

Issue link
https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73

Verdict output
Scope — codepath/pathreview-ai301-fa26-s1 is the one scoped repo. In scope. Path Review house rule noted (classmate claim comments don't block); moot here, the thread is empty.

┌────────────────────┬───────┬─────────────────────────────────────────────────────────────────────────────────────┐
│        Check       │ Grade │                                      Evidence                                       │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ maintainer_active  │ pass  │ Collaborator Aburke225 committed 2026-09-16 (6 days ago) and labeled this issue the │
│                    │       │   same day — well inside 90 days                                                    │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ repo_in_use        │ pass  │ 29 commits on main (Link header page=29, per_page=1), pushed_at 2026-09-16,         │
│                    │       │ archived: false                                                                     │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────┤
│                    │       │ No CONTRIBUTING.md, AI_POLICY.md, or issue template in the repo — silence passes;   │
│ policy_compliant   │ pass  │ issue is a docs mismatch, not a vuln report, and asks for no secrets (only variable │
│                    │       │   names)                                                                            │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ clear_scope        │ pass  │ Body names exactly two files (README.md, .env.example), states the concrete         │
│                    │       │ discrepancy, and estimates "1–2 hours"; labeled good first issue + tier-1           │
├────────────────────┼───────┼─────────────────────────────────────────────────────────────────────────────────────┤
│ no_active_assignee │ pass  │ "assignees": [], comments: 0, timeline holds only 4 labeled events; the sole open   │
│                    │       │ PR (#74) targets issue #60                                                          │
└────────────────────┴───────┴─────────────────────────────────────────────────────────────────────────────────────┘

Fit note — the one accepted candidate lands well: it's a config/provider-key consistency fix around core/config.py and LLM_PROVIDER, so it puts you in the AI-engineering plumbing you want without any front-end UI work.

{
  "item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/73",
  "checks": [
    {"name": "maintainer_active", "grade": "pass",
     "evidence": "Collaborator Aburke225 committed 2026-09-16 and labeled this issue 2026-09-16T21:50:06Z, within 90 days of today (2026-09-22)"},
    {"name": "repo_in_use", "grade": "pass",
     "evidence": "29 commits on default branch main (pagination Link rel=last page=29); pushed_at 2026-09-16T21:48:27Z; archived=False"},
    {"name": "policy_compliant", "grade": "pass",
     "evidence": "No CONTRIBUTING.md/.github/CONTRIBUTING.md/AI_POLICY.md and no issue template; issue is a docs mismatch requesting no keys or secrets"},
    {"name": "clear_scope", "grade": "pass",
     "evidence": "Body: 'Relevant files: README.md, .env.example' with 'Estimated effort: 1-2 hours'; labels include 'good first issue' and 'tier-1'"},
    {"name": "no_active_assignee", "grade": "pass",
     "evidence": "assignees: [], comments: 0, timeline has only 4 labeled events; only open PR #74 is for issue #60"}
  ],
  "verdict": "accept"
}

Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

Run history
Run 1: 13/20 scored items (65%)
Run 2: 15/20 scored items (75%)
Run 3: 14/20 scored items (70%)
Run 4: 16/20 scored items (80%)

Issue analysis
issue-13: Your rubric's decision was REJECT, gold label was REJECT. The rubric checked `no_active_assignee` and identified that although no user was listed under `assignees`, a contributor had posted a comment claiming the issue and linked an open draft pull request. Because the rubric explicitly checks for linked PRs and active claims in comments, it correctly produced a REJECT decision matching the gold label.

Check rationale
"| clear_scope | issue body, title, or reproduction details | The task is bounded with a clear goal (small bug fix, UI tweak, doc update, or localized feature). PASS standard bug fixes or small tweaks even if short. REJECT if the issue requires broad architectural refactoring, changes across multiple subsystems, or lacks a concrete goal | required |"
Reasoning: Standard beginner issues are often written concisely without exhaustive line-by-line reproduction steps or exact file pointers. By explicitly instructing the model that standard bug fixes and doc updates pass even if brief—while reserving rejections for broad multi-module architectural overhauls—the check avoids false rejections on sparse beginner issues while still stopping unbounded tasks.

Trade-offs
By making `clear_scope` accept short or sparse descriptions for single bounded tasks, the rubric accepts that it will miss certain edge-case issues (such as `issue-12` and `issue-15`) where an issue description appears small on the surface but actually requires deeper architectural changes or touches multiple underlying subsystems once implementation begins.

Selection rationale

Selection rationale
Issue #73 fits my interest in backend configuration and LLM provider setup, with an estimated effort of 1–2 hours that easily fits within the Unit 2 timeline. The skill correctly identified active maintainer engagement, valid repo commit history, clear file boundaries (README.md and .env.example), and no existing assignees or PRs. What I weighed that the rubric could not was my familiarity with environment configuration files and how straightfoward the fix is to test locally. I anticipate low difficulty in claiming it since the comment thread is currently empty and unassigned.
