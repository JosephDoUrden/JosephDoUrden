# Yusufhan Sacak

AI Platform Engineer at [rubica](https://www.rubica.au/) — LLM & MCP infrastructure and application & supply-chain security for a regulated Australian financial-advice platform. I built the platform's core end-to-end: multi-provider chat (AWS Bedrock, native Anthropic, Google, OpenAI), a Model Context Protocol (MCP) connector fleet, and the security posture that runs them.

Background in Cyber Security and Computer Engineering. Mostly TypeScript on Node.js and Next.js, with the Anthropic SDK on the platform side.

→ [yusufhan.dev](https://yusufhan.dev) · [/now](https://yusufhan.dev/now) · [linkedin](https://www.linkedin.com/in/yusufhansacak/) · [x](https://twitter.com/0xSCK)

---

## Open source

- [**vercel-seo-audit**](https://github.com/JosephDoUrden/vercel-seo-audit) — CLI auditing Next.js / Vercel deploys for SEO and indexing failures. Published on npm.
- [**webhook-hmac-kit**](https://github.com/JosephDoUrden/webhook-hmac-kit) — Stripe-style webhook signing without the Stripe lock-in.
- [**clean-repo-standard**](https://github.com/JosephDoUrden/clean-repo-standard) — Production-safe GitHub repo template: branch protection, CI, PR templates, verified commits.

## Merged upstream

- [`modelcontextprotocol/registry#1436`](https://github.com/modelcontextprotocol/registry/pull/1436) — fix(api): allow PATCH in CORS so browsers can call the status endpoints
- [`modelcontextprotocol/registry#1149`](https://github.com/modelcontextprotocol/registry/pull/1149) — fix(publisher): omit repository when URL cannot be detected
- [`modelcontextprotocol/registry#1145`](https://github.com/modelcontextprotocol/registry/pull/1145) — feat(publisher): copy version from package.json and prefer mcpName in init
- [`modelcontextprotocol/typescript-sdk#1875`](https://github.com/modelcontextprotocol/typescript-sdk/pull/1875) — feat(client): support custom claims in PrivateKeyJwtProvider
- [`modelcontextprotocol/servers#3893`](https://github.com/modelcontextprotocol/servers/pull/3893) — fix(memory): resolve Vitest false positive for expected rejection
- [`cloudflare/workerd#6040`](https://github.com/cloudflare/workerd/pull/6040) — Add TextDecoder support for x-user-defined encoding (fixes #6039)
- [`aws/aws-sdk-js-v3#8281`](https://github.com/aws/aws-sdk-js-v3/pull/8281) — fix(credential-provider-node): handle passive credential refresh rejection
- [`rjsf-team/react-jsonschema-form#5044`](https://github.com/rjsf-team/react-jsonschema-form/pull/5044) — fix(@rjsf/core): prevent extraErrors duplication on array field mutation (#5041)
- [`cased/kit#189`](https://github.com/cased/kit/pull/189) — fix: don't post non-actionable errors as GitHub review comments

## Security

- **[CVE-2026-44429](https://github.com/advisories/GHSA-rqv2-m695-f8j4)** — Stored XSS in the official Model Context Protocol Registry catalogue UI. Disclosed and patched, May 2026. Assigned by GitHub-as-CNA.

## Writing

The [Lessons series](https://yusufhan.dev/blog) — long-form essays on production AI systems, MCP, LLM infrastructure, and security engineering.
