# Methodology

This page describes exactly how the data in `data/tool_pricing.csv` is produced, including where the process is limited. If a row cannot be defended under these rules, it does not go in.

## 1. Sources

Every row must be traceable to a **primary source** the vendor controls: the public pricing page, official documentation, or the vendor's help center. Third-party articles, reviews and aggregator sites are not used as the source of a price. They can be used to notice that a price may have changed, but the row is only updated after checking the vendor's own page.

`source_url` is stored as a clean link to the vendor page, with no tracking or affiliate parameters. `source_type` records which kind of page it is (`pricing_page`, `documentation`, `help_center`).

## 2. Verification

Each row is read from its source page on the date in `verified_date`. In this dataset the reading is done by an AI assistant (Claude) working for the maintainer. It opens the vendor's page in a real browser, reads the text the page displays, switches the billing toggle and plan selectors so that every billing period and tier the page offers is captured, and checks each figure against the page. Rows are then run through automated checks for format, allowed values, duplicate keys and arithmetic.

The maintainer has not personally re-opened every row. The `verified_by` column says who did the check: `ai-assisted` means the reading described above, and `maintainer` means the maintainer personally checked that row against the vendor page. A row that has not been read against its source page on that date does not get that date.

The limits of this approach are real. An AI assistant can misread a page, or miss a plan hidden behind a selector or a sales form. That is why every row links to its source, why corrections are welcome (see [CONTRIBUTING.md](CONTRIBUTING.md)), and why the dataset claims only that a figure is what the vendor's page displayed on that date.

If a page shows different prices by region, currency, platform or sign-in state, the row records the version that was seen and says so in `notes`. Pages were viewed from a single location, and some vendors price differently elsewhere. Prices are recorded exclusive of tax unless the vendor states otherwise.

## 3. What "blank" means

If a vendor does not publish a clear price, limit or unit definition, the field is left blank and `status` is set to `not_published` or `unclear`. Values are never estimated, inferred from similar plans or copied from another site to make a row look complete.

## 4. Calculated fields

`cost_per_unit` is calculated only for a unit the vendor itself names on the pricing page, such as a credit, a message credit or an outcome.

- For plan rows it is `price_amount / usage_limit_value`, and the formula is written in `cost_per_unit_basis` so anyone can redo the arithmetic.
- For usage-based rows where the vendor states a unit price, that price is copied and the basis says so.
- For annual and quarterly rows the calculation uses the monthly equivalent shown in `price_amount`.

The dataset never converts a vendor's unit into a different one, such as credits into minutes of audio or into finished videos. How much one credit buys depends on the model, feature or file, and is not fixed. Where a plan states its allowance in one unit and sells extra usage in another, or where one price covers several allowances, no figure is calculated. A blank here is deliberate.

## 5. Freshness

Each row carries its own `verified_date`. A row is treated as stale once its `verified_date` is more than 90 days old, whether or not its `status` has been updated yet. The maintainer sets `status` to `stale` when reviewing the dataset. Because prices can change at any time, a recent date reduces risk but never removes it, and users should confirm on the vendor's page.

When a vendor changes a price, the old row is set to `stale` and a new row is added with the new value and date, so the history stays visible. The dataset does not promise a fixed re-check schedule for every tool; it promises that every row shows how old it is.

## 6. Independence

Affiliate relationships, sponsorships and other commercial ties do not decide which tools are included or how their rows are written. The data file contains no affiliate links: `source_url` is always the vendor's own page. The coverage table in the README does include the maintainer's affiliate links for the tools where the maintainer has them. They are labeled as affiliate links, they sit outside the data file, and they never replace the vendor source link.

Readers should still be able to weigh the maintainer's position, so the `maintainer_affiliate` column says `yes` when AI Hustle World has an affiliate or referral link with that vendor on its website, and `no` when the maintainer knows of none. The first release covers tools that AI Hustle World has already written about, and some of those are affiliate relationships. In the first release ElevenLabs, AdCreative.ai and Weav are marked `yes`. AI Hustle World's broader disclosures are on its [Disclaimer](https://aihustleworld.com/disclaimer) page.

## 7. Scope of the first release

- Self-serve plan pricing shown on each vendor's public pricing page on the date in `verified_date`.
- Enterprise, custom and sales-only pricing is recorded as `not_published` and never estimated.
- Add-ons are covered only in part. The first release includes credit top-ups that have a stated unit price. Extra seats, extra email addresses, branding removal and similar add-ons are not yet covered.
- API, per-token and developer pricing is out of scope unless a row says otherwise. For ElevenLabs only the Creative plans tab was read, not the Agents or API tabs.
- Promotional prices, such as a discounted first month, are noted in `price_notes` and are not recorded as the plan price.

## 8. What this dataset does not claim

- It does not measure output quality, reliability or fit for a task.
- It is not based on purchasing or hands-on testing of the plans unless a row's `notes` says a specific plan was tested.
- It is maintained by a small independent publication and will miss changes between checks.
- Rows are read and checked by an AI assistant, not by a person on every row, unless `verified_by` says `maintainer`.

## 9. Corrections

See [CONTRIBUTING.md](CONTRIBUTING.md) and the site's [Corrections Policy](https://aihustleworld.com/corrections-policy).

## Data dictionary

| Column | Meaning |
|---|---|
| `tool_name` | Product name as the vendor writes it. |
| `vendor` | Company that sells the product. |
| `category` | Short label for the tool's main job, for example `video clipping`. |
| `plan_name` | Plan name as shown on the vendor page. Where a plan has several credit or usage tiers, the tier is added in brackets. |
| `billing_period` | `monthly`, `quarterly`, `annual`, `one-time` or `usage-based`. |
| `price_amount` | Number only, no currency symbol. For `quarterly` and `annual` rows it is the monthly equivalent the vendor displays; the total is given in `price_notes` when the page states it. For `usage-based` rows it is the vendor's stated price per unit, and `price_notes` names the unit. Blank if not published. |
| `price_currency` | ISO 4217 code, for example `USD`. |
| `price_notes` | Anything that changes how to read the price, such as "per seat per month" or "monthly equivalent shown". |
| `usage_limit_value` | The plan's stated limit as a number, if the vendor states one. If a plan states several limits, the main one is recorded here and the others are listed in `usage_limit_notes`. |
| `usage_limit_unit` | What the limit counts, for example `credits`, `media hours`, `seats`. |
| `usage_limit_notes` | Caveats on the limit, such as team size, rollover rules or other allowances. |
| `cost_per_unit` | Calculated only under section 4. Blank otherwise. |
| `cost_per_unit_basis` | The formula used, in plain words. |
| `free_tier` | `yes`, `no` or `limited`. Blank if the page does not say. |
| `source_url` | Vendor page the row was read from. |
| `source_type` | `pricing_page`, `documentation` or `help_center`. |
| `verified_date` | `YYYY-MM-DD` of the last check. |
| `verified_by` | `ai-assisted` or `maintainer`, as described in section 2. |
| `status` | `verified`, `not_published`, `unclear` or `stale`. |
| `maintainer_affiliate` | `yes` if AI Hustle World has an affiliate or referral link with this vendor, `no` if none is known (section 6). |
| `notes` | Anything else a careful reader would want to know. |
