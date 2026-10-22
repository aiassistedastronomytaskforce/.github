# Contributing to AI-Assisted Astronomy Taskforce projects

This is the default guide for every repo in the org. A repo may have its own CONTRIBUTING.md with extra rules.

## Starting a new project

1. Create it from [`project-template`](https://github.com/aiassistedastronomytaskforce/project-template)
   ("Use this template"). Name it with a kind prefix:

   | Prefix | For | Example |
   |---|---|---|
   | `pipeline-` | Searches and analysis of survey data | `pipeline-eb-residuals` |
   | `demo-` | Interactive or visual demos, simulations, teaching pages | `demo-doppler-wobble` |
   | `tool-` | Reusable utilities and libraries | `tool-tesscut-photometry` |
   | `data-` | Curated datasets, catalogs, cross-matches | `data-tess-cbp-list` |
   | `paper-` | A write-up, note or poster and its figures | `paper-rnaas-quadruples` |

2. Fill in `project.yaml` and add the same information as `projects/<repo-name>.yaml` in
   [`hub`](https://github.com/aiassistedastronomytaskforce/hub). That registration is what keeps 50 repos findable.
3. Add the topics `kind-<kind>` and `stage-sandbox` to the repo.

Before you start, look at the [project registry](https://github.com/aiassistedastronomytaskforce/hub/blob/main/PROJECTS.md).
If something close exists, a PR or a fork is often better than a new repo. When a new repo really is easier
(often true with AI tools), say in its README what it replaces or differs from.

## Working on someone else's project

Open an issue first for anything bigger than a small fix, so the owner can say whether it fits. Owners decide what
goes into their repos. If you disagree, fork it and register the fork: that is a normal outcome here, not a conflict.

## AI-generated work

Nearly everything here will be written with AI help. That's fine. The rules:

- **Disclose it.** Each project README has an AI-use section saying what the AI did and what you checked yourself.
- **Check what you publish.** Catalog IDs, periods, citations and data values from AI output must be checked against
  the source before they're committed. Made-up references are the most common failure.
- **Don't flood.** Don't open large AI-generated PRs on other people's repos without asking first. Reviewing them
  costs the owner far more than they cost you to generate.
- **Physics claims need data.** A demo can simplify the physics, but its README should say what is simplified.

## Science results

Candidate objects, search coverage and independent checks go in `hub`, following
[`hub/VETTING.md`](https://github.com/aiassistedastronomytaskforce/hub/blob/main/VETTING.md). Nothing is announced
as a discovery from this org. Use the usual channels (ExoFOP, AAVSO VSX, RNAAS, the relevant professional team).
