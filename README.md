# TG Toolkit

A free suite of **51 Telegram tools**. No backend, no tracking, no sign-up — everything runs in your browser, and nothing you type ever leaves the page (except AI chats, which go to the free AI service to generate replies).

Live site: https://ryoaonetsuki.github.io/telegram-formatter/ (GitHub Pages)

## Tools (51, all real, all client-side)

### Write (10)
- **Post Formatter** (`formatter.html`) — toolbar editor (bold, italic, link, quote, list, code) + keyboard shortcuts, live Telegram-bubble preview, rich-text copy that pastes into Telegram with formatting intact
- **AI Post Writer** (`write.html#ai-writer`) — topic + tone → free AI draft, one-tap send into the Formatter
- **Post Preview** (`preview.html`) — channel-post rendering at phone (390px) and desktop widths
- **Caption & Message Counter** (`counter.html`) — live counts vs Telegram's 1024-character caption and 4096-character message limits
- **Word Counter** (`write.html#word-counter`) — words, characters, sentences, paragraphs
- **Poll Text Builder** (`poll.html`) — question + options → copyable poll text
- **Quiz Builder** (`write.html#quiz-builder`) — question + correct/wrong answers → copyable quiz text
- **Caption Ideas** (`write.html#caption-ideas`) — template-based ideas in four vibes (no AI)
- **Bio Generator** (`write.html#bio-generator`) — three template-based bio styles
- **Reading Time Estimator** (`write.html#reading-time`) — words + speed → minutes

### Format (18)
- **Stylish Fonts** (`fonts.html`) — real Unicode styles (bold, italic, script, monospace, double-struck, sans bold, circled), per-style copy
- **Spoiler Formatter, Strikethrough/Underline, Zalgo/Glitch, Code Block Builder, Quote Card** (canvas → downloadable PNG), **Case Converter, Text Reverser, Morse Code, Binary/Hex Converter, Remove Extra Spaces, Join Lines, Sort Lines, Remove Duplicate Lines, Emoji Remover, Text Diff, Lorem/Placeholder, Slug Generator** (all on `format.html`)

### AI (1 new; AI Post Writer counted under Write)
- **AI Chat** (`ai.html`) — free chat, no API key, powered by the free Puter.js AI with Pollinations as fallback

### Links (8)
- **Link Builder** (`links.html`) — validated t.me profile/channel/post links
- **Share Link Generator, Deep Link Builder** (bot start/startgroup), **Link Cleaner, Link Extractor, Mention Extractor, QR Code Generator** (local MIT library, PNG download), **UTM Builder** (all on `links2.html`)

### Media (5)
- **Image Compressor, Sticker Resizer** (Telegram 512px spec), **Color Palette Generator, Gradient Text Preview, Aspect Ratio Calculator** (all on `media.html`)

### Growth (6)
- **Hashtag Helper** (`hashtags.html`) — cleaned, deduplicated hashtags
- **Giveaway Winner Picker** (cryptographically random), **Countdown Text, Post Time Converter** (Dhaka default), **Poll Results Formatter, Follower Goal Progress** (all on `growth.html`)

### Developer (3)
- **Markdown → Telegram HTML** (`md2html.html`) — Bot API HTML converter
- **Inline Keyboard JSON Builder, Bot Commands JSON Builder** (both on `dev.html`)

## Free AI — how it works, and its limits

AI Chat and AI Post Writer call the **free Puter.js AI** (Puter.js SDK, no API key) first, and fall back to the **Pollinations free text API** (`https://text.pollinations.ai/`, GET request) if Puter fails. Neither needs an API key and nothing is stored here. Both are real third-party **shared free services** — not our own model, not unlimited — so replies can be slow or busy at times, and heavy Puter use may ask you to sign in to a free Puter account. If both fail, the UI shows the error and a retry button; replies are never faked. Do not paste passwords or private information into the AI chat (your prompt is sent to the free AI service to generate the reply).

## Why the Post Formatter exists

Telegram's message box does not render markdown pasted as plain text. Copying `**bold**` from a code block shows the asterisks literally. The Formatter puts formatted HTML on the clipboard instead, so Telegram receives the formatting itself.

## Design

Design v3 in `assets/style.css`: premium dark product design — solid refined panels, hairline borders, one restrained accent family, clear typography and spacing (no gradients, no glows, no backdrop blur). App-shell layout — a sidebar on desktop (content pane beside it) and a bottom navigation bar on mobile, so the site feels like a desktop app on desktop and an Android app on phones.

Icons are **Lucide** (MIT, https://lucide.dev) for UI and **Simple Icons** (CC0, https://simpleicons.org) for real brand marks — SVGs vendored locally under `assets/icons/` and inlined at build time; no CDN hotlink for icons, no emoji-as-icons anywhere in UI chrome. The logo is an original geometric mark (`assets/logo.svg`: solid accent tile, double-chevron construction). The QR code library is qrcode-generator by Kazuhiko Arase (MIT), vendored locally in `assets/qrcode.js` with its license header intact.

Design history: v1 of this site was styled with the solid-glass design system (MIT, deeplethe/solid-glass); v2 used a custom glassmorphism system. Both were replaced in the 2026-11-01 v3 redesign; neither ships anymore, and no solid-glass docs content, logos, or text were ever copied.

## Run it locally

No build step, no server, no install. Open `index.html` in a browser — or serve the folder with any static host. Hosted on GitHub Pages (`.nojekyll` at the repo root so Pages serves files as-is).

## Privacy

No backend, no analytics, no data collection. All tools run entirely in the browser, except AI features as described above.

## License

MIT — see [LICENSE](LICENSE).
