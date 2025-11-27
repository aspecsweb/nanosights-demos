# NanoSights + Vanilla JS & HTML

This example shows how to use [NanoSights](https://www.nanosights.dev) in a plain HTML and JavaScript site.

- 🔗 **Live Demo:** www.html.nanosights.dev
- 🎥 **YouTube Walkthrough:** [Watch](https://www.youtube.com/watch?v=todo)
- 📚 **Docs Page:** [Docs](https://www.nanosights.dev/docs)

---

## 📄 Quick Start

Use a local dev Server like [Live Server](https://github.com/ritwickdey/vscode-live-server-plus-plus) to start the project.

## 📦 Usage in your own project

### NanoAnalytics

Works out of the box with [CDN](https://www.nanosights.dev/docs/tags/analytics/cdn).

#### Link to a CDN in your `index.html`

```html
<script type="module">
  import nanoAnalytics from "https://cdn.jsdelivr.net/npm/nano-analytics@1.0.0 +esm";
</script>
```

#### Embed the element in your `index.html`

```html
<nano-analytics projectKey="YOUR_PROJECT_KEY" userId="USER_ID" />
```
