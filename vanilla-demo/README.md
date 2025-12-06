# NanoSights + Vanilla JS & HTML

This example shows how to use [NanoSights](https://www.nanosights.dev) in a plain HTML and JavaScript site.

- 🔗 **Live Demo:** www.html.nanosights.dev
- 🎥 **YouTube Walkthrough:** [Watch](https://www.youtube.com/watch?v=todo)
- 📚 **Docs Page:** [Docs](https://www.nanosights.dev/docs)

---

## 📄 Quick Start

Use a local dev Server like [Live Server](https://github.com/ritwickdey/vscode-live-server-plus-plus) to start the project.

## 📦 Usage in your own project

> _Don't use self-closing elements like `<nano-tag />`. Use the normal syntax `<nano-tag></nano-tag>`instead._

### NanoAnalytics

Works out of the box with [CDN](https://www.nanosights.dev/docs/tags/analytics/cdn).

#### Link to a CDN

_in `index.html`_

```html
<script type="module">
  import nanoAnalytics from "https://cdn.jsdelivr.net/npm/nano-analytics@1.1.0 +esm";
</script>
```

#### Embed the element

_in `index.html`_

```html
<nano-analytics
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoInsights

Works out of the box with [CDN](https://www.nanosights.dev/docs/tags/analytics/cdn).

#### Link to a CDN

_in `index.html`_

```html
<script type="module">
  import nanoInsights from "https://cdn.jsdelivr.net/npm/nano-insights@1.0.0/+esm";
</script>
```

#### Embed the element

_in `index.html`_

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Works out of the box with [CDN](https://www.nanosights.dev/docs/tags/analytics/cdn).

#### Link to a CDN

_in `index.html`_

```html
<script type="module">
  import nanoCustom from "https://cdn.jsdelivr.net/npm/nano-custom@1.0.0/+esm";
</script>
```

#### Embed the element

_in `index.html`_

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Use the track function

_in `*.html` files_

```html
<button onclick="track('CTA')">
  Track CTA
</button>
```
