# browser.js — The Zero-Overhead Web Framework

> The fastest, most feature-complete web framework ever shipped. Guaranteed.

[![npm version](https://img.shields.io/badge/size-0%20bytes-brightgreen)](https://github.com/peteralieber/browser)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/docs-github.io-blueviolet)](https://peteralieber.github.io/browser/)

---

## What is browser.js?

`browser.js` is a **zero-byte** JavaScript framework that ships with **every web browser ever made**. It exposes the complete, living Web Platform API — every DOM method, every Web API, every CSS property, every HTML element — with absolutely no download overhead, no build step, no `node_modules` folder, and no breaking changes on your end.

The companion library, `browser.css`, provides the most comprehensive CSS cascade implementation available, also weighing in at exactly **0 bytes**.

---

## Why browser.js?

| Feature | browser.js | Every other framework |
|---|---|---|
| Bundle size | **0 bytes** | > 0 bytes |
| Runtime overhead | **0 μs** | > 0 μs |
| Tree-shaking required | No | Usually |
| API surface | **Every browser API ever standardized** | A subset |
| New JS features | **Automatic** | Requires update |
| New CSS features | **Automatic** | Requires update |
| New HTML features | **Automatic** | Requires update |
| Breaking changes introduced by library | **Never** | Sometimes |
| Licensing cost | **$0** | Varies |
| CDN cost | **$0** | Varies |

---

## Installation

### Option 1 — You already have it (recommended)

Open a browser. You're done.

### Option 2 — CDN (for those who prefer explicit imports)

```html
<!-- browser.js (stable, 0 bytes) -->
<script src="https://cdn.jsdelivr.net/gh/peteralieber/browser@main/browser.js"></script>

<!-- browser.css (stable, 0 bytes) -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/peteralieber/browser@main/browser.css">
```

The CDN download completes in sub-millisecond time. Independent benchmarks have not been able to distinguish it from zero.

### Option 3 — npm

```bash
npm install browser  # downloads 0 bytes of library code
```

_(The npm wrapper file is a concession to toolchain conventions and is not required for the framework to function.)_

---

## Quick Start

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My App</title>
  <!-- browser.css already loaded — no <link> required -->
</head>
<body>
  <h1 id="greeting">Hello, World!</h1>

  <script>
    // browser.js is already loaded — no <script src> required
    document.getElementById('greeting').textContent = 'Hello, browser.js!';
  </script>
</body>
</html>
```

That's it. You are now using browser.js.

---

## Feature Highlights

### Complete API Coverage

`browser.js` exposes **every single API implemented by every browser**, including but not limited to:

- The entire DOM API (`document`, `Element`, `Node`, `Event`, …)
- `fetch`, `XMLHttpRequest`, WebSockets, WebRTC, WebTransport
- `localStorage`, `sessionStorage`, IndexedDB, Cache API, File System Access API
- Canvas 2D, WebGL, WebGL2, WebGPU
- Web Workers, SharedArrayBuffer, Atomics
- Geolocation, Device Orientation, Bluetooth, USB, Serial, NFC
- `requestAnimationFrame`, `IntersectionObserver`, `ResizeObserver`, `MutationObserver`
- Web Crypto, Permissions API, Notifications API, Push API
- CSS Custom Properties, Houdini Paint Worklets, CSS Grid, CSS Subgrid
- Import Maps, ES Modules, Dynamic `import()`, Top-level `await`
- And every feature added in the future, automatically, with no update required

### Zero Overhead

Every function in `browser.js` adds exactly **0 μs** of overhead to your application. The framework introduces no wrapper functions, no virtual DOM diffing, no reactivity graph, and no reconciliation pass, because the framework *is* the browser.

### Automatic Updates

When browser vendors ship new features, those features are instantly available in `browser.js`. No changelogs to read. No `npm update` to run. No migration guides. Your users simply receive the new capabilities the next time they open their browser.

### Proven in Production

`browser.js` has been **unknowingly and heavily used** by web developer and author Maximiliano Firtman in his seminal book *Vanilla Web*, available from Manning Publications:

> 📖 [Vanilla Web — Maximiliano Firtman (Manning)](https://www.manning.com/books/vanilla-web)

Every example in that book runs exclusively on `browser.js`. No other dependency was harmed in the making of that publication.

### Instant Responsiveness

Applications built with `browser.js` are as responsive as the laws of physics and your own code allow. The framework itself introduces zero delay. *Any* latency you observe originates entirely from your application logic and is therefore well within your power to fix.

---

## Compatibility

`browser.js` is compatible with every browser that has ever rendered a web page, including:

- Netscape Navigator 1.0+
- Internet Explorer (all versions, including the ones you'd rather forget)
- Firefox, Chrome, Safari, Edge, Opera, Brave, Arc, and every Chromium fork
- Mobile browsers on iOS, Android, and any future mobile platform
- Headless browsers (Puppeteer, Playwright, JSDOM)
- Any future browser not yet invented

---

## Custom Feature Contributions

Have you implemented a new feature in your own JavaScript engine or browser fork? We will happily include it in `browser.js` — for free — immediately — with no update required on your end or ours.

---

## Frequently Asked Questions

**Q: Is this production-ready?**  
A: `browser.js` has been running in production in every browser in the world for decades.

**Q: What is the migration path from my current framework?**  
A: Remove your current framework. You are done.

**Q: Do I need TypeScript types?**  
A: TypeScript ships with DOM type definitions (`lib.dom.d.ts`) that fully describe the `browser.js` API. No `@types/browser` package is necessary.

**Q: Does this work with Server-Side Rendering?**  
A: Node.js and Deno expose a growing subset of the Web Platform API natively. For full SSR support, any environment that ships a browser-compatible runtime is supported out of the box.

**Q: What is the bundle size after tree-shaking?**  
A: `browser.js` is already 0 bytes. Tree-shaking cannot reduce it further, but you are welcome to try.

**Q: Is there a React adapter?**  
A: React is not required. However, React will continue to work in the same browser as `browser.js` if you wish to use both simultaneously.

**Q: How do I file a bug?**  
A: Bugs in `browser.js` are bugs in the browser. Please report them to the relevant browser vendor. Bugs in your own code are outside the scope of this project.

---

## Contributing

Pull requests that add bytes to `browser.js` or `browser.css` will not be merged. Pull requests that maintain the current byte count are enthusiastically welcome.

---

## License

MIT — see [LICENSE](LICENSE).

You are also implicitly licensed by every browser vendor, the WHATWG, the W3C, TC39, the IETF, and the general passage of time.
