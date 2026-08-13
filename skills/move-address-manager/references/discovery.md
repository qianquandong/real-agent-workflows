# Discovery playbook

## Gmail searches

Start narrow and search `in:anywhere`. Use separate queries and paginate instead of one giant query.

1. Exact old street address in standard and abbreviated forms.
2. Exact old city plus ZIP when the street form varies.
3. Recent mail indicators: `"mailing address"`, `"address on file"`, `"mailed to"`, `"sent by mail"`, `"paper statement"`.
4. Financial and tax indicators: `"tax document"`, `W-2`, `1099`, `"replacement card"`, `"new card"`, `"mailed check"`.
5. Policy and renewal indicators: `policy`, `renewal`, `declarations`, `premium`, `coverage`, `license`, `EOB`, `"explanation of benefits"`.
6. Delivery and membership indicators: `shipped`, `delivery`, `subscription`, `membership`, `renewal notice`.

Prefer a two- or three-year window for discovery, then widen only for long-lived government, legal, retirement, education, property, or insurance relationships. An exact old-address match is stronger than generic mailing language.

Read only shortlisted messages needed to identify:

- organization and official domain
- whether physical mail is involved
- address type
- evidence date
- exact old-address match or weaker evidence
- next action

Do not treat marketing footers, sender office addresses, event venues, or shipping addresses for gifts to other people as the user's address.

## Other sources

- Statements and policies: inspect the address block and document date.
- Tax forms: capture payer/issuer and tax year; do not copy tax IDs into the ledger.
- Transactions: infer candidate merchants only; mark Possible until confirmed.
- Password manager or browser: accept domain names only, never credential exports.
- Physical mail: photograph or scan the envelope front with barcodes/account numbers redacted when possible.
- Previous move checklists: use them as candidates, not current proof.

## Deduplication

Normalize organization names and domains. Merge candidates only when account owner, organization, and address type match. Keep separate rows for distinct household members, business entities, policies, loans, properties, or address types.

## Evidence hygiene

Record the smallest useful evidence snippet. Prefer `Exact old address on July 2026 statement` over copying the full address or message body. Keep source links or message subjects only when access-controlled and useful for later verification.
