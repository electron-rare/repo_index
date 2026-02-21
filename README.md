# repo_index

Global index for:

- `electron-rare/Kill_LIFE`
- `electron-rare/RTC_BL_PHONE`
- `electron-rare/le-mystere-professeur-zacus`

## Workflow

- Workflow file: `.github/workflows/index.yml`
- Trigger:
  - manual (`workflow_dispatch`)
  - schedule (`0 */6 * * *`)

Each run clones the 3 repositories, regenerates repo state via
`tools/repo_state/collect.py`, and publishes:

- `index/Kill_LIFE.json`
- `index/RTC_BL_PHONE.json`
- `index/le-mystere-professeur-zacus.json`
- `index/summary.md`

Outputs are both:

- uploaded as artifact `repo-index`
- committed to `main` when changed (`chore(index): refresh repo states [skip ci]`)

## Quick links

- Summary: `index/summary.md`
- Actions: `https://github.com/electron-rare/repo_index/actions`
