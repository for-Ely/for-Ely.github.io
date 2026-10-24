# Nguyễn Sỹ Quân — Portfolio

An English, responsive portfolio built with HTML and CSS. No JavaScript, dependencies, external fonts, tracking, or build step. Public contact is GitHub only. The source CV is deliberately not included.

## Preview locally

From this folder, run:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000. Stop the server with Ctrl+C when finished. You can also open `index.html` directly.

## Publish with GitHub Pages

1. Sign into your GitHub account **for-Ely**.
2. Create a public repository named **for-Ely.github.io**. If it already exists, review its contents before changing anything; do not overwrite an existing site accidentally. Alternatively, use a new repository such as `portfolio`, which publishes at https://for-Ely.github.io/portfolio/.
3. Upload `index.html`, `styles.css`, and optionally this README to the repository root on the `main` branch. Do not upload your CV or private documents.
4. In **Settings → Pages → Build and deployment**, select **Deploy from a branch**, then **main** and **/(root)**, and save.
5. Wait for the Pages deployment to complete. Verify the public site at https://for-Ely.github.io/ (or the project URL above) on desktop and mobile. All stylesheet paths are relative, so either setup works.
6. Confirm the biography and education are accurate before sharing. The page says studies started in 2022 rather than assuming a current enrollment or graduation status.

## Request sy.is-a.dev yourself

The site must be published and reasonably complete before applying. is-a.dev is a free subdomain service, not hosting. Personal portfolios must relate to software development and be noncommercial. Acceptance is determined by volunteer maintainers.

**The is-a.dev README asks applicants not to use AI to generate their registration requests. Write and submit the DNS file and PR yourself using the official instructions. This project deliberately does not include a registration JSON or submit a PR.**

1. Read the [quickstart](https://docs.is-a.dev/quickstart/), [terms](https://is-a.dev/terms), [GitHub Pages guide](https://docs.is-a.dev/guides/github-pages/), and [domain structure](https://docs.is-a.dev/domain-structure/).
2. Check whether `domains/sy.json` exists in the [registration repository](https://github.com/is-a-dev/register/tree/main/domains). Also check [open PRs mentioning sy](https://github.com/is-a-dev/register/pulls?q=is%3Apr+is%3Aopen+sy). A missing file does not reserve the name or guarantee availability or approval.
3. Fork that repository. Following the official guide, manually create the registration file for `sy` with your GitHub username and the DNS record appropriate to GitHub Pages. The DNS CNAME target is a hostname, not a full URL or a project path. Use the guide's exact requirements rather than guessing.
4. Open a PR, fill in its template yourself, and provide your working portfolio URL. Check back for requested changes. No review deadline is guaranteed.
5. **Only after your registration PR is merged**, open your website repository's **Settings → Pages → Custom domain**, enter `sy.is-a.dev`, and save. The official GitHub Pages guide explicitly requires this order. Before this step, keep the standard Pages address working for review.
6. Wait for the DNS and certificate checks, and enable **Enforce HTTPS** when available. Test https://sy.is-a.dev and its stylesheet. Optionally follow the official guide's domain-verification instructions to verify ownership through a separate TXT-record request you author yourself.

### Two different CNAME concepts

- **is-a.dev DNS CNAME record:** managed through the registration repository, pointing the subdomain to your hosting hostname.
- **GitHub Pages `CNAME` file:** lives in your website repository and contains the custom domain. GitHub normally creates it when saving the Pages custom-domain setting. It does not register a name or configure is-a.dev DNS.

No `CNAME` file is committed here yet, so the portfolio can be previewed on the standard GitHub Pages address without prematurely redirecting to an unapproved name.

DNS changes or domain removal later require another PR to is-a.dev. NS delegation is restricted and is not needed for this portfolio.
