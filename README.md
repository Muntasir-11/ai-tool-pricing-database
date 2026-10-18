# AI Tool Pricing Database

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23054247.svg)](https://doi.org/10.5281/zenodo.23054247)

Open, source-linked pricing data for AI tools, maintained by [AI Hustle World](https://aihustleworld.com), an independent publication about practical AI tools and workflows.

Most AI pricing comparisons are screenshots of a pricing page on the day someone wrote the article. This dataset is built the other way around: every row carries the URL it came from and the date it was last checked, and anything the vendor does not publish clearly is left blank instead of guessed.

**Status:** first release, v0.1.0 (2026-09-24), with 90 rows across 8 tools. The `main` branch has grown since then: Tidio and Murf were added on 2026-10-03 and 41 more tools on 2026-10-18, so it now has 422 rows across 51 tools. These will be part of the next release, and more tools are being added. Rows were read from each vendor's own pricing page by an AI assistant and run through automated checks; they were not hand-checked by a person one by one. Read [METHODOLOGY.md](METHODOLOGY.md) before relying on any figure.

**Also available on:** [Kaggle](https://www.kaggle.com/datasets/aihustleworld/ai-tool-pricing-database) · [Zenodo](https://doi.org/10.5281/zenodo.23054247) (archived releases with DOIs). This GitHub repository is the canonical source; the copies mirror its releases.

**Listed in:** [Awesome Public Datasets](https://github.com/awesomedata/awesome-public-datasets#economics) (Economics).

## What is in this repository

| File | What it is |
|---|---|
| [`data/tool_pricing.csv`](data/tool_pricing.csv) | The dataset. One row per tool, plan, billing period and credit tier. |
| [`METHODOLOGY.md`](METHODOLOGY.md) | How prices are collected, checked, calculated and marked stale, what the first release covers, and what the dataset does not claim. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to report a wrong or outdated price. |
| [`SECURITY.md`](SECURITY.md) | How to report tampered data or a repository security problem privately. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | How to behave in issues, pull requests and discussions. |
| [`CITATION.cff`](CITATION.cff) | Machine-readable citation details (GitHub shows a "Cite this repository" button from this file). |
| [`LICENSE`](LICENSE) | CC BY 4.0 (the official legal text). |

## Tools covered in v0.1.0

**Affiliate disclosure:** the links in the last column are affiliate links. If you sign up through one, AI Hustle World may earn a commission at no extra cost to you. They do not change what a row says: every price is read from the vendor's own page in the Source page column, and the affiliate links are kept out of the data file.

| Tool | Source page | Rows | Affiliate link |
|---|---|---|---|
| ElevenLabs (Creative plans) | <https://elevenlabs.io/pricing> | 12 | [ElevenLabs (affiliate link)](https://try.elevenlabs.io/yh2xrua7zq9x) |
| OpusClip | <https://www.opus.pro/pricing> | 5 | none |
| Descript | <https://www.descript.com/pricing> | 8 | none |
| AdCreative.ai | <https://www.adcreative.ai/#new-pricing-section> | 30 | [AdCreative.ai (affiliate link)](https://free-trial.adcreative.ai/w3gpiv0v8iiw) |
| Intercom helpdesk and Fin AI Agent | <https://www.intercom.com/pricing> | 9 | none |
| Captions | <https://captions.ai/pricing> | 8 | none |
| Chatbase | <https://www.chatbase.co/pricing> | 9 | [Chatbase (affiliate link)](https://link.chatbase.co/muntasir-ahmad-chowdhury) |
| Weav | <https://weav.com/pricing> | 9 | [Weav (affiliate link)](https://go.weav.com/muntasir-ahmad-chowdhury) |
| Tidio | <https://www.tidio.com/pricing/> | 11 | [Tidio (affiliate link)](https://affiliate.tidio.com/2ll7vttz9s4o) |
| Murf (Studio plans) | <https://murf.ai/pricing> | 6 | [Murf (affiliate link)](https://get.murf.ai/0k1qozd4inx6) |
| Adobe Express | <https://www.adobe.com/express/pricing> | 5 | none |
| Adobe Firefly | <https://www.adobe.com/products/firefly/plans.html> | 9 | none |
| Ahrefs | <https://ahrefs.com/pricing> | 13 | none |
| Algolia | <https://www.algolia.com/pricing> | 4 | none |
| Apollo.io | <https://www.apollo.io/pricing> | 7 | none |
| Buffer | <https://buffer.com/pricing> | 5 | none |
| Canva | <https://www.canva.com/pricing/?countryCode=us> | 6 | none |
| Cartesia | <https://cartesia.ai/pricing> | 5 | none |
| ChatGPT | <https://chatgpt.com/pricing> | 11 | none |
| Claude | <https://claude.com/pricing> | 12 | none |
| Clay | <https://www.clay.com/pricing> | 6 | none |
| Cursor | <https://cursor.com/pricing> | 9 | none |
| DeepL | <https://www.deepl.com/en/pro> | 8 | none |
| Fathom | <https://www.fathom.ai/pricing> | 8 | none |
| Fireflies.ai | <https://fireflies.ai/pricing> | 6 | none |
| Gamma | <https://gamma.app/pricing> | 9 | none |
| Gemini | <https://gemini.google/subscriptions/> | 7 | none |
| GitHub Copilot | <https://github.com/features/copilot/plans> | 6 | none |
| Gorgias | <https://www.gorgias.com/pricing> | 8 | none |
| Grammarly | <https://www.grammarly.com/plans> | 5 | none |
| Granola | <https://www.granola.ai/pricing> | 3 | none |
| Hootsuite | <https://www.hootsuite.com/plans> | 7 | none |
| HubSpot | <https://www.hubspot.com/pricing/suite> | 12 | none |
| InVideo AI | <https://invideo.io/pricing> | 12 | none |
| Jasper | <https://www.jasper.ai/pricing> | 3 | none |
| Krisp | <https://krisp.ai/pricing/> | 8 | none |
| Microsoft Copilot | <https://www.microsoft.com/en-us/copilot/pricing/individuals> | 15 | none |
| NotebookLM | <https://support.google.com/gemininotebook/answer/16213268?hl=en> | 6 | none |
| Notion AI | <https://www.notion.com/pricing> | 7 | none |
| Otter.ai | <https://otter.ai/pricing> | 6 | none |
| Perplexity | <https://www.perplexity.ai/enterprise/pricing> | 11 | none |
| Pictory | <https://pictory.ai/pricing> | 7 | none |
| Predis.ai | <https://predis.ai/pricing/> | 6 | none |
| Read AI | <https://www.read.ai/plans-pricing> | 7 | none |
| Runway | <https://runway.com/pricing> | 10 | none |
| Semrush | <https://www.semrush.com/pricing/seo-ai-search/> | 9 | none |
| Shopify | <https://www.shopify.com/pricing> | 7 | none |
| Speechify | <https://speechify.com/pricing/> | 3 | none |
| Surfer SEO | <https://surferseo.com/pricing/> | 11 | none |
| Writesonic | <https://writesonic.com/pricing> | 10 | none |
| Zapier | <https://zapier.com/pricing> | 6 | none |

The first release follows the tools AI Hustle World has already written about. That is why the affiliate column exists: see [section 6 of the methodology](METHODOLOGY.md#6-independence). Tidio and Murf were added on 2026-10-03 and 41 more tools on 2026-10-18, after the v0.1.0 release. Every tool in this table is covered in at least one AI Hustle World article.

## Reading a row

- `verified_date` is the last day the source page was read and the row confirmed. It is the most important column. A price with an old date is a lead, not a fact. Treat any row older than 90 days as stale.
- `verified_by` is `ai-assisted` unless a person has personally checked that row, in which case it says `maintainer`.
- `status` is `verified`, `not_published`, `unclear` or `stale`. Rows are never silently deleted when a vendor changes a price; the old row is marked `stale` and a new row is added.
- Blank price fields mean the vendor did not publish a clear price for that plan. That is information, not a gap to fill.
- For `annual` and `quarterly` rows, `price_amount` is the monthly equivalent the vendor displays. `price_notes` gives the billed total when the page states it.
- `cost_per_unit` is calculated only for a unit the vendor itself defines, such as a credit or an outcome. The formula is written in `cost_per_unit_basis` so you can check the arithmetic yourself. It never converts credits into minutes, videos or messages.
- `maintainer_affiliate` says whether AI Hustle World has an affiliate or referral link with that vendor.

## What this dataset is not

- It is not real-time. Vendors change prices without notice, so always confirm on the vendor's own page before you buy.
- It is not a ranking or a recommendation. It records published prices and limits, nothing about output quality.
- It is not based on buying or testing plans unless a row's `notes` column says so explicitly. Prices are read from public vendor sources.
- It is not hand-verified row by row. An AI assistant can misread a page or miss a plan hidden behind a selector, so treat the source link as the authority and report mistakes.
- The data file contains no affiliate links. `source_url` always points to the vendor's own page, with no tracking parameters. The only affiliate links in this repository are the labeled ones in the coverage table above.

## Using and citing the data

The data is released under [CC BY 4.0](LICENSE): you may copy, share and build on it, including commercially, as long as you credit the source. A suitable credit is:

> AI Tool Pricing Database, AI Hustle World (https://aihustleworld.com), CC BY 4.0. Check the `verified_date` of each row you use.

Use the "Cite this repository" button on GitHub for a formatted citation.

Each release is archived on Zenodo. To cite the dataset in general, use DOI [10.5281/zenodo.23054247](https://doi.org/10.5281/zenodo.23054247), which always resolves to the latest version. To cite the exact data you used, use that release's own DOI; v0.1.0 is [10.5281/zenodo.23054248](https://doi.org/10.5281/zenodo.23054248).

## Reporting a problem

Found a price that changed, a broken source link or a wrong calculation? Open an issue using the **Price correction** template, or read [CONTRIBUTING.md](CONTRIBUTING.md). Corrections are reviewed against the vendor's own page.

## AI Hustle World articles on these tools

These are the AI Hustle World articles that review or compare the tools in this dataset. They add context the data file cannot, such as who each tool fits and where it falls short. Articles are written on their own dates, so if a price in an article differs from a row here, trust the row with the later `verified_date` and confirm on the vendor's page.

| Tool | Articles |
|---|---|
| ElevenLabs | [ElevenLabs Review 2026](https://aihustleworld.com/2026/08/elevenlabs-review.html) · [ElevenLabs vs Alternatives](https://aihustleworld.com/2026/08/elevenlabs-vs-alternatives.html) |
| OpusClip, Descript, Captions | [OpusClip vs Descript vs Captions](https://aihustleworld.com/2026/09/opusclip-vs-descript-vs-captions.html) · [AI Video Clipping Tools: Cost Per Minute](https://aihustleworld.com/2026/09/ai-video-clipping-tools.html) |
| AdCreative.ai | [AdCreative.ai Pricing](https://aihustleworld.com/2026/08/adcreative-ai-pricing.html) · [AdCreative.ai Review](https://aihustleworld.com/2026/08/adcreative-ai-review.html) · [AdCreative.ai Free Trial](https://aihustleworld.com/2026/08/adcreative-ai-free-trial.html) |
| Intercom Fin | [Weav vs Intercom Fin](https://aihustleworld.com/2026/09/weav-vs-intercom-fin.html) |
| Chatbase | [Weav vs Chatbase](https://aihustleworld.com/2026/09/weav-vs-chatbase.html) |
| Weav | [Weav Pricing Explained](https://aihustleworld.com/2026/09/weav-pricing-explained.html) · [Weav Review 2026](https://aihustleworld.com/2026/09/weav-review.html) |
| Tidio | [Best AI E-Commerce Tools](https://aihustleworld.com/2026/09/best-ai-e-commerce-tools.html) · [Best AI Customer Service Tools](https://aihustleworld.com/2026/07/best-ai-customer-service-tools-in-2026-free-paid-top-10-compared.html) |
| Murf | [ElevenLabs vs Alternatives](https://aihustleworld.com/2026/08/elevenlabs-vs-alternatives.html) · [Best AI Voice Generators](https://aihustleworld.com/2026/07/best-ai-voice-generators-in-2026.html) |
| Adobe Express | [Best AI Tools for Pinterest Content Creation](https://aihustleworld.com/2026/08/best-ai-tools-for-pinterest-content-creation.html) |
| Adobe Firefly | [Best AI Video Generators (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-video-generators-free-paid-top-10-tools-compared.html) |
| Ahrefs | [Best AI SEO Tools in 2026: 10 Tools Compared](https://aihustleworld.com/2026/08/best-ai-seo-tools-in-2026-10-tools-compared.html) |
| Algolia | [10 Best AI E-Commerce Tools for Content & Support (2026)](https://aihustleworld.com/2026/09/best-ai-e-commerce-tools.html) |
| Apollo.io | [Best AI Lead Generation Tools in 2026: 8 Platforms Compared](https://aihustleworld.com/2026/08/best-ai-lead-generation-tools-in-2026-8-platforms-compared-by-use-case.html) |
| Buffer | [Best AI Tools for Pinterest Content Creation](https://aihustleworld.com/2026/08/best-ai-tools-for-pinterest-content-creation.html) |
| Canva | [Best AI Tools for Pinterest Content Creation](https://aihustleworld.com/2026/08/best-ai-tools-for-pinterest-content-creation.html) |
| Cartesia | [ElevenLabs vs Alternatives 2026: Same Script Tested in 3 Tools](https://aihustleworld.com/2026/08/elevenlabs-vs-alternatives.html) |
| ChatGPT | [Best AI Translation Tools (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-translation-tools-free-paid-top-10-tools-compared.html) |
| Claude | [Cursor vs GitHub Copilot vs Claude Code: Which to Choose?](https://aihustleworld.com/2026/10/cursor-vs-github-copilot-vs-claude-code.html) |
| Clay | [Best AI Lead Generation Tools in 2026: 8 Platforms Compared](https://aihustleworld.com/2026/08/best-ai-lead-generation-tools-in-2026-8-platforms-compared-by-use-case.html) |
| Cursor | [Cursor vs GitHub Copilot vs Claude Code: Which to Choose?](https://aihustleworld.com/2026/10/cursor-vs-github-copilot-vs-claude-code.html) |
| DeepL | [Best AI Translation Tools (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-translation-tools-free-paid-top-10-tools-compared.html) |
| Fathom | [Best AI Meeting Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-meeting-assistants-free-paid.html) |
| Fireflies.ai | [Best AI Meeting Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-meeting-assistants-free-paid.html) |
| Gamma | [Best AI Tools to Create and Sell Digital Products in 2026](https://aihustleworld.com/2026/07/best-ai-tools-to-create-and-sell-digital-products-complete-guide.html) |
| Gemini | [Best AI Research Assistants (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-research-assistants-free-paid-top-10-tools-compared.html) |
| GitHub Copilot | [Best AI Coding Assistants (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-coding-assistants-free-paid-top-10-tools-compared.html) |
| Gorgias | [10 Best AI E-Commerce Tools for Content & Support (2026)](https://aihustleworld.com/2026/09/best-ai-e-commerce-tools.html) |
| Grammarly | [Best AI Tools for Beginners in 2026 (Free & Paid)](https://aihustleworld.com/2026/07/best-ai-tools-for-beginners-in-2026-free-paid.html) |
| Granola | [Best AI Meeting Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-meeting-assistants-free-paid.html) |
| Hootsuite | [Best AI Tools for Creating Social Media Content (Free & Paid)](https://aihustleworld.com/2026/07/best-ai-tools-for-creating-social-media-content-free-paid.html) |
| HubSpot | [Best AI Lead Generation Tools in 2026: 8 Platforms Compared](https://aihustleworld.com/2026/08/best-ai-lead-generation-tools-in-2026-8-platforms-compared-by-use-case.html) |
| InVideo AI | [Best AI Video Generators (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-video-generators-free-paid-top-10-tools-compared.html) |
| Jasper | [Best AI Writing Tools in 2026: Free & Paid Picks](https://aihustleworld.com/2026/07/best-ai-writing-tools-in-2026-free-paid-top-10-picks.html) |
| Krisp | [Best AI Meeting Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-meeting-assistants-free-paid.html) |
| Microsoft Copilot | [Best AI Email Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-email-assistants-free-paid.html) |
| NotebookLM | [Best AI Tools for Beginners in 2026 (Free & Paid)](https://aihustleworld.com/2026/07/best-ai-tools-for-beginners-in-2026-free-paid.html) |
| Notion AI | [Best AI Tools for Beginners in 2026 (Free & Paid)](https://aihustleworld.com/2026/07/best-ai-tools-for-beginners-in-2026-free-paid.html) |
| Otter.ai | [Best AI Meeting Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-meeting-assistants-free-paid.html) |
| Perplexity | [Best AI Tools for Beginners in 2026 (Free & Paid)](https://aihustleworld.com/2026/07/best-ai-tools-for-beginners-in-2026-free-paid.html) |
| Pictory | [8 Best AI Content Repurposing Tools in 2026](https://aihustleworld.com/2026/09/best-ai-content-repurposing-tools.html) |
| Predis.ai | [Best AI Tools for Pinterest Content Creation](https://aihustleworld.com/2026/08/best-ai-tools-for-pinterest-content-creation.html) |
| Read AI | [Best AI Meeting Assistants (Free & Paid): 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-meeting-assistants-free-paid.html) |
| Runway | [Best AI Video Generators (Free & Paid): Top 10 Tools Compared](https://aihustleworld.com/2026/07/best-ai-video-generators-free-paid-top-10-tools-compared.html) |
| Semrush | [Best AI SEO Tools in 2026: 10 Tools Compared](https://aihustleworld.com/2026/08/best-ai-seo-tools-in-2026-10-tools-compared.html) |
| Shopify | [10 Best AI E-Commerce Tools for Content & Support (2026)](https://aihustleworld.com/2026/09/best-ai-e-commerce-tools.html) |
| Speechify | [ElevenLabs vs Alternatives 2026: Same Script Tested in 3 Tools](https://aihustleworld.com/2026/08/elevenlabs-vs-alternatives.html) |
| Surfer SEO | [Best AI SEO Tools in 2026: 10 Tools Compared](https://aihustleworld.com/2026/08/best-ai-seo-tools-in-2026-10-tools-compared.html) |
| Writesonic | [Best AI SEO Tools in 2026: 10 Tools Compared](https://aihustleworld.com/2026/08/best-ai-seo-tools-in-2026-10-tools-compared.html) |
| Zapier | [Best AI Workflow Automation Tools (Free & Paid)](https://aihustleworld.com/2026/07/best-ai-workflow-automation-tools-free-paid.html) |

## Related

- Full write-up and context: <https://aihustleworld.com/ai-tool-pricing-database>
- How AI Hustle World researches and tests tools: <https://aihustleworld.com/research-methodology>
- Corrections policy: <https://aihustleworld.com/corrections-policy>

Maintained by [Muntasir Ahmad Chowdhury](https://github.com/Muntasir-11).
