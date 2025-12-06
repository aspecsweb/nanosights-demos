# NanoSights + Webpack

This webpack setup shows how to use [NanoSights](https://www.nanosights.dev) in a fully type-safe TypeScript environment.

- 🔗 **Live Demo:** www.webpack.nanosights.dev  
- 🎥 **YouTube Walkthrough:**  
- 📚 **Docs Page:** [Docs](https://www.nanosights.dev/docs)

---

## 📄 Quick Start

```bash
npm install
npm start
```

## 📦 Usage in your own project

### NanoAnalytics

Works out of the box.

#### Install the package

```bash
npm install nano-analytics
```

#### Import the module

_in `index.ts`_

```ts
import "nano-analytics"
```

#### Embed the element

_in `src/index.html`_

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

_in `src/index._ts`

```ts
import "nano-insights"
```

#### Embed the element

_in `index.html`_

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Requires additional steps for TypeScript to recognize the module and locate the `track` function.

#### Install the package

```bash
npm install nano-custom
```

#### Import the module

_in `index.ts`_

```ts
import "nano-custom"
```

#### Embed the element

_in `index.html`_

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Assign the track function to the global window object

_in `index.ts`_

```ts
(window as any).track = track;
```

#### Use the track function

_in `*.html` files_

```html
<button onclick="track('CTA')">
  Track
</button>
```
