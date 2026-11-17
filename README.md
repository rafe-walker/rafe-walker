# Hi, I'm Joshua

I run [IsoKron](https://isokron.ai/?utm_source=github&utm_medium=profile&utm_campaign=readme). We test what happens when AI agents write to real systems through MCP servers, and we build open tools so anyone can check their own.

Before this I spent ten years in support engineering at Ring. The worst problems were always the ones where every system said "done" and the data said otherwise. Agents bring the same problem back.

## What I've built

**The MCP Write-Safety Requirements (MWS 0.9)**: an open draft of 37 requirements for MCP servers that write data, each with a test method. Open for comment until 16 Dec 2026.
→ [isokron-ai/mcp-write-safety](https://github.com/isokron-ai/mcp-write-safety)

**mcp-writecheck**: a CLI that tests an MCP server's write tools against MWS in a test environment: two writers on one record, a retry after a lost answer, a batch that fails part-way. The same repo has **tiny-tracker**, a small server with a correct build and one switchable defect per requirement.
→ [isokron-ai/mcp-write-safety](https://github.com/isokron-ai/mcp-write-safety) · npm `@mcp-write-safety/writecheck`

**mcp-writecheck GitHub Action**: runs those checks in CI.
→ [isokron-ai/mcp-writecheck-action](https://github.com/isokron-ai/mcp-writecheck-action)

**MWS kits for TypeScript and Python**: helpers that give a write tool the result shape the spec describes.
→ [isokron-ai/mcp-write-safety-kits](https://github.com/isokron-ai/mcp-write-safety-kits)

**writesafe for Strapi**: a Strapi plugin that gives agents a write path that refuses stale edits instead of losing them.
→ [isokron-ai/strapi-plugin-writesafe](https://github.com/isokron-ai/strapi-plugin-writesafe)

## What we found

- Two agents editing one record through GitHub's MCP server: one of the two edits was lost in 19 of 30 pairs, and both agents were told it worked.
- Reading the write paths of 100 popular MCP servers from source: 15 accept an idempotency key, and 7 can say "I don't know if that write happened" in a form a program can read.

Each study has a runnable experiment repo: [GitHub](https://github.com/isokron-ai/github-mcp-writepath-experiment), [Kubernetes](https://github.com/isokron-ai/kubernetes-mcp-writepath-experiment), [PostHog](https://github.com/isokron-ai/posthog-mcp-writepath-experiment) and [Payload](https://github.com/isokron-ai/payload-mcp-writepath-experiment). Plans are written down before the runs in [preregistrations](https://github.com/isokron-ai/preregistrations).

## Contact

[isokron.ai](https://isokron.ai/?utm_source=github&utm_medium=profile&utm_campaign=readme) · [LinkedIn](https://www.linkedin.com/in/joshua-bryan-54b83144a/)
