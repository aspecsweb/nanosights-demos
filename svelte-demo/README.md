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

#### Install package

```bash
npm install nano-analytics
```

#### Import in your `src/routes/+layout.svelte`

```html
<script lang="ts">
  import 'nano-analytics';
</script>
```

#### Embed the element in your `src/routes/+layout.svelte`

```html
<nano-analytics
  projectKey="YOUR_PROJECT_KEY"
  userId="USER_ID"
/>
```

### NanoInsights

Works out of the box.

#### Install package

```bash
npm install nano-insights
```

#### Import in your `src/routes/+layout.svelte`

```html
<script lang="ts">
  import 'nano-insights';
</script>
```

#### Embed the element in your `src/routes/+layout.svelte`

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
  userId="USER_ID"
/>
```

### NanoCustom

Works out of the box.

#### Install package

```bash
npm install nano-custom
```

#### Import in your `src/routes/+layout.svelt`

```html
<script lang="ts">
  import 'nano-custom';
</script>
```

#### Embed the element in your `src/routes/+layout.svelt`

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
  userId="USER_ID"
/>
```

#### Use the track function in `*.svelte` components

```html
<script lang="ts">
  let sendEvent = () => {
    if (typeof track === 'function') {
      track('CTA');
    }
  };
</script>

<button on:click={sendEvent}>Track CTA</button>
```
