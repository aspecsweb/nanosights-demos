# NanoSights + Svelte

This example shows how to use [NanoSights](https://www.nanosights.dev) in a site built with Svelte.

- 🔗 **Live Demo:** www.astro.nanosights.dev  
- 🎥 **YouTube Walkthrough:**
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

_in `src/routes/+layout.svelte`_

```html
<script lang="ts">
  import 'nano-analytics';
</script>
```

#### Embed the element

_in `src/routes/+layout.svelte`_

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

_in `src/routes/+layout.svelte`_

```html
<script lang="ts">
  import 'nano-insights';
</script>
```

#### Embed the element

_in `src/routes/+layout.svelte`_

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Requires an extra step because Svelte’s module-scoped `<script>` doesn’t expose global functions like track automatically.

#### Install the package

```bash
npm install nano-custom
```

#### Import the module

_in `src/routes/+layout.svelt`_

```html
<script lang="ts">
  import 'nano-custom';
</script>
```

#### Embed the element

_in `src/routes/+layout.svelt`_

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Use the track function

_in `*.svelte` components_

```html
<script lang="ts">
  let sendEvent = () => {
    if (typeof track === 'function') {
      track('CTA');
    }
  };
</script>

<button on:click={sendEvent}>
  Track CTA
</button>
```
