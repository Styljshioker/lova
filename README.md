```markdown
# Lova — local chat frontend & server (free fallback)

This repository includes a lightweight chat UI and a Node server that:
- Proxies chat requests to OpenAI if OPENAI_API_KEY is set on the server (secure).
- Falls back to a local deterministic responder when OPENAI_API_KEY is not set (no charges).

Quick start (free mode)
1. Install dependencies:
   npm install

2. Run in development:
   npm run dev

3. In the chat UI, set the proxy URL to `/api/chat` (or `http://localhost:5000/api/chat`) — the server will return the free fallback responses if OPENAI_API_KEY is not set.

Enable OpenAI (secure)
1. Set OPENAI_API_KEY on the server (do not add it to client code).
2. Restart server — the /api/chat endpoint will forward to OpenAI.

Deployment
- Replit: .replit is present so you can import the repo into Replit and run it.
- Vercel / Render: connect GitHub, set environment variables (OPENAI_API_KEY if using OpenAI).
```
