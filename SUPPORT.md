# Recall · Help and known limits

## I see only folders when installing

The folder picker hides regular files. Select the extracted root folder, where `manifest.json` lives. Do not choose `models`, `icons` or another subfolder. [See the installation guide](GETTING-STARTED.md#2-load-recall-into-edge).

## The browser says the manifest is missing

Extract **Recall-0.1.2.zip** first. Select its extracted root, not the ZIP, the directory above it, or GitHub's automatic “Source code” download.

## Recall has no results

Check that this browser profile has ordinary HTTP/HTTPS favorites. Recall does not search other profiles, history, Edge Collections or saved posts inside other services. File links and bookmarklets are excluded. Try a known bookmark name before a descriptive query.

## Meaning search is still preparing

Keep the popup open. Progress is saved as bookmarks finish, and the next opening resumes after an interruption. A large first library takes longer than a subsequent cached opening. Text matching remains available while meaning search prepares.

## The suggestions are not what I meant

Search with a specific name, topic or folder, and inspect the website and folder under the result. A vague bookmark may not provide enough context. On its original page, use **Remember this page** to add a title, description and headings. The model is English-focused; “Related” results can be weak matches.

## Remember this page is missing or fails

Open the actual bookmarked web page, then click Recall's toolbar button there. The active URL must match a supported saved bookmark. Browser settings pages and other restricted pages cannot be read. If the page navigated while Recall was open, reopen the popup on the current page.

## Search reports an error

Use **Try again**, or close and reopen Recall. If files were moved or incompletely extracted, restore the complete extension folder and reload it on the browser's Extensions page. Text results remain usable if only the meaning-search model fails. Record the exact error before considering a reset.

## The toolbar icon is missing

In Edge, open **Extensions** and choose **Show in toolbar** beside Recall. In Chrome, click its pin in the Extensions menu. Confirm Recall is enabled on `edge://extensions` or `chrome://extensions`.

## I want to update

Replace the files in the existing unpacked folder and click **Reload**. Do not uninstall as an update step; that clears Recall's remembered context. Native favorites are not removed. [Full update instructions](GETTING-STARTED.md#7-update-without-starting-over).

## Compatibility and scope

- Currently tested: installed desktop Microsoft Edge and Google Chrome on Windows. Other operating systems and Chromium-based browsers are not yet qualified.
- The manifest requires Chromium 120 or later; that minimum does not mean every intervening version has been tested.
- No mobile-browser support is claimed.
- No browser-store listing or automatic update service is currently provided.
- Enterprise policy may prevent unpacked installation. Contact your administrator; do not bypass policy.
- No guarantee of all-language semantic accuracy, full 50,000-bookmark indexing performance, or accessibility with every assistive technology. Automated accessibility checks have passed; human screen-reader testing remains open.

## Report an issue

Open an [issue](https://github.com/MiMat82/Recall-release/issues) with your Recall version, browser version, operating system, steps to reproduce, expected behavior and actual behavior. A small invented example is more useful—and safer to share—than your full favorites library.

Product development is maintained separately from this public release and support repository.
