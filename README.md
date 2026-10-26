# Centsless developer documentation

Source for https://docs.centsless.org, built on Mintlify.

- `docs.json` is the site configuration (navigation, branding, API playground).
- Pages are MDX files with YAML frontmatter. Folders: `concepts/`, `guides/`, `reference/`, `api-reference/`.
- `openapi.yaml` is the API document. The API Reference tab is generated from it; it is also the file to import into Postman.
- `logo/` and `favicon.png` are the brand assets.

## Connect this repository to Mintlify (one time)

1. Push this folder to a GitHub repository (for example `kthatfield/centsless-docs`). Keep it private; Mintlify reads it through its GitHub app.
2. In the Mintlify dashboard (https://dashboard.mintlify.com), open **Settings > Git Settings** (or **Organization > GitHub app** on first run), install the Mintlify GitHub app on your GitHub account, and grant it access to the repository.
3. Back in the dashboard, select the repository and the default branch, and leave the docs root as `/` (the folder that holds `docs.json`).
4. The first deployment builds within a minute or two and is served at `https://<project>.mintlify.site`. Check it before changing DNS.
5. **Custom domain:** Settings > Domain Setup > enter `docs.centsless.org`. Mintlify shows a CNAME target. In GoDaddy DNS for `centsless.org`, edit the existing `docs` CNAME record to that target (TTL 600). Mintlify issues the certificate automatically once the record resolves.
6. Retire the old site: in the old Mintlify account, delete the deployment (Settings > Delete project) and make the old repository `kthatfield/CentslessAPIdocs` private or archive it, so stale pages stop being served and indexed.

After that, every push to the default branch deploys. The Mintlify connector in claude.ai can edit pages directly once the project exists.

## Local preview

```
npm i -g mint
mint dev
```

Opens http://localhost:3000. `mint broken-links` checks links; `mint validate` checks the build.

## Writing rules

No em dashes, no exclamation points, no contractions, no buzzwords. Centsless is one word. Records are "tamper-evident", never "tamper-proof" or "immutable". No patent claims. Every statutory statement names its primary source. See `AGENTS.md`.
