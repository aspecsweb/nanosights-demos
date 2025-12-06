# NanoSights + Vue

This Vue example demonstrates how to plug [NanoSights](https://www.nanosights.dev) into a reactive, component-driven UI.

- 🔗 **Live Demo:** www.vue.nanosights.dev  
- 🎥 **YouTube Walkthrough:** https://www.youtube.com/watch?v=_ceO3riNmro
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

_in `src/main.ts`_

```ts
import "nano-analytics"
```

#### Embed the element

_in `src/App.vue`_

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

_in `src/main.ts`_

```ts
import "nano-insights"
```

#### Embed the element

_in `src/App.vue`_

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Requires an extra step because Vue’s `<script setup>` runs in module scope, so the global track function isn’t available automatically and must be imported explicitly.

#### Install the package

```bash
npm install nano-custom
```

#### Import the module

_in `src/main.ts`_

```ts
import 'nano-custom';
```

#### Embed the element

_in `src/App.vue`_

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Use the track function

_in `*.vue` components_

```html
<script setup lang="ts">
import { track } from 'nano-custom'
</script>

<button @click="track('CTA')">
  Track CTA
</button>
```
