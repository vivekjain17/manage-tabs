# Manage Tabs

**Your browser tabs, organized.**

Manage Tabs is a Chrome extension that replaces your new tab page with a clean dashboard of everything you have open. View tabs grouped by domain or by Chrome tab group, drag and drop to reorganize, and close duplicates in one click.

No server. No account. No external API calls. Just a Chrome extension.

---

## Features

### Views
- **Domain view** — tabs grouped by website, homepages (Gmail, X, LinkedIn, YouTube, GitHub) pulled into their own card at the top
- **Tab Groups view** — tabs organized by your Chrome tab groups, with ungrouped tabs shown as domain sub-cards below
- **Smart default** — automatically opens in Tab Groups view when you have named Chrome groups set up

### Organization
- **Drag and drop** — drag a group header or individual tab chip onto another group to merge them
- **Localhost grouping** — shows port numbers so you can tell your local projects apart
- **Expandable cards** — first 8 tabs shown, click "+N more" to expand

### Cleanup
- **Duplicate detection** — duplicate tabs are highlighted with an amber left stripe and `(Nx)` pill badge in both domain and tab group views
- **One-click duplicate removal** — "Close N duplicates" button on any card that has them
- **Close with style** — swoosh sound + confetti burst on close
- **Save for later** — bookmark tabs to a checklist before closing them

### Dashboard
- **Personalized greeting** — shows your first name when you're signed into Chrome
- **Live tab counts** — badge and close-all button update in real time as you close tabs, no full reload
- **Jump to any tab** — click any tab title to focus it across windows

### Privacy
- **100% local** — your data never leaves your machine
- **Pure Chrome extension** — no server, no Node.js, no npm

---

## Setup

**1. Clone the repo**

```bash
git clone https://github.com/vivekjain17/manage-tabs.git
```

**2. Load the extension in Chrome**

1. Go to `chrome://extensions`
2. Enable **Developer mode** (top-right toggle)
3. Click **Load unpacked**
4. Select the `extension/` folder inside the cloned repo

**3. Open a new tab**

Manage Tabs replaces your new tab page.

---

## How it works

```
You open a new tab
  → Dashboard shows open tabs grouped by domain or Chrome tab group
  → Homepages get their own card at the top
  → Click any tab title to jump to it
  → Drag groups or individual tabs to reorganize
  → Close duplicates, groups, or individual tabs
  → Save tabs to a checklist before closing
```

Everything runs inside the Chrome extension. Saved tabs are stored in `chrome.storage.local`.

---

## Tech stack

| What | How |
|---|---|
| Extension | Chrome Manifest V3 |
| Tab groups | `chrome.tabGroups` API |
| Identity | `chrome.identity` API |
| Storage | `chrome.storage.local` |
| Drag and drop | Pointer Events API |
| Sound | Web Audio API (synthesized, no files) |
| Animations | CSS transitions + JS confetti |

---

## License

MIT — see [LICENSE](LICENSE)

---

Built on top of [Tab Out](https://github.com/zarazhangrui/tab-out) by [Zara Zhang](https://x.com/zarazhangrui) (MIT License).
