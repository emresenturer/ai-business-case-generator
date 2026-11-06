# AI Business Case Generator

AI system that transforms product ideas into structured business cases.

**Live:** https://emresenturer.github.io/ai-business-case-generator/

## What it does

Enter a product idea, target customer, problem, industry, and company stage (idea, startup, or enterprise), plus optional team size and budget range in your own words. The tool asks Claude for a structured JSON business case and renders it as a clean document with section navigation:

1. Executive summary
2. Problem and opportunity
3. Solution
4. Target market and sizing (TAM / SAM / SOM **method**, with every input labeled as an assumption)
5. Competitive landscape (categories, with a reminder to verify any names)
6. Business model options
7. Cost and resource estimate (ranges, assumptions labeled)
8. Risks and mitigations
9. KPIs
10. 90-day plan
11. Recommendation: **Go**, **Test first**, or **No-go**, with reasons

Export the case as a Markdown download, copy it as Markdown, or use **Print / PDF** (a dedicated print stylesheet hides the app and keeps the document). A **Load sample idea** button fills in an example.

### Honesty by design

The model is instructed never to present invented figures as data. Market sizing is a formula plus labeled assumptions and pointers to where real numbers can be found. Competitor names, if any, come with a note to verify them. Treat the output as a structured first draft, not financial advice.

## Privacy

- Your inputs go from your browser directly to `api.anthropic.com`. Nothing is sent anywhere else and nothing is stored on a server.
- Your Anthropic API key is saved only in this browser's `localStorage` (`ai-business-case-generator_anthropic_key`). **Forget** removes it.

## Bring your own key

Get an Anthropic API key at https://console.anthropic.com/settings/keys. Usage is billed to your own Anthropic account. The app calls the Messages API with model `claude-opus-5-5`.

## Run locally

```bash
git clone https://github.com/emresenturer/ai-business-case-generator.git
cd ai-business-case-generator
python3 -m http.server 8000
# open http://localhost:8000
```

## Stack

A single `index.html`: plain HTML, CSS, and JavaScript. No build step, no dependencies, no framework. Fonts from Google Fonts. Deployed with GitHub Pages from `main` (root).

## License

MIT, Emre Senturer, 2026.
