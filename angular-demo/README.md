# NanoSights + Angular

This example showcases how to integrate [NanoSights](https://www.nanosights.dev) into an Angular app using TypeScript and modular components.

- 🔗 **Live Demo:** www.angular.nanosights.dev  
- 🎥 **YouTube Walkthrough:** [Watch](https://www.youtube.com/watch?v=TvVNuH3hUkg)
- 📚 **Docs Page:** [Docs](https://www.nanosights.dev/docs)

---

## 📄 Quick Start

```bash
npm install
ng serve
```

## 📦 Usage in your own project

`Custom elements` requrie the `component` to import [CUSTOM_ELEMENTS_SCHEMA](https://angular.dev/api/core/CUSTOM_ELEMENTS_SCHEMA).

In every component you use any of the nano-tags you will need to do the following:

```typescript
import { CUSTOM_ELEMENTS_SCHEMA } from '@angular/core';

@Component({
  // ...
  schemas: [CUSTOM_ELEMENTS_SCHEMA],
  // ...
})
```

### NanoAnalytics

Works out of the box.

#### Install package

```bash
npm install nano-analytics
```

#### Import in your `src/app/app.component.ts`

```ts
import "nano-analytics"
```

#### Embed the element in your `src/app/app.component.html`

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

#### Import in your `src/app/app.component.ts`

```ts
import "nano-insights"
```

#### Embed the element in your `src/app/app.component.html`

```html
<nano-insights
  projectKey="YOUR_PROJECT_KEY"
/>
```

### NanoCustom

Requires an extra step to make the `track` function available in the `component`.

#### Install package

```bash
npm install nano-custom
```

#### Import in your `src/app/app.component.ts`

```ts
import "nano-custom"

export class Component {
  // Expose track function as method on component.
  track(eventName: string, eventData?: Record<string, string>) {
    track(eventName, eventData);
  }
}
```

#### Embed the element in your `src/app/app.component.html`

```html
<nano-custom
  projectKey="YOUR_PROJECT_KEY"
/>
```

#### Use the track function in `src/app/app.component.html`

```html
<button (click)="track('Tracks')">Track</button>
```
