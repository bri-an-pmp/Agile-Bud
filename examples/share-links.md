# [Share Links] Generate share links in bulk

As a Canto admin at an enterprise company
I want to generate share links for many assets in one request
So that I can hand those links to clients during a migration without creating them one by one

**Problem**
Admins recreate client-facing share links one at a time in the UI. A migration with hundreds of existing links is too slow to do by hand, and the links then have to be copied into the customer's CRM.

**Proposed behavior**
An admin selects an album or a list of assets and receives a share link for each one, including the asset name and an expiration date when one is set. The same result can be downloaded as CSV.

**Acceptance criteria**

- [ ] An admin can start generation for an album or a list of assets
- [ ] Each result includes the asset name, the link, and the expiration date when set
- [ ] The admin can download those results as CSV
- [ ] Generated links follow the same permission and expiration rules as a link created in the UI

**Developer handoff**

- In scope: create many links in one action and export the result
- Out of scope: editing links that already exist, and sending the CSV to a CRM
- Affected surfaces: share-link API and the share-link UI
- Permissions: admins only
- Edge cases: album with no assets, asset the caller cannot share, expiration omitted
- How to verify: generate links for a small album and confirm the CSV matches links opened in the UI

**Assumptions**

- Bulk generation uses the same link rules as the single-link flow. `[confirm]`
- Volume in the reported case is hundreds of links, not millions.

**Priority signal**

- Customer-reported: Yes
- Affects more than one customer: Yes
- Blocks a deal or renewal: Unknown
