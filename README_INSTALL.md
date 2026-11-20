# SIVORA GROUP — Five-Division Website Upgrade (2026)

## Deliverables
- `index.html`: A **new standalone 5-division homepage** with all 5 logos, animated orbit, 5 service cards and SIVORA AI Assistant in website-knowledge mode.
- `fitverse.html`: Five discipline cards, independent JS **Explore Options** panels, searchable 40 full programmes, downloadable original master catalogue, and assistant.
- `divyam.html`: 18 spiritual wing cards, independent Explore Options panels, searchable **108 programmes in English and Tamil**, original document downloads, philosophy preserved, and assistant.
- `contact.html`: All five divisions, three original SIVORA GROUP contact numbers, shared address, assistant, and proposed-division notices.
- Shared CSS/JS: `sivora-five.css`, `sivora-common.js`, `sivora-program-explore.js`, `sivora-ai-assistant.css`, `sivora-ai-assistant.js`.
- `assets/fitverse.png` and `assets/divyam.png`: **Original provided designs**, in high-resolution PNG format (2048 px), not redrawn.
- `documents/`: Four DIVYAM documents and the FITVERSE master Word and PDF catalogues.
- `sivora-index-integration.js`: A **safer integration path** for the current elaborate original `index.html`, which is already ~6.57 MB with its own art, services and embedded AI assistant.

## Important — choosing your homepage approach
### RECOMMENDED: Preserve your current production `index.html`
1. Upload the new `assets/`, `documents/`, all new HTML pages, CSS and JS to your GitHub website repository root. Do **not** overwrite `assets/multimedia.png`, `assets/trendz.png` or `assets/farming.png`. Keep the existing `multimedia.html`, `trendz.html` and `farming.html`.
2. In your **existing** `index.html`, add this one line before `</body>`:
   `<script src="sivora-index-integration.js" defer></script>`
   This keeps the existing content, three original venture cards and embedded assistant, while adding the two new venture cards, 5-logo hero animation and new navigation links.
3. Upload the updated `contact.html` and the two programme HTML files and shared assets.
4. Commit, trigger Render Static Site deployment, and verify each page.

### ALTERNATIVE: Replace the existing homepage
You can instead upload the enclosed `index.html` as the new clean five-division homepage. This **replaces** the very large current homepage and its legacy design and is not the recommended route unless you specifically want a redesign. The two new logo files are bundled; the three existing logos are referenced at `assets/multimedia.png`, `assets/trendz.png`, `assets/farming.png` and must remain in the repository.

## AI Assistant capabilities
The new assistant provides a client-side website FAQ and keyword matching for services, programmes, divisions, prices and contact details. It is not a live LLM, does not contact a backend, submit enquiries, store chat logs, claim confirmed admission or collect private data. A true generative model requires a separately deployed secure server/API, never API keys in browser code. The original homepage and multimedia pages can retain their current embedded assistant.

## Accuracy and status
FITVERSE: 5 categories × 8 programmes = 40. DIVYAM: 18 wings × 6 programmes = 108 in both language views. All are labelled proposed. The 104-page Tamil source retains its original title even if its layout renders at a different page count in particular editors. SIVORA DIVYAM official philosophy: “உடல் • பொருள் • ஆத்மா அனைத்தும் இறைவனுக்கே”.

## Testing
Check desktop/mobile navigation, five logo image requests, reduced-motion animation preference, 5 FITVERSE Explore panels, 18 DIVYAM Explore panels in both languages, programme filtering, all file download links, contact phone/WhatsApp handoff, assistant launch and FAQ, and browser console for errors. The current user website has NOT been changed by preparing this ZIP.
