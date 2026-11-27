# Yusufhan Sacak

AI Platform Engineer at [rubica](https://www.rubica.au/). I work on LLM and MCP infrastructure, and on application and supply-chain security, for a regulated Australian financial-advice platform. I built the platform's core end to end: multi-provider chat (AWS Bedrock, native Anthropic, Google, OpenAI), a Model Context Protocol (MCP) connector fleet, and the security posture that runs them.

Background in Cyber Security and Computer Engineering. Mostly TypeScript on Node.js and Next.js, with the Anthropic SDK on the platform side.

→ [yusufhan.dev](https://yusufhan.dev) · [/now](https://yusufhan.dev/now) · [linkedin](https://www.linkedin.com/in/yusufhansacak/) · [x](https://twitter.com/0xSCK)

---

## Open source

- [**vercel-seo-audit**](https://github.com/JosephDoUrden/vercel-seo-audit): CLI and GitHub Action that audits Next.js and Vercel deploys for SEO and indexing failures. The October 2026 releases added a check for metadata streamed into the body, plus `--only` and `--ignore`. Published on npm.
- [**nextjs-seo-audit-mcp**](https://github.com/JosephDoUrden/nextjs-seo-audit-mcp): Read-only MCP server that audits a deployed Next.js or Vercel site for SEO and indexing problems, from what it serves. Published on npm.
- [**webhook-hmac-kit**](https://github.com/JosephDoUrden/webhook-hmac-kit): Verify and sign Standard Webhooks over the raw bytes, plus its own format with nonce replay protection. Web Crypto only, no runtime dependencies. 2.2.0 added a test-vector corpus (`npx webhook-hmac-kit vectors`) and 2.3.0 a Web Request adapter and Hono middleware.
- [**clean-repo-standard**](https://github.com/JosephDoUrden/clean-repo-standard): Production-safe GitHub repo template: branch protection, CI, PR templates, signed commits.

## Merged upstream

**modelcontextprotocol/registry**
- [#1734](https://github.com/modelcontextprotocol/registry/pull/1734) feat(publisher): read the login private key from a file or MCP_PRIVATE_KEY
- [#1583](https://github.com/modelcontextprotocol/registry/pull/1583) fix(validators): reject invalid argument types and empty positional arguments
- [#1457](https://github.com/modelcontextprotocol/registry/pull/1457) fix(publisher): pad ECDSA P-384 signature to fixed width
- [#1588](https://github.com/modelcontextprotocol/registry/pull/1588) fix(publisher): tolerate transient device-flow failures during login polling
- [#1436](https://github.com/modelcontextprotocol/registry/pull/1436) fix(api): allow PATCH in CORS so browsers can call the status endpoints
- [#1145](https://github.com/modelcontextprotocol/registry/pull/1145) feat(publisher): copy version from package.json and prefer mcpName in init
- [#1149](https://github.com/modelcontextprotocol/registry/pull/1149) fix(publisher): omit repository when URL cannot be detected

**modelcontextprotocol/typescript-sdk** · **conformance** · **servers**
- [typescript-sdk#1875](https://github.com/modelcontextprotocol/typescript-sdk/pull/1875) feat(client): support custom claims in PrivateKeyJwtProvider
- [conformance#476](https://github.com/modelcontextprotocol/conformance/pull/476) fix(http-base): return valid empty results for unhandled list methods
- [servers#3893](https://github.com/modelcontextprotocol/servers/pull/3893) fix(memory): resolve Vitest false positive for expected rejection

**dexidp/dex**
- [#5162](https://github.com/dexidp/dex/pull/5162) fix(api): require a username in CreatePassword
- [#5163](https://github.com/dexidp/dex/pull/5163) fix(storage/ent): store an unset blocked_until as NULL
- [#5133](https://github.com/dexidp/dex/pull/5133) fix(tokens): undo the refresh claim when the offline session update fails

**getsentry/sentry-javascript**
- [#24233](https://github.com/getsentry/sentry-javascript/pull/24233) feat(bun): Capture Bun.serve request bodies with `maxRequestBodySize`
- [#24070](https://github.com/getsentry/sentry-javascript/pull/24070) fix(deno): Gate tracing integrations on hasSpansEnabled
- [#24030](https://github.com/getsentry/sentry-javascript/pull/24030) fix(deno): Don't throw in Deno.serve wrapper when no client is bound

**Elsewhere**
- [cloudflare/workerd#6040](https://github.com/cloudflare/workerd/pull/6040) Add TextDecoder support for x-user-defined encoding (fixes #6039)
- [aws/aws-sdk-js-v3#8281](https://github.com/aws/aws-sdk-js-v3/pull/8281) fix(credential-provider-node): handle passive credential refresh rejection
- [rjsf-team/react-jsonschema-form#5044](https://github.com/rjsf-team/react-jsonschema-form/pull/5044) fix(`@rjsf/core`): prevent extraErrors duplication on array field mutation (#5041)
- [cased/kit#189](https://github.com/cased/kit/pull/189) fix: don't post non-actionable errors as GitHub review comments
- [CodeWithCJ/SparkyFitness#621](https://github.com/CodeWithCJ/SparkyFitness/pull/621) fix(health-data): apply default units for HealthConnect sync (fixes #567)

## Security

- **[CVE-2026-44429](https://github.com/advisories/GHSA-rqv2-m695-f8j4)**: Stored XSS in the catalogue UI of the official Model Context Protocol Registry, through a publisher-controlled `websiteUrl`. Sole credited reporter. Fixed by the maintainers in 1.7.7, published 08 May 2026.
- **[CVE-2026-104850](https://github.com/advisories/GHSA-6qxp-vccf-f47h)**: MCP TypeScript SDK, High 7.5. The client sent stored OAuth credentials to whichever authorisation server the MCP server named. One of 7 credited reporters. Fixed in `@modelcontextprotocol/sdk` 1.31.0, published 06 Oct 2026.
- **[GHSA-8w82-h3w4-62r5](https://github.com/twentyhq/twenty/security/advisories/GHSA-8w82-h3w4-62r5)**: Twenty CRM, no CVE. A user allowed to manage members but not roles could invite an account straight into the Admin role. One of 4 credited reporters. Fixed in 2.47.0, published 19 Oct 2026.
- **[GHSA-rxhc-fwc2-57jq](https://github.com/modelcontextprotocol/registry/security/advisories/GHSA-rxhc-fwc2-57jq)**: MCP Registry, Low, no CVE. Generic OIDC authentication could panic when an extra-claim rule and the token claim were both lists. One of 2 credited reporters. Fixed in 1.7.7, published 27 Nov 2026.
- **Langfuse**: Revoked API keys could keep authenticating because of a cache invalidation ordering race. Fixed in [langfuse/langfuse#17651](https://github.com/langfuse/langfuse/pull/17651) and listed in the [Langfuse security Hall of Fame](https://langfuse.com/security/responsible-disclosure).

Full list: [yusufhan.dev/security](https://yusufhan.dev/security)

## Writing

The [Lessons series](https://yusufhan.dev/blog): long-form essays on production AI systems, MCP, LLM infrastructure and security engineering.

Write-ups: [CVE-2026-44429](https://yusufhan.dev/blog/cve-2026-44429-stored-xss-mcp-registry) · [CVE-2026-104850](https://yusufhan.dev/blog/cve-2026-104850-mcp-typescript-sdk-oauth-credentials) · [two bodies, one valid webhook signature](https://yusufhan.dev/blog/two-bodies-one-valid-webhook-signature)
