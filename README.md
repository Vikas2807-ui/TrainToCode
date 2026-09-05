# train-to-code — Coding Platform Upgrade

This build upgrades Code Practice toward a HackerRank/LeetCode-style architecture.

## Included
- Topic/difficulty-aware coding problem bank across C, C++, Java, Python, JavaScript, C#, PHP, SQL, Go, Rust, Kotlin and HTML/CSS.
- Problem statement, input/output, examples, constraints and test cases.
- Run and Submit actions wired to secure server endpoints.
- Professional AI tutor panel with persistent conversation UI and full coding context.
- AI can explain, debug, review, compare approaches, analyze complexity and provide complete solutions when requested.

## Important production setup
The frontend is intentionally not given an API key.

Set these Vercel environment variables:
- `OPENAI_API_KEY` — server-side model key.
- `OPENAI_MODEL` — optional; defaults to `gpt-5.6-luna`.
- `PISTON_URL` — URL of your self-hosted Piston execution service.

Piston is used as the execution abstraction because arbitrary user code must run inside a sandbox. The public Piston API is no longer freely available as of February 15, 2026, so a self-hosted instance or authorized execution provider is required for production.

Never put an API key directly in `index.html`.
