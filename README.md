# oyster-broodstock.github.io

Public project website for **Strengthening U.S. Oyster Broodstock Systems: Building Healthier, More Resilient Seed for American Growers** (USDA NIFA AFRI Sustainable Agricultural Systems, award 2026-68012-47021).

Built with [Quarto](https://quarto.org) and published to GitHub Pages.

## Site map

| File | Page |
|---|---|
| `index.qmd` | Landing page |
| `objectives.qmd` | The four objectives in detail |
| `team.qmd` | PD, Co-PDs, Co-Is, trainees |
| `partners.qmd` | Institutions, commercial partners, SAB, evaluator |
| `outputs.qmd` | Publications, data, code, extension products (**the reporting log**) |
| `timeline.qmd` | Year-by-year milestones |
| `news.qmd` + `posts/` | Dated announcements and updates |
| `contact.qmd` | Contacts and official award information |

## Before first publish

This repo is the **organization root site**. Because it is named `<org>.github.io`, GitHub publishes it at the org root with no path segment: `https://oyster-broodstock.github.io`. The repo name must match the org name exactly or the root URL will not work.

1. **Create the organization.** Create the GitHub org `oyster-broodstock` (free tier is sufficient). Add at least three owners spanning at least two institutions, so the org survives any one person's departure, and record the succession plan in the project's sustainability documentation.
2. **Create this repo as `oyster-broodstock.github.io`** inside that org and push this scaffold to `main`.
3. **Add the images.** Drop `logo.png` and `favicon.png` into `assets/`, then uncomment the `logo:` and `favicon:` lines in `_quarto.yml`. The site renders without them; the navbar just shows text.
4. **Turn on Pages.** Settings → Pages → Source → GitHub Actions. The included workflow does the rest.
5. **Custom domain (optional).** Add a `CNAME` file at the repo root containing your domain, point a DNS CNAME at `oyster-broodstock.github.io`, and set the domain under Settings → Pages. Less necessary now that the org root URL is already short.

### Access

Use org teams rather than per-repo collaborators. A team per institution (VIMS, Texas A&M, ARS, NOAA, OSU, UW) and a team per product keeps write access scoped, and keeps partner staff out of repos that do not concern them.

Federal co-PDs at USDA ARS and NOAA may be subject to agency policy on which GitHub organizations they can join or contribute to in an official capacity. Confirm with them before assuming they can be org members.

## Local preview

```bash
quarto preview
```

## Publish

Pushing to `main` triggers `.github/workflows/publish.yml`, which renders the site and deploys it to GitHub Pages.

## Adding a news post

```bash
mkdir -p posts/YYYY-MM-DD-short-slug
```

Create `index.qmd` in that folder with `title`, `description`, `date`, and `categories` in the front matter. It appears on the News page automatically.

## Maintenance

The `outputs.qmd` page is the one that matters for reporting. Add each publication, dataset, code release, extension product, presentation, and trainee outcome when it happens. At annual NIFA progress report time that page should be a copy-paste, not a reconstruction.

Suggested cadence: one named person does a 15-minute pass monthly, plus a review before each quarterly all-investigator call.

## What does not live here

The **PRISM Portal** and the **decision dashboard** are separate products with their own repositories and URLs. This site links to them; it does not host them. Planned repos in the `oyster-broodstock` org:

| Repo | Contents | Published at | Visibility |
|---|---|---|---|
| `oyster-broodstock.github.io` | This public project site | `oyster-broodstock.github.io` | Public |
| `prism` | PRISM Portal | `oyster-broodstock.github.io/prism` | Public |
| `dashboard` | Risk and portfolio-optimization decision tool | `oyster-broodstock.github.io/dashboard` | Public |
| `protocols` | Priming and phenotyping protocols, manuals | | Public |
| `data-schemas` | Shared cross-site data schemas (Year 1 milestone) | | Public |
| `admin` | Meeting notes, MOU and subaward status, budget and milestone tracking | | **Private** |

Any repo in the org that enables Pages publishes under the org root path automatically, so the products get clean sibling URLs without extra configuration.

Internal coordination material belongs in `admin`, not here.

## Acknowledgment

This work is supported by the Agriculture and Food Research Initiative Sustainable Agricultural Systems program, award no. 2026-68012-47021, from the U.S. Department of Agriculture, National Institute of Food and Agriculture.
