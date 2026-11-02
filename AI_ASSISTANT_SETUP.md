# SIVORA GROUP — Website Assistant

## Pages supported
`index.html`, `multimedia.html`, `trendz.html`, `farming.html`, and `contact.html` all load the same floating assistant from `sivora-assistant.js` and `sivora-assistant.css`.

## Static deployment (your existing GitHub → Render Static Site)
Upload **all files**, especially `sivora-knowledge.json`, `sivora-assistant.js`, and `sivora-assistant.css`, in the repository root. Publish as usual. The assistant works in **website knowledge mode** with matching SIVORA business information, links to source pages and a contact handoff. This mode does **not** call an AI model, send leads, book appointments, process orders or perform automations.

## Conversational AI mode (optional)
The included `server.js` is a minimal Node.js server that serves the same website and offers `/api/assistant`. It uses an OpenAI API key stored **only on the server**.

1. Create a Render **Web Service** from the repository (rather than a Static Site), using Node.js 20+.
2. Set start command: `node server.js`. No npm dependencies are needed.
3. Set environment variable `OPENAI_API_KEY` to your private API key in Render's environment settings. Optionally set `OPENAI_MODEL` to a model available to your API account (default in code: `gpt-4.1-mini`). Never commit `.env` or your key.
4. Deploy and visit the Web Service URL. The chat widget automatically uses the same-origin `/api/assistant` endpoint, and falls back to website knowledge mode if unavailable.
5. To keep your current Render Static Site URL, either point the domain at the new Web Service or configure a secure proxy for `/api/assistant` to the Web Service. Without that, the static site stays in website knowledge mode.

### What the assistant knows
`sivora-knowledge.json` includes curated user-provided details and extracted visible website text from all five pages. Update it when you change pricing, contact details or product availability. **Prices and availability are not live.**

### Customer support, lead generation and automation
The assistant can answer questions, explain services and suggest contacting SIVORA. It does not collect or store customer details, submit forms, create CRM leads, send WhatsApp messages or automate workflows. Those features require a separately authorized backend/CRM integration and privacy/consent design.

### Safety and production notes
Server-side requests have a basic per-IP rate limit, request-size limits, bounded history and a knowledge-grounding instruction. For high-traffic production, add persistent rate limiting, monitoring, abuse protection, privacy policy and proper logging/redaction. The browser-side fallback is keyword retrieval, not a generative model. API usage may incur charges.
