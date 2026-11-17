# Vibe Coding & AI-Powered Software Development
## Research References & Workshop Demo Plan

Companion document to `Vibe_Coding_AI_Powered_Software_Development.pptx`
Prepared for Tesha Technologies · Keynote 2026

---

## Research References

Verify all tool versions and features on the vendor pages before each delivery — this space moves monthly.

### Primary sources (vendor documentation)

- **Anthropic — Claude & Claude Code**: https://docs.anthropic.com · https://docs.claude.com/en/docs/claude-code
- **OpenAI — Codex & ChatGPT paid plans**: https://platform.openai.com/docs
- **Google — Gemini API & Gemini CLI**: https://ai.google.dev/docs
- **Mistral — Vibe agent**: https://mistral.ai/news/vibe-agent (launched May 28, 2026)
- **Cursor**: https://cursor.com
- **GitHub Copilot & Copilot Agent**: https://docs.github.com/en/copilot
- **Replit (Agent 4)**: https://replit.com
- **Lovable**: https://lovable.dev
- **Bolt.new**: https://bolt.new
- **v0 by Vercel**: https://v0.dev
- **Windsurf / Devin Desktop (Cognition)**: https://cognition.ai

### Deployment & infrastructure

- **Vercel**: https://vercel.com/docs
- **Netlify**: https://docs.netlify.com
- **Render**: https://render.com/docs
- **Railway**: https://docs.railway.app
- **Cloudflare Workers & Pages**: https://developers.cloudflare.com
- **Supabase**: https://supabase.com/docs
- **Firebase**: https://firebase.google.com/docs

### Security & best-practice guidance

- **OWASP Top 10 (2025)**: https://owasp.org/Top10
- **OWASP Top 10 for LLM Applications**: https://owasp.org/www-project-top-10-for-large-language-model-applications
- **GitHub secret scanning & Dependabot**: https://docs.github.com/en/code-security
- **Snyk — AI-generated code security**: https://snyk.io/research
- **Supabase RLS best practices**: https://supabase.com/docs/guides/database/postgres/row-level-security

### Industry commentary & background

- **Andrej Karpathy — "vibe coding" (2025 coinage)**: original X/Twitter post, Feb 2025
- **Collins Dictionary — Word of the Year 2025**: "vibe coding"
- **Model Context Protocol (MCP) — Anthropic open standard (2024)**: https://modelcontextprotocol.io
- **Zapier — Best vibe coding tools 2026**: https://zapier.com/blog/best-vibe-coding-tools
- **MarkTechPost — 15 vibe coding tools 2026 comparison**: June 2026
- **DataCamp — Vibe coding guide**: March 2026

---

## Live Demonstration Plan

Use this during the workshop that follows the keynote. The demo is **not part of the 21-slide deck** — it's the hands-on segment.

### Setup (5 minutes before you start)

1. Browser tabs open: your chosen app builder (Lovable / Bolt / Replit / v0)
2. One AI agent available: Claude Code or Cursor Agent Mode in a side window
3. GitHub account ready to receive the exported repo
4. Vercel or Netlify account ready to deploy
5. Clear browser cache so the demo starts fresh

### Project to build (matches slide 12)

**"AI-Powered Personal Finance Dashboard"** — small enough to finish in 30-45 minutes, meaningful enough to feel real.

### Demo script

**Step 1 · Initial prompt (3 min)**
Paste this into your chosen app builder:

> Build a personal finance dashboard. Users sign up with email and password. They can add transactions (amount, category, date, note), see a monthly spend chart, a category breakdown pie, and filter by date. Stack: Next.js + Tailwind + Supabase (Postgres with Row-Level Security). Add Jest tests for the API routes.

Narrate the agent's plan as it appears. Highlight the plan-first pattern — this is what separates agents from chatbots.

**Step 2 · First preview (5 min)**
Walk the audience through what the agent produced:
- Pages the agent generated
- Components it chose
- Schema it defined
- Auth it wired up

Point out what's missing or weak — don't pretend the first output is production code.

**Step 3 · Iterative refinement (10 min)**
Three follow-up prompts:
1. "Add dark mode support and a currency selector in settings."
2. "The chart should show the last 6 months, not just the current one. Also add a 'today vs. last month' comparison card at the top."
3. "Add input validation on the transaction form — amount must be positive, date can't be in the future, category required."

Each time, show the plan before accepting changes.

**Step 4 · Database check (3 min)**
Open the Supabase dashboard (or equivalent). Show the audience:
- The schema the agent created
- The RLS policies (explain what they do)
- Verify that a user can't read another user's transactions

**This is the critical moment.** Many AI-generated apps fail this test. Make the point: the UI looked fine; the backend was wide open. Always check.

**Step 5 · Tests (3 min)**
Run the test suite in the terminal. Show what passes, what fails. Ask the agent to fix a failing test live.

**Step 6 · Error recovery (3 min)**
Intentionally break something — delete a line, mistype an import. Paste the error into the agent. Watch it diagnose, propose a fix, verify.

**Step 7 · Deploy (5 min)**
- Push to GitHub (agent or manual)
- Connect GitHub repo to Vercel/Netlify
- Watch the build run
- Visit the live URL

**Step 8 · Wrap (2 min)**
- Share the live URL with the audience — ask them to sign up and try it
- Point out what you'd still fix before a real launch (performance, accessibility, edge cases, deeper security review)

### Audience engagement during the demo

- **At step 2**: "Who has an idea they'd love to see the AI try next?" — collect 2-3 pitches.
- **At step 4** (RLS check): "If I had skipped this step and shipped — what could go wrong?" — collect answers before explaining.
- **At step 7** (deploy): "What URL should I send you?" — commit on a public address.

### Fallback plan if the demo fails

Live coding fails sometimes. Have a pre-recorded 90-second screen capture ready to show if the demo won't cooperate. Then pivot:

> "This is the honest reality of building with AI — it's not magic, it's a tool. Let me show you what it looks like when it works, and then let's talk about why it sometimes doesn't."

Turn it into a teaching moment about iteration.

---

## Delivery timing (90-minute keynote)

| Segment                         | Slides   | Time         |
|---------------------------------|----------|--------------|
| Act 1 — Revolution              | 1–4      | 15 min       |
| Act 2 — Ecosystem               | 5–9      | 20 min       |
| Act 3 — Building                | 10–15    | 25 min       |
| Act 4 — Reality & roadmap       | 16–20    | 20 min       |
| Thank you / Q&A                 | 21       | 10 min       |

If running a longer workshop (half-day): follow the keynote with the live demo plan above (~45 min), then an open hack session where attendees build their own idea (~90 min) with you circulating for help.

---

## Follow-up materials to send attendees

Within 48 hours of the workshop, email:

1. A link to the deck (PDF)
2. The 7-day challenge (slide 20) as a one-pager
3. Sign-up links for the tools you demoed
4. A short list of starter prompts matching the 30 use-cases (slide 18)
5. Your contact details and office hours

Keep the energy alive while it's fresh.
