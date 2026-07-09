# UnPay Docs

Public developer documentation for the [UnPay](https://www.unpay.co) API —
Payments (Payouts), Banking (wallets & Connected Banking), and Artificial
Intelligence (AI Calling). Built with [Mintlify](https://mintlify.com).

## Structure

| Path | Contents |
|---|---|
| `docs.json` | Site config and navigation (tabs: Get started · Payments · Banking · Artificial Intelligence · API reference). |
| `index.mdx`, `quickstart.mdx`, `how-unpay-works.mdx` | Get-started pages. |
| `guides/` | Task walkthroughs (first payout, banking, first campaign, verifying webhooks). |
| `kb/` | Knowledge base / troubleshooting articles. |
| `api-reference/` | API concepts + curated pages. |
| `api-reference/openapi/payouts.yaml` | OpenAPI spec for the Payouts API. |
| `api-reference/openapi/ai-calling.yaml` | OpenAPI spec for the AI Calling API. |

The API reference pages are generated from the two OpenAPI specs. Keep those
specs in sync with the source of truth in the platform repo:

- `plugins/payouts/routes/public/payout.routes.ts` → `payouts.yaml`
- `server/routes/public-api.ts` → `ai-calling.yaml`

## Local development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) and run the dev
server from the repo root (where `docs.json` lives):

```bash
npm i -g mint
mint dev            # preview at http://localhost:3000
mint broken-links   # validate internal links before pushing
```

## Publishing

Changes deploy automatically after merging to the default branch via the
Mintlify GitHub app.
