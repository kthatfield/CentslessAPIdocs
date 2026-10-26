# Documentation project instructions

## About this project

- Developer documentation for the Centsless Decision and Evidence Engine, built on Mintlify. Configuration lives in `docs.json`; pages are MDX with YAML frontmatter; the API Reference tab is generated from `openapi.yaml`.
- The engine is a cash rounding compliance API: it resolves where a sale happened, finds the governing rule for the date and the transaction type, rounds the cash total, and seals the statute and the location into a hash-chained record.

## Terminology

- "Centsless" is one word, always.
- "Decision and Evidence Engine" or "the engine". Not "platform", "solution" or "tool".
- Records are "tamper-evident" and "hash-chained". Never "immutable" or "tamper-proof".
- A rule "governs" a transaction. Use "obligates" and "permits" for statutory obligation, not "mandatory" and "optional" in prose.
- "Enacted" is not "in force". Use "in force", "pending effective", "default practice" as the engine does.
- Use the engine's field names in backticks when referring to API data.

## Style

- No em dashes or en dashes. No exclamation points. No contractions.
- Never use: leverage, utilize, robust, seamless, delve, cutting-edge, best-in-class.
- Sentence case for headings. Second person for instructions.
- Hedge negative existence claims with "to our knowledge". Avoid absolute "only" claims unless verified in the enacted text.
- Every statutory statement names its source: bill, chapter or session law, codified section. Dates are read from the enacted text, not from secondary sources.

## Content boundaries

- Do not document internal admin features beyond what the OpenAPI document lists.
- Do not claim a patent. Do not describe a sandbox environment; pilots run against production with their own records.
- Do not state that H.R. 10167 is law unless the federal row in the dataset says `enacted`.
- Do not describe the Observatory's local research records as rules the engine applies.
