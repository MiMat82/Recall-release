# Recall · Edge Add-ons submission copy

**Prepared for 0.1.4. Draft for submission, not evidence of a live store listing.**

## Identity and listing fields

- Name: **Recall**
- Parent brand / intended publisher: **Novalon**, subject to the owner's completed publisher registration.
- Endorsement: **A Novalon app**
- Language: English (United States)
- Category: Productivity
- Website: https://github.com/MiMat82/Recall-release
- Support: https://github.com/MiMat82/Recall-release/issues
- Privacy policy: https://github.com/MiMat82/Recall-release/blob/main/PRIVACY.md
- Suggested search terms: bookmark search; favorites; local search; recall; productivity; saved pages; Novalon
- Suggested availability: Public; all supported markets. Confirm actual account and submission settings in Partner Center.

## Short description

Find saved pages by what you remember. Private favorites search for Microsoft Edge. A Novalon app.

## Full description

You saved the right page. Now find it again.

Recall is a Novalon app that brings a focused favorites search to your Microsoft Edge toolbar. Click the blue Recall icon, enter a name, a topic or a short description, and open the page you need. Your favorites stay in the folders you already use.

FIND WHAT YOU REMEMBER

Search across supported web favorites in your current browser profile. Recall combines ordinary text matching, prefix and typo tolerance with local meaning-based suggestions. Results show the saved title, website and folder so you can check the match before opening it in a new tab.

GIVE VAGUE BOOKMARKS BETTER CLUES

A bookmark called “Home” may not say enough. While you are on that bookmarked page, open Recall and choose Remember this page. Recall saves its title, description and headings on your device and can use those details in later searches. It does not capture form values, archive the full page or automatically visit every favorite.

KEEP SEARCH LOCAL

The search model, runtime and Rust/WebAssembly search core are included. There is no account, API key, cloud AI call, analytics service or first-run model download. Text results are available while the meaning-search index prepares. Indexing progress saves as it goes and resumes when you reopen Recall.

A SIMPLE DAILY FLOW

Pin Recall, click, search and open. Use the arrow keys and Enter if you prefer the keyboard. Light and dark appearances follow your browser. The optional Alt+Shift+F shortcut opens Recall when that shortcut is available.

UPDATES AND YOUR EXISTING CONTEXT

When installed from Microsoft Edge Add-ons, approved updates are delivered automatically by Edge. If you are moving from Recall's unpacked edition, first export your remembered context from About, then import it into the store edition. Existing context is kept, matching favorites receive missing context, and the search index rebuilds locally. Backup files contain URLs and remembered text and should be kept private.

KNOW THE SCOPE

Recall searches web favorites in the current profile. It does not search browsing history, Edge Collections, another profile or saved posts inside other services. File links and bookmarklets are excluded. Meaning search is English-focused and can return weak suggestions; labels such as Related and Possible matches are suggestions to inspect, not guarantees.

Opening a result connects to that website normally. GitHub links open GitHub, and store updates use Microsoft's browser update service. There is no Recall cloud sync or backup. Your browser's native favorites synchronization follows your browser settings separately.

Recall. Save today. Find tomorrow.

## Single purpose

Help users retrieve their existing web favorites from a toolbar search, optionally enriched with page details they explicitly choose to remember locally.

## Permission justifications

| Permission | Justification |
|---|---|
| bookmarks | Read the current profile's web favorites and observe changes so results stay current. Production code does not create, rename, move or delete favorites. |
| activeTab | Determine the active page after the user invokes Recall and provide temporary access for the explicit Remember this page action. |
| scripting | Read the bookmarked page's title, description metadata and headings only after the user chooses Remember this page. No form values or full page bodies are captured. |

No broad website host permission, native messaging helper or background crawler is requested. Context export uses an ordinary local browser download; import reads only the file the user selects.

## Remote code and data handling

No remote executable code is loaded. JavaScript, WebAssembly and the quantized model/runtime files are bundled. The WebAssembly CSP allowance enables these local files. The Edge submission package removes the GitHub update API connection allowance and hides the unpacked edition's manual checker. Microsoft provides the store update channel.

Declare the local handling of bookmark titles/URLs/folders and user-selected page title/description/headings accurately in the current Partner Center fields. These can contain personal or sensitive information even though Recall does not send them to the publisher. IndexedDB stores remembered context and cached vectors in the browser profile. Explicit JSON exports put remembered URLs/text in a user-controlled local file. Import adds missing context for current bookmarks without replacing existing entries.

No advertising, sale of data, analytics, query history, cloud AI or publisher-operated server is used. The app does not add separate encryption to its database or backup file. Opening links has ordinary website network effects. The owner must review the current submission declarations and certify that they match these facts; no certification has yet been submitted.

## Reviewer instructions

1. No login or test account is required. Add ordinary HTTP/HTTPS favorites to an isolated Edge profile, including a page with an opaque title such as Home.
2. Pin Recall and open its toolbar popup. Search an exact title, a folder name and a descriptive phrase. Text matching works while local meaning indexing prepares; leave the popup open to finish indexing.
3. Select a result by mouse or arrow keys/Enter. It opens the saved URL in a new tab. Escape clears the query, then closes the popup.
4. On the bookmarked web page, open Recall from its toolbar button. Choose Remember this page. Verify the saved-context status, then search a word in the page's description/headings. Browser settings pages are intentionally excluded.
5. In About, export context, then import that same file. Existing entries should be kept. Importing malformed JSON should show a clear failure and preserve data.
6. Switch between light/dark appearance. Search and context handling work offline after installation because the model is bundled. Opening destination websites still requires normal connectivity.
7. The Edge package displays Automatic updates through Edge. That describes store-installed behavior; sideloading the submission ZIP for review does not activate store updates by itself.

Meaning search is English-focused and may return weak related suggestions for unrelated queries. The approximately 22.3 MB package includes its own model and runtime. Bundled notices are available in About → Third-party licenses and attribution.

## Assets

- `assets/edge-store/logo-128.png`: 128 × 128 logo.
- `assets/edge-store/search-walkthrough.png`: 1280 × 800 explanatory image with an actual search capture and synthetic favorites.
- `assets/edge-store/remember-walkthrough.png`: 1280 × 800 explanatory image with an actual toolbar capture on a local sample page.

The screenshots use synthetic data. Surrounding callouts explain the workflow and do not represent additional application screens.
