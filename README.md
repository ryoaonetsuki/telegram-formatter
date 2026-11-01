# TG Toolkit

A free suite of Telegram tools. No backend, no tracking, no sign-up — everything runs in your browser, and nothing you type ever leaves the page.

Live site: https://telegram-formatter.pages.dev

## Tools

| Page | What it does |
|---|---|
| `index.html` | Home — hero + grid of all tools |
| `formatter.html` | **Post Formatter** — toolbar editor (bold, italic, link, quote, list, code) + keyboard shortcuts, live Telegram-bubble preview, rich-text copy that pastes into Telegram with formatting intact |
| `fonts.html` | **Stylish Fonts** — real Unicode styles (bold, italic, script, monospace, double-struck, sans bold, circled) with per-style copy |
| `counter.html` | **Caption & Message Counter** — live counts against Telegram's 1024-character caption and 4096-character message limits, with over-limit warnings |
| `links.html` | **Link Builder** — validated t.me links for profiles, channels, posts and share-text links |
| `md2html.html` | **Markdown → Telegram HTML** — converts markdown to Telegram Bot API HTML (`<b>`, `<i>`, `<a>`, `<code>`, `<pre>`, `<blockquote>`) for bot developers |
| `poll.html` | **Poll Text Builder** — question + options → clean copyable poll text |
| `hashtags.html` | **Hashtag Helper** — cleaned, deduplicated hashtag list from messy input |
| `preview.html` | **Post Preview** — see a post rendered as a Telegram channel post at phone (390px) and desktop widths |

## Why the Post Formatter exists

Telegram's message box does not render markdown pasted as plain text. Copying `**bold**` from a code block shows the asterisks literally. The Formatter puts formatted HTML on the clipboard instead, so Telegram receives the formatting itself.

## Run it locally

No build step, no server, no install. Open `index.html` in a browser — or serve the folder with any static host (Cloudflare Pages, GitHub Pages, Netlify).

## Privacy

No backend, no analytics, no data collection. All tools run entirely in the browser.

## License

MIT — see [LICENSE](LICENSE).
