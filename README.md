# demos.sholajegede.com

The front door for my live demos. Each demo is its own Vercel project, served
under a path on this domain through a rewrite in `vercel.json`.

| Path | Project |
| --- | --- |
| `/agent-identity` | [agent-identity-helpdesk](https://github.com/sholajegede/agent-identity-helpdesk) |

## Adding a demo

1. In the demo's project, set `NEXT_PUBLIC_BASE_PATH=/<path>` (or the framework's
   base path) so its pages and assets live under that path.
2. Add two rewrites here, one for `/<path>` and one for `/<path>/:path*`,
   pointing at the demo's `*.vercel.app` URL with the same path.
3. Add a card to `index.html`.
