# sholajegede.com/demos

The landing page for my live demos. Each demo is its own Vercel project. The
portfolio at sholajegede.com serves every demo under `/demos/<name>` through a
rewrite in its `vercel.json`, and serves this page at `/demos`.

This project also owns `demos.sholajegede.com`, which now redirects
permanently to `sholajegede.com/demos`, path included, so older links keep
working.

| Path | Project |
| --- | --- |
| `/demos/agent-identity` | [agent-identity-helpdesk](https://github.com/sholajegede/agent-identity-helpdesk) |
| `/demos/convex-sentry` | [convex-sentry](https://github.com/sholajegede/convex-sentry) |
| `/demos/convex-weflayr` | [convex-weflayr](https://github.com/sholajegede/convex-weflayr) |
| `/demos/convex-langfuse` | [convex-langfuse](https://github.com/sholajegede/convex-langfuse) |
| `/demos/convex-supermemory` | [convex-supermemory](https://github.com/sholajegede/convex-supermemory) |
| `/demos/convex-vapi` | [convex-vapi](https://github.com/sholajegede/convex-vapi) |
| `/demos/convex-livekit` | [convex-livekit](https://github.com/sholajegede/convex-livekit) |
| `/demos/convex-github` | [convex-github](https://github.com/sholajegede/convex-github) |
| `/demos/convex-linear` | [convex-linear](https://github.com/sholajegede/convex-linear) |
| `/demos/convex-paystack` | [convex-paystack](https://github.com/sholajegede/convex-paystack) |
| `/demos/convex-flutterwave` | [convex-flutterwave](https://github.com/sholajegede/convex-flutterwave) |

## Adding a demo

1. Build the demo so its pages and assets live under `/demos/<name>`. For a
   Vite app, set `base: "/demos/<name>/"` for production builds and add a
   rewrite from `/demos/<name>/:path*` to `/:path*` in its own `vercel.json`.
   For a Next.js app, set `NEXT_PUBLIC_BASE_PATH=/demos/<name>`.
2. In the portfolio's `vercel.json`, add two rewrites, one for `/demos/<name>`
   and one for `/demos/<name>/:path*`, pointing at the demo's `*.vercel.app`
   URL with the same path.
3. Add a card to `index.html` here.
