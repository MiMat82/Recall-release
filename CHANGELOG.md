# Recall · Release notes

## Publishing update — 1 November 2026

GitHub is the distribution channel for Recall. The planned Edge Add-ons enrollment has been discontinued. The product page, launch materials and user guides now reflect GitHub installation and manual updates using the existing About controls. This is a documentation update: **the 0.1.4 ZIP, extension identity and stored data are unchanged**.

[Launch kit](MARKETING.md) · [Update safely](UPDATING.md)

## 0.1.4 — 1 November 2026

Back up remembered context and bring it to another Recall installation.

- Added **About → Export context** and **Import context**. The local JSON contains remembered URLs and page text; keep it private.
- Imports add missing context for matching favorites and keep existing entries. Invalid files are rejected without partial writes; favorites are not modified.
- Earlier preparation included a separate Edge Add-ons submission package, copy and images. That publishing route has since been discontinued; the preparation remains an inactive reference, not an upcoming release.
- Kept the current GitHub/unpacked edition's identity and manual update path. Both previous public downloads remain unchanged.

Cross-ID migration, transaction rollback, offline search and accessibility passed in isolated Edge and Chrome profiles. In-place upgrades through 0.1.4 retained existing fixture context and vectors. The store ZIP was exercised unpacked for code verification; this does not test Microsoft-delivered installation or updates.

[Distribution update](EDGE-ADDONS.md) · [Update the current ZIP edition](UPDATING.md)

## 0.1.3 — 1 November 2026

Update your existing installation with clearer guidance and an on-demand release check.

- Added **About → Check for updates**, which compares the installed version with the latest complete public GitHub release.
- Added an in-place update walkthrough and **Reload Recall**, using the browser's reload function after you replace the files.
- Added distinct messages for newer, current and ahead-of-public builds, plus connection failures and GitHub rate limits.
- Kept the extension identity, storage format, search engine and browser permissions unchanged.
- Checks run only on click and contain no favorites, searches or page context. GitHub receives normal connection metadata. No background checker or automatic installer is included.

Read [Update without starting over](UPDATING.md). Do not remove/reinstall Recall to update. Upgrades from 0.1.1 through 0.1.2 to 0.1.3 and the new reload button retained fixture favorites, context and cached vectors in isolated Edge and Chrome profiles. The public 0.1.2 download remains unchanged.

## 0.1.2 — 1 November 2026

Recall is presented as **a Novalon app**, with the product name remaining **Recall**.

- Added the Novalon credit to About and license information.
- Added **Downloads & updates** pointing to the public Recall-release repository.
- Retained **More apps on GitHub** for the wider public app collection.
- Added a full public product presentation, original cover artwork, real product screenshots, privacy information and an illustrated installation/use/update guide.
- Preserved the extension identity, permissions, search engine and storage format.

Install the named **Recall-0.1.2.zip** asset. Verify it against its accompanying SHA-256 file if desired. The guide is also available in this repository. GitHub's automatic source archives are documentation snapshots, not the installable add-on.

For an existing unpacked installation, replace the files in its current folder and click **Reload**. Do not uninstall to update. This release does not add automatic updates or browser-store distribution.

Validation covers the actual extension and exact extracted package in installed Edge and Chrome, including offline search and the new About links. The small synthetic relevance benchmark and prior recovery/scale measurements are not guarantees for a personal collection.

## 0.1.1 — 1 November 2026

- Blue layered-card identity, rounded search results and matching light/dark themes.
- Redesigned About page and public-apps link.
- Additional popup-layout and accessibility checks.

## 0.1.0 — 1 November 2026

- Initial local development build: native bookmark search, Rust/WebAssembly ranking, bundled local meaning search, optional page-context capture, keyboard navigation and resumable indexing.

Versions 0.1.0 and 0.1.1 were local development builds. Version 0.1.2 is the initial public package in this release repository.
