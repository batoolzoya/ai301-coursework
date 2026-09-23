# Rubric: is this a good first issue?

Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer_active | repo-facts block (`latest_commit_date` or comment timestamps) | At least 1 maintainer commit or comment within the last 90 days | required |
| repo_in_use | repo-facts block (`default_branch_commit_count` or issue thread activity) | The repository has at least 10 commits on default branch and activity within the last 180 days | required |
| policy_compliant | issue text, repo guidelines, or security disclosures | Issue complies with repo policies. REJECT if the issue reports a security vulnerability/exploit, asks for API keys/secrets, violates CONTRIBUTING rules, or is missing required issue template sections | required |
| clear_scope | issue body, title, or reproduction details | The task is bounded and self-contained (small bug fix, UI tweak, doc update, localized feature). REJECT if the issue requires broad architectural changes, multi-module refactoring, or lacks reproduction info | required |
| no_active_assignee | issue metadata block (`assignees` list or comment thread) | The issue is NOT assigned in `assignees`, has NO open pull request (PR), and has NO maintainer comment assigning it. Unconfirmed comments asking "can I take this?" MUST PASS | required |

Verdict rule

ACCEPT if every `required` check passes (`maintainer_active`, `repo_in_use`, `policy_compliant`, `clear_scope`, and `no_active_assignee`).

If ANY `required` check fails, the issue MUST be REJECTED.