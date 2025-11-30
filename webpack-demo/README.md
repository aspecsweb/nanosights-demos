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

#### Install package

```bash
npm install nano-analytics
```

#### Import in your `index.ts`

```ts
import "nano-analytics"
```

#### Embed the element in your `src/index.html`

```html
<nano-analytics
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoInsights

Works out of the box.

#### Install package

```bash
npm install nano-insights
```

#### Import in your `src/index.ts`

```ts
import "nano-insights"
```

#### Embed the element in your `index.html`

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Requires additional steps for TypeScript to recognize the module and locate the `track` function.

#### Install package

```bash
npm install nano-custom
```

#### Import in your `index.ts`

```ts
import "nano-custom"
```

#### Embed the element in your `index.html`

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Use the track function in `*.html`

```html
<button onclick="track('Tracks')">Track</button>
```

#### Assign the track function to the global window object in `index.ts`

```ts
(window as any).track = track;
```

#### Configure `tsconfig.json`

Add the following inside your `tsconfig.json`

```json
{
  "compilerOptions": {
    // ...
    "moduleResolution": "nodenext",
    "paths": {
      "nano-custom": ["node_modules/nano-custom"]
    }
  }
}
```