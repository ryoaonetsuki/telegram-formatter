# Telegram Formatter

Write simple markup, preview it like a Telegram message, and copy **real rich text** — so bold, quotes and links survive the paste into Telegram.

## Why this exists

Telegram's message box does not render markdown pasted as plain text. If you copy `**bold**` or `[text](url)` from a code block or a plain-text file, Telegram shows the asterisks and brackets literally.

This tool puts formatted HTML on the clipboard instead, so Telegram receives the formatting itself — the same way copying from a formatted document works.

## How to use (3 steps)

1. **Write** your post in the left box using the markup below (or press **Load sample**).
2. Press **Copy formatted**.
3. **Paste into Telegram** (Desktop, Web, or mobile) — bold, quotes and links stay intact.

## Supported markup

- `**bold**`
- `__italic__` or `*italic*`
- `` `code` ``
- `> quote line`
- `[link text](https://example.com)`
- `- list item`
- `# Heading line`

## Run it locally

No build step, no server, no install. Just open `index.html` in a browser — it works offline.

Or host the folder with any static host (Cloudflare Pages, GitHub Pages, Netlify).

## Privacy

No backend, no tracking, no analytics. Everything runs in your browser; nothing you type is sent anywhere.

## License

MIT — see [LICENSE](LICENSE).
