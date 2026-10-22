# Governance

This is a small volunteer group, so the rules are kept light. They borrow from projects that have handled the same
problems at much larger scale: the CNCF project maturity levels, Apache-style lazy consensus, and Astropy's
proposal (APE) process.

## Roles

| Role | Who | Can |
|---|---|---|
| **Member** | Anyone invited to the org | Create repos (they start as `sandbox`), open PRs and issues anywhere, post in Discussions |
| **Project owner** | The person who created a repo, plus anyone they add | Run their repo however they like, within the Code of Conduct |
| **Maintainer** | Listed below | Merge PRs to the shared files in [`hub`](https://github.com/aiassistedastronomytaskforce/hub), change org settings, move projects between stages, enforce the Code of Conduct |

Maintainers: @troynguyen8transits

New maintainers are nominated in a hub Discussion by an existing maintainer, after a few months of steady
contributions, and added by lazy consensus. The aim is at least three maintainers from different places, so the
org never depends on one person.

## Making decisions

- **Your own repo:** your call.
- **Shared files in `hub`** (data formats, vetting rules, benchmark, templates): open a PR. Small fixes merge after one
  maintainer approval. Changes to rules or formats stay open **7 days** for comment and merge if nobody objects
  (lazy consensus). An objection needs a reason and, ideally, an alternative.
- **Big changes** (a new data format, a change to the evidence ladder, anything that makes existing work
  non-compliant): add a short proposal in `hub/proposals/` and link it in Discussions. Decide by lazy consensus
  after 14 days, or by a majority of maintainers if it's contested.

## Project lifecycle

Every repo in the org is at one of four stages, shown by a `stage-*` topic on the repo.

| Stage | Meaning | Requirements |
|---|---|---|
| `sandbox` | New or experimental. No promises. | A `project.yaml` and a registry entry in `hub/projects/` within 2 weeks of creation |
| `active` | Usable by someone other than the author | README that explains how to run it, a license, an AI-use section, and one other member has run it |
| `featured` | Recommended starting points | Pipelines: published benchmark results. Demos and tools: read or write the shared formats in `hub/schemas/`. Agreed by a maintainer |
| `archived` | Kept for the record, read-only | No commits for 6 months and no reply to a ping, or the owner asks. Reversible at any time |

Moving to `active` or `featured`: open a PR that changes the stage in your `hub/projects/<repo>.yaml` file.

## Why this structure

AI tools make new code cheap, so there will be many repos, often overlapping. The shared value is not one perfect
codebase. It is:

1. a record of what has been searched and found (`hub/targets`, `hub/coverage`);
2. common data formats, so independently generated projects can work together (`hub/schemas`);
3. a common test set and vetting standard, so results can be compared (`hub/benchmark`, `hub/VETTING.md`).

Projects can be messy, regenerated or abandoned. The shared files are what get careful review.
