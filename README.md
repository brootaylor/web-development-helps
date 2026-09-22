# Web Development Helps

> This is a living document — updated as often as possible to keep the helps, references, and resources below current and relevant.

A reference for building on the web platform itself — HTML, CSS, and JavaScript as browsers actually implement them, plus the media, performance, and accessibility practices that go with them — with no frameworks or abstractions layered on top. Each topic below is a short pointer to the best resource I've found on it, not a full explanation in itself.

## Contents

- [HTML](#html)
- [CSS](#css)
- [JavaScript](#javascript)
- [Media](#media)
- [Performance](#performance)
- [Accessibility](#accessibility)
- [My Resources](#my-resources)

## HTML

### Semantic elements

Picking the right element (`<article>`, `<nav>`, `<section>`, `<aside>`...) instead of a generic `<div>` for everything gives structure meaning to browsers, screen readers, and search engines.

- [Periodic Table of HTML Elements](https://blog.alena.rocks/en/artifacts/html-elements/) — all 115 elements laid out by category, great for spotting ones you've forgotten exist
- [HTML elements reference (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)
- [Semantic HTML (web.dev)](https://web.dev/learn/html/semantic-html)

### Document structure & metadata

What belongs in `<head>` — title, charset, viewport, favicons, and the meta tags that control how a page is described and shared.

- [What's in the head? Web page metadata (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Webpage_metadata)
- [HEAD](https://github.com/brootaylor/HEAD) — a simple guide to HTML `<head>` elements
- [Metadata (web.dev)](https://web.dev/learn/html/metadata)

### Forms & validation

Native HTML can validate a lot of form input on its own — `required`, `pattern`, `type="email"` — before you'd reach for JavaScript.

- [Client-side form validation (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms/Form_validation)
- [Learn Forms (web.dev)](https://web.dev/learn/forms)

***

## CSS

> [Kevin Powell](https://www.kevinpowell.co/) is worth a general mention here — a genuine expert on all things CSS, and a great resource beyond any single topic below.

### Selectors & specificity

Why one rule beats another when two selectors target the same element — the ID/class/type weighting system that decides it.

- [Specificity (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade/Specificity)
- [Specificity (web.dev)](https://web.dev/learn/css/specificity)

### The box model

Content, padding, border, margin — and why `box-sizing: border-box` fixes most of the confusion around element sizing.

- [Introduction to the CSS box model (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Box_model/Introduction)
- [Box Model (web.dev)](https://web.dev/learn/css/box-model)

### Flexbox

One-dimensional layout — a single row or column — for distributing and aligning items within a container.

- [A Complete Guide to Flexbox (CSS-Tricks)](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Flexbox (web.dev)](https://web.dev/learn/css/flexbox)

### Grid

Two-dimensional layout — rows and columns together — for page-level and component-level layouts that flexbox isn't suited for.

- [A Complete Guide to CSS Grid (CSS-Tricks)](https://css-tricks.com/complete-guide-css-grid-layout/)
- [Grid (web.dev)](https://web.dev/learn/css/grid)

### Custom properties & cascade layers

Native CSS variables (`--my-color`) for values you reuse, and `@layer` for controlling which groups of rules win without fighting specificity.

- [Using CSS custom properties (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascading_variables/Using_custom_properties)
- [Cascade layers (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Cascade_layers)
- [Custom properties (web.dev)](https://web.dev/learn/css/custom-properties)

### Responsive design & media queries

Building layouts that adapt to viewport size without a framework's grid system doing it for you.

- [Responsive web design (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Responsive_Design)
- [CSS media queries (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Media_queries)
- [Media queries (web.dev)](https://web.dev/learn/design/media-queries)

***

## JavaScript

### Core language: scope, closures & `this`

The parts of native JS that feel like magic until they click — where a variable is visible from, why an inner function can still see an outer function's variables after it has returned, and what `this` is bound to depending on how a function is called.

- [Variable scope, closure (javascript.info)](https://javascript.info/closure)
- [`this` (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)
- [The "this" keyword (web.dev)](https://web.dev/learn/javascript/functions/this)

### The DOM

Selecting, creating, and modifying elements directly with `querySelector`, `createElement`, and friends — no jQuery required.

- [DOM scripting introduction (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/DOM_scripting)

### Events

Listening and reacting to what happens on a page — clicks, input, keypresses — with `addEventListener`.

- [Introduction to events (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Events)

### Async JS: promises & `async`/`await`

Handling things that don't finish immediately — fetch requests, timers — without nesting callbacks.

- [Promise (javascript.info)](https://javascript.info/promise-basics)
- [Async/await (javascript.info)](https://javascript.info/async-await)

### ES modules

Splitting code across files with native `import`/`export` — no bundler required for the browser to understand it.

- [JavaScript modules (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules)

***

## Media

### Responsive images

Serving the right image — size, resolution, even a different crop — for the viewport and device requesting it, with `srcset`, `sizes`, and `<picture>`.

- [Using responsive images in HTML (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Responsive_images)
- [Responsive images (web.dev)](https://web.dev/learn/images/responsive-images)

### Image formats & lazy loading

Modern compressed formats like WebP and AVIF beat JPEG/PNG on file size, and the native `loading="lazy"` attribute defers offscreen images without a library.

- [Image formats: WebP (web.dev)](https://web.dev/learn/images/webp)
- [Image formats: AVIF (web.dev)](https://web.dev/learn/images/avif)
- [Lazy loading (MDN)](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/Lazy_loading)

### Native video & audio

The `<video>` and `<audio>` elements, `<source>` for format fallbacks, and `<track>` for captions/subtitles — no video.js or other player library required.

- [HTML video and audio (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_video_and_audio)
- [Audio and video (web.dev)](https://web.dev/learn/html/audio-video)

***

## Performance

### The critical rendering path & resource loading

How the browser goes from HTML/CSS/JS to pixels on screen, and what blocks it along the way — the foundation for most other performance work.

- [Understand the critical path (web.dev)](https://web.dev/learn/performance/understanding-the-critical-path)
- [Optimize resource loading (web.dev)](https://web.dev/learn/performance/optimize-resource-loading)

### Resource hints

Giving the browser a head start with `preconnect`, `preload`, and `prefetch` — without a bundler or framework doing it automatically.

- [Assist the browser with resource hints (web.dev)](https://web.dev/learn/performance/resource-hints)

### Web fonts

Fonts are often the biggest render-blocking resource on a page — `font-display`, self-hosting, and subsetting fix most of it.

- [Optimize web fonts (web.dev)](https://web.dev/learn/performance/optimize-web-fonts)

### JavaScript: code-splitting

Loading only the JavaScript a page actually needs upfront, using native dynamic `import()`.

- [Code-split JavaScript (web.dev)](https://web.dev/learn/performance/code-split-javascript)

### Core Web Vitals

The three field metrics — LCP, INP, CLS — Google uses to measure real-world loading speed, responsiveness, and visual stability.

- [Web Vitals (web.dev)](https://web.dev/articles/vitals)

***

## Accessibility

### Semantic HTML & ARIA

The first rule of ARIA is not to use it — reach for the right native element before reaching for ARIA attributes on a `<div>`.

- [ARIA and HTML (web.dev)](https://web.dev/learn/accessibility/aria-html)

### Keyboard focus

Making sure everything reachable with a mouse is also reachable — and visibly focused — with just a keyboard.

- [Keyboard focus (web.dev)](https://web.dev/learn/accessibility/focus)

### Color & contrast

Meeting WCAG contrast ratios, and respecting `prefers-color-scheme`/`prefers-contrast` for users with low vision or color blindness.

- [Color and contrast (web.dev)](https://web.dev/learn/accessibility/color-contrast)

### Accessible forms

Labels, descriptions, and error messages connected to their fields programmatically, not just visually.

- [Forms (web.dev)](https://web.dev/learn/accessibility/forms)

***

## My Resources

> A running, personal collection of the tools, references, and people I follow for front-end work — kept separately and updated over time.

- [My Web Development Resources 2026](https://brootaylor.com/writing/2026-09-13/my-frontend-resources-2026)

***
