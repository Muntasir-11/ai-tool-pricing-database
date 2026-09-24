# AI Tool Pricing Database

Open, source-linked pricing data for AI tools, maintained by [AI Hustle World](https://aihustleworld.com), an independent publication about practical AI tools and workflows.

Most AI pricing comparisons are screenshots of a pricing page on the day someone wrote the article. This dataset is built the other way around: every row carries the URL it came from and the date it was last checked, and anything the vendor does not publish clearly is left blank instead of guessed.

**Status:** first release, v0.1.0 (2026-09-24). 90 rows across 8 tools. Rows were read from each vendor's own pricing page by an AI assistant and run through automated checks; they were not hand-checked by a person one by one. Read [METHODOLOGY.md](METHODOLOGY.md) before relying on any figure.

## What is in this repository

| File | What it is |
|---|---|
| [`data/tool_pricing.csv`](data/tool_pricing.csv) | The dataset. One row per tool, plan, billing period and credit tier. |
| [`METHODOLOGY.md`](METHODOLOGY.md) | How prices are collected, checked, calculated and marked stale, what the first release covers, and what the dataset does not claim. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to report a wrong or outdated price. |
| [`CITATION.cff`](CITATION.cff) | Machine-readable citation details (GitHub shows a "Cite this repository" button from this file). |
| [`LICENSE`](LICENSE) | CC BY 4.0 (the official legal text). |

## Tools covered in v0.1.0

| Tool | Source page | Rows | Affiliate link on aihustleworld.com |
|---|---|---|---|
| ElevenLabs (Creative plans) | <https://elevenlabs.io/pricing> | 12 | yes |
| OpusClip | <https://www.opus.pro/pricing> | 5 | no |
| Descript | <https://www.descript.com/pricing> | 8 | no |
| AdCreative.ai | <https://www.adcreative.ai/#new-pricing-section> | 30 | yes |
| Intercom helpdesk and Fin AI Agent | <https://www.intercom.com/pricing> | 9 | no |
| Captions | <https://www.captions.ai/pricing> | 8 | no |
| Chatbase | <https://www.chatbase.co/pricing> | 9 | no |
| Weav | <https://weav.com/pricing> | 9 | yes |

The first release follows the tools AI Hustle World has already written about. That is why the affiliate column exists: see [section 6 of the methodology](METHODOLOGY.md#6-independence).

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
- It contains no affiliate links. `source_url` always points to the vendor's own page, with no tracking parameters.

## Using and citing the data

The data is released under [CC BY 4.0](LICENSE): you may copy, share and build on it, including commercially, as long as you credit the source. A suitable credit is:

> AI Tool Pricing Database, AI Hustle World (https://aihustleworld.com), CC BY 4.0. Check the `verified_date` of each row you use.

Use the "Cite this repository" button on GitHub for a formatted citation.

## Reporting a problem

Found a price that changed, a broken source link or a wrong calculation? Open an issue using the **Price correction** template, or read [CONTRIBUTING.md](CONTRIBUTING.md). Corrections are reviewed against the vendor's own page.

## Related

- Full write-up and context: <https://aihustleworld.com/ai-tool-pricing-database>
- How AI Hustle World researches and tests tools: <https://aihustleworld.com/research-methodology>
- Corrections policy: <https://aihustleworld.com/corrections-policy>

Maintained by [Muntasir Ahmad Chowdhury](https://github.com/Muntasir-11).
