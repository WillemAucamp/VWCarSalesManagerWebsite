# VW Car Sales Manager

Static one-page landing site for **vwcarsalesmanager.lol**.

Open `index.html` locally, or view the live site after GitHub Pages + DNS are connected.

## Go live (GitHub Pages)

### 1. Merge & enable Pages

1. Merge the landing-page PR into `main`.
2. In the repo: **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. The deploy workflow (`.github/workflows/pages.yml`) will publish on every push to `main`.

### 2. DNS at your registrar

Point `vwcarsalesmanager.lol` at GitHub Pages with these **A** records:

| Type | Name | Value             |
|------|------|-------------------|
| A    | `@`  | `185.199.108.153` |
| A    | `@`  | `185.199.109.153` |
| A    | `@`  | `185.199.110.153` |
| A    | `@`  | `185.199.111.153` |

Optional `www` → apex:

| Type  | Name  | Value                   |
|-------|-------|-------------------------|
| CNAME | `www` | `vwcarsalesmanager.lol` |

Or point `www` at `willemaucamp.github.io` if your registrar prefers that.

DNS can take a few minutes to a few hours to propagate. In **Settings → Pages**, confirm the custom domain shows as `vwcarsalesmanager.lol` (the repo `CNAME` file sets this) and enable **Enforce HTTPS** once the certificate is ready.
