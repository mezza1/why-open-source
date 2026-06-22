# Why You Should Use Open Source Models

A simple, single-page site listing reasons to build on open-source / open-weight AI models instead of closed, proprietary ones. Each reason expands to reveal a short explanation and sources.

**Live:** https://mezza1.github.io/why-open-source/

## Stack

Plain static HTML + CSS — no build step, no dependencies.

- `index.html` — the page and all reasons
- `style.css` — the styling (clean, document-style theme)

Reasons are native `<details>`/`<summary>` elements, so the expand/collapse works without JavaScript.

## Run locally

```bash
python3 -m http.server 4173
# then open http://localhost:4173
```

## Add or edit a reason

Each reason is one `<li>` in `index.html`:

```html
<li>
  <details class="reason">
    <summary><span class="reason-title">So you ...</span></summary>
    <div class="reason-body">
      <p>The explanation.</p>
      <p class="sources">Source: <a href="..." target="_blank" rel="noopener">Title</a></p>
    </div>
  </details>
</li>
```

The numbers are generated automatically, so just add the `<li>` in the order you want. Bump the "Last updated" date in the header when you make changes.

## Contributing

Contributions are welcome! Got another reason to use open-source models — or a better source for an existing one? Open a pull request (add or edit an `<li>` as shown above) or file an issue with the suggestion. Sources and real-world examples are especially appreciated.

## Deploy

Hosted on GitHub Pages from `main` (root). Any push rebuilds the site automatically:

```bash
git add -A && git commit -m "your message" && git push
```

---

Collated by [Doubleword](https://doubleword.ai), who ❤️ open source.
