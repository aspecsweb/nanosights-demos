# NanoSights + Astro

This example shows how to use [NanoSights](https://www.nanosights.dev) in a content-optimized site built with Astro.

- 🔗 **Live Demo:** www.astro.nanosights.dev  
- 🎥 **YouTube Walkthrough:** [Watch](https://www.youtube.com/watch?v=ykyXX1HkMXU)
- 📚 **Docs Page:** [Docs](https://www.nanosights.dev/docs)

---

## 📄 Quick Start

```bash
npm install
npm run dev
```

## 📦 Usage in your own project

### NanoAnalytics

Works out of the box.

#### Install the package

```bash
npm install nano-analytics
```

#### Import the module

_in `src/layouts/Lauyout.astro`_

```ts
import "nano-analytics"
```

#### Embed the element

_in `src/layouts/Lauyout.astro`_

```html
<nano-analytics
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoInsights

Works out of the box.

#### Install the package

```bash
npm install nano-insights
```

#### Import the module

_in `src/layouts/Lauyout.astro`_

```ts
import "nano-insights"
```

#### Embed the element

_in `src/layouts/Lauyout.astro`_

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Works out of the box.

#### Install the package

```bash
npm install nano-custom
```

#### Import the module

_in `src/layouts/Lauyout.astro`_

```ts
import "nano-custom"
```

#### Embed the element

_in `src/layouts/Lauyout.astro`_

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Use the track function

_in `*.astro` components_

```html
<button onclick="track('Tracks')">
  Track
</button>
```
