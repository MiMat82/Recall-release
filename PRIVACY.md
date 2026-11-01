# Recall · Privacy and permissions

**A Novalon app · Applies to version 0.1.4**

Recall's search processing runs in your browser. It does not send your queries, favorites or remembered page context to a Novalon server or a cloud AI provider.

## What Recall reads

- Supported web bookmark titles, URLs and folder paths in the current browser profile.
- Changes to those bookmarks so search can stay current.
- Only when you click **Remember this page**: the active bookmarked page's title, description metadata and headings.

Recall does not automatically open all your saved pages. The context-capture function does not read form values or capture the full page body. Page titles and headings can still contain sensitive information; only remember pages whose context you want stored in this browser profile.

## What is stored

Recall uses the browser profile's IndexedDB storage for its search vectors, fingerprints and optional remembered page context. Searches run locally; Recall does not maintain a query-history feature.

The stored context and index are not separately encrypted by Recall. They rely on the protection of the browser profile, operating-system account and device. People or software with access to that profile may be able to access its local data.

There is no Recall account, cloud backup or cross-device sync. The browser's own favorites synchronization is separate and follows your browser settings.

## Local context backups

Only when you choose **Export context**, Recall creates a JSON download containing the URLs and page text you asked it to remember. This file is not encrypted and may contain private information. Keep it in a private location; do not post it in a public issue. The file is not a backup of all browser favorites and does not include cached vectors.

**Import context** reads the file you select locally, validates it, and adds missing context only for matching favorites. It keeps existing entries. Invalid files are rejected before writes; an import transaction failure rolls back its changes. Recall does not upload the file. The next search opening rebuilds any needed vectors locally.

## Network activity

The model, runtime and search core are bundled. Indexing and searching require no external network requests. Recall includes no analytics, remote favicon service or cloud inference calls.

Opening a search result connects to the destination website in the normal way. Clicking **Downloads & updates** or **More apps on GitHub** opens GitHub. Those websites have their own data practices.

In the unpacked/GitHub edition, only when you click **Check for updates** in About, Recall requests the latest public release information from GitHub's API. The request contains no favorites, queries or remembered page context; it omits cookies and authentication. GitHub receives normal connection metadata, such as your IP address. The unpacked edition has no background release checks and does not automatically download or install updates.

The separate Edge Add-ons package delegates updates to Microsoft Edge and does not use the GitHub checker. Store update requests follow Microsoft's browser service behavior. The store listing is not yet live; [current status](EDGE-ADDONS.md).

## Why these permissions are requested

| Permission | Use in Recall |
|---|---|
| `bookmarks` | Read favorites and observe changes. Production code does not create, rename, move or delete bookmarks. The browser permission itself is broader than this read-only use. |
| `activeTab` | Temporary access to the current tab when you invoke Recall, used to determine whether Remember this page is available. |
| `scripting` | Read the title, description and headings after you explicitly click Remember this page. |

There is no broad all-websites host permission or background page crawler. Browser-internal and other protected pages cannot be captured.

## Deletion, updating and removal

Uninstalling Recall removes its local index and saved page context. Native favorites are kept. A prior context export can be imported into a new installation; there is no individual remembered-context deletion screen. Exported files remain wherever you saved them and are not removed by uninstalling Recall.

For unpacked updates, replace files in the existing installation folder and reload the extension. About includes **Reload Recall** for this step. Avoid uninstalling if you want to retain Recall's context. [Illustrated update instructions](UPDATING.md). If you need to remove all Recall-owned local data, uninstalling is the available reset mechanism; a later installation will have to rebuild its index.

## Questions or problems

Report reproducible issues in the [public issue tracker](https://github.com/MiMat82/Recall-release/issues). Use invented sample URLs and titles where possible. Do not post a full personal bookmark export or sensitive page text to a public issue.
