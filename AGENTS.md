# Agent guide

The public website for smart-arrivals.com, served by GitHub Pages straight from this repo.
It is three hand-written HTML pages with no build step and no package manager.

## Where things go

```
index.html      Landing page
privacy.html    Privacy policy
sms-terms.html  SMS terms and conditions
CNAME           Custom domain for GitHub Pages (smart-arrivals.com)
```

- New pages are lowercase, hyphenated `.html` files in the root, with the same `<head>`
  setup (meta tags, Inter font) as the existing pages, linked from `index.html`.
- Styles and scripts stay inline in each page, as they are now. If the same block ends up
  in every page and keeps drifting, propose a shared file in a PR before adding one.
- Images and other assets go in an `assets/` folder, not the root.

## Rules

- Whatever merges to `main` is live on the public site. Always work on a branch and open
  a PR.
- Keep it build-free: no frameworks, bundlers, `package.json` or `node_modules`.
- Don't edit, rename or delete `CNAME`; it breaks the domain.
- `privacy.html` and `sms-terms.html` are legal and SMS-compliance text. Don't change
  their wording unless asked; layout and styling fixes are fine. Keep both linked from
  every page's footer.
- No tracking scripts, analytics or third-party embeds without explicit approval: they
  change what the privacy policy has to say.

## Keeping the repo organized

These rules apply to every change, whether it comes from a person, Claude Code or Codex.

- Start from an up-to-date `main`, check open PRs (`gh pr list`) so you don't redo work,
  and use a short-lived branch (`feat/...`, `fix/...`, `docs/...`).
- One concern per PR. Keep copy changes, design changes and cleanup separate.
- Keep scratch files, drafts, screenshots and notes out of the repo.
- Delete unused markup, CSS and scripts instead of commenting them out.
- Before finishing, open every changed page in a browser, click each link, check the
  console for errors, and check it at phone width. If you couldn't view it, say so.
- Use conventional commit messages (`feat:`, `fix:`, `docs:`, `chore:`) and a PR that says
  what changed and why, with a screenshot for visual changes.
- If you add a page or folder, update the list above in the same PR.
