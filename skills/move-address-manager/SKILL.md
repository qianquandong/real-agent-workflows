---
name: move-address-manager
description: Audit, plan, execute, and verify postal-address changes for a household or business move. Use when a user is moving, wants to find every organization that may hold an old physical or mailing address, search Gmail or supplied records for address evidence, build a master change-of-address checklist, update accounts through official sites, check USPS/government/employer/financial/insurance/business/subscription records, or follow up on missed mail after a move.
---

# Move Address Manager

Manage a move as an evidence-backed address migration. Discover every likely address holder, distinguish address types, update only the correct records, and verify completion.

## Choose the mode

- **Audit:** Discover candidates and produce a prioritized ledger. Make no external changes.
- **Plan:** Audit, resolve address scopes, and prepare an execution sequence. Make no external changes.
- **Execute:** Work through an approved ledger using official provider pages and connected apps.
- **Verify:** Check confirmations, new statements, returned mail, and unresolved candidates.

If the user's request is ambiguous, begin in Audit mode. Do not treat “one click” as authorization to change every account.

## Start with a move profile

Collect only what is needed:

1. Move country/state, move date, and whether the move is permanent or temporary.
2. Who is moving: user, household members, dependents, or a business.
3. Address labels and scopes, such as `Old home`, `New home`, `Business mailing`, and `Registered agent`.
4. Whether Gmail, uploaded statements, account-site review, or a domain-only account list may be used.
5. Whether the user wants Audit, Plan, Execute, or Verify mode.

Do not store exact addresses in the skill. Default the ledger to labels and redacted evidence. Ask before saving full addresses in a persistent artifact. Never ask the user to paste passwords, SSNs, full payment-card numbers, or security codes into chat.

## Distinguish address types

Never copy one new address into every field without inspection. Classify each record as one or more of:

- residential or legal residence
- mailing or correspondence
- billing
- shipping
- service location
- vehicle garaging
- tax residence
- employer/payroll/benefits
- business principal office or mailing
- registered-agent address

Changing one type may not change the others. Flag any change that could affect taxes, insurance rating, voting eligibility, immigration obligations, licenses, or business registration for official-source verification and user confirmation.

## Discover address holders

Read [references/discovery.md](references/discovery.md) before searching mail or records. Read [references/categories.md](references/categories.md) when building the coverage checklist.

Use multiple discovery surfaces because none is complete:

1. Search connected Gmail for the exact old address and common formatting variations, then for evidence of mailed statements, policies, tax forms, renewals, cards, checks, and deliveries. Follow the Gmail skill. Shortlist first; read only messages needed to identify the institution and address evidence.
2. Search user-supplied statements, policies, tax forms, leases, closing documents, and account exports. Extract organization, address type, evidence date, and current-address evidence.
3. Review connected provider records when an app supports them. Do not use a browser as a substitute for a provider connector.
4. Accept a domain-only list from a password manager or browser account list. Never request or accept a password export containing credentials.
5. Use financial statements only with permission to infer recurring merchants that may ship, bill, insure, or maintain a membership. Treat the inference as Possible until confirmed.
6. Use direct browser interaction only after an explicit request to open or act on specific sites. A cloud browser normally cannot read the user's local Safari or Chrome history; state this limitation instead of claiming full history access.

Do not browse public web pages merely to infer that the user has an account. Public research may identify an official change process, not prove account ownership.

## Build the master ledger

Copy [assets/address-change-ledger.csv](assets/address-change-ledger.csv) or reproduce its columns in a spreadsheet. Preserve one row per organization and address type. Use only these confidence values:

- **Confirmed:** Exact old address appears in a current profile, statement, policy, form, or recent correspondence.
- **Probable:** Strong recent evidence shows the organization sends physical mail, but the stored address has not been viewed.
- **Possible:** An account or recurring relationship exists, but physical-mail or address evidence is absent.

Use only these statuses: `Discovered`, `Needs review`, `Ready`, `Submitted`, `Verified`, `Not applicable`, `Blocked`, `Deferred`.

Never mark a row Submitted from a clicked button alone if the site returned an error or no success state. Never mark it Verified without confirmation evidence or a later account/statement check.

## Prioritize and plan

Sequence work by consequences and deadlines:

1. Mail forwarding and immediate legal/government duties.
2. Identity, immigration, tax, license, voter, and business registrations that apply.
3. Employer, payroll, retirement, brokerage, banking, credit, loans, and insurance.
4. Housing, utilities, vehicles, health care, schools, pets, and professional licenses.
5. Commerce, memberships, subscriptions, charities, loyalty programs, and personal contacts.

USPS forwarding is a safety net, not a universal update. It does not replace direct changes and not all mail is forwarded. For government, legal, immigration, tax, insurance, or business obligations, verify current deadlines and procedures on official sources at execution time. Prefer `.gov`, state agency, regulator, employer, insurer, or provider pages; do not rely on remembered rules.

## Execute safely

Before changing anything, show the user the batch: organization, address type, proposed target label, expected consequence, and whether identity verification is likely. Obtain explicit authorization for the batch.

For each approved row:

1. Open the official provider page or connected app.
2. Let the user take over for login, MFA, identity questions, or sensitive values when necessary. Do not accept credentials in chat.
3. Inspect the current field and confirm its address type and scope.
4. Present the proposed change if it affects government, finance, insurance, employment, immigration, licenses, voting, taxes, or a business record.
5. Submit only the approved change.
6. Capture non-sensitive proof: success message, confirmation reference, timestamp, or confirmation-email subject.
7. Update the ledger immediately.

Do not silently change autopay, paperless settings, beneficiaries, tax withholding, policy coverage, delivery instructions, household members, or other adjacent settings. Do not delete historical or gift-recipient shipping addresses merely because the default address changes. Do not send address details to an email recipient unless the user explicitly asks and the recipient is verified.

## Verify and close

After execution:

1. Search for confirmation emails and compare the account profile or next statement when available.
2. Review forwarded mail and mail arriving at the old address for missed senders.
3. Re-run the old-address search after new statements and tax forms arrive.
4. Keep unresolved Possible rows separate from completed rows.
5. Produce a closeout summary with counts for Verified, Submitted-not-verified, Blocked, Deferred, and Possible.

Suggest a later follow-up only when a real verification window or unresolved dependency exists. Create a reminder or recurring check only if the user requests it.

## Guardrails

- There is no universal API that safely updates every organization. Describe the experience as assisted batch execution, not guaranteed one-click replacement.
- Minimize sensitive data in outputs and never repeat full addresses unnecessarily.
- Do not infer legal residence from where the user wants mail delivered.
- Do not change another household member's record without their authorization.
- Stop on conflicting address evidence, unclear account ownership, a sign-in wall without supported takeover, or any change whose consequences cannot be determined.
- In Audit or Plan mode, remain read-only.
