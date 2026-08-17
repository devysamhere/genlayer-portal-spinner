# GenLayer Portal Spinner

A community-designed animated loading spinner for the GenLayer Portal.

Designed to be clean, lightweight, recognizable, and suitable for repeated use across loading pages and loading states throughout the Portal.

## Live Demo

**View the animated spinner:**  
https://devysamhere.github.io/genlayer-portal-spinner/

**GitHub Repository:**  
https://github.com/devysamhere/genlayer-portal-spinner

---

## Features

- Smooth infinite animation
- Official GenLayer logo at the center
- Independent rotating outer ring
- GenLayer logo rotates while smoothly zooming in and out
- Optimized for both light and dark backgrounds
- Automatic white logo treatment on dark backgrounds
- Responsive size variants
- Pure HTML + CSS
- No JavaScript required
- No external dependencies
- Accessibility support with `prefers-reduced-motion`
- Designed to remain recognizable at small UI sizes

---

## Design Concept

The GenLayer Portal Spinner combines two independent layers of motion.

The outer layer uses four segmented gradient elements that continuously rotate around the GenLayer mark.

At the center, the official GenLayer logo rotates independently while gradually scaling up and down.

The combination creates a smooth, continuous loading state while giving the animation a distinctive GenLayer identity.

The layered motion is also intended as a subtle visual reference to coordination and consensus: multiple moving elements working around a recognizable GenLayer core.

### Dark Mode

The official GenLayer logo is primarily black, which creates limited contrast against dark interfaces.

For dark backgrounds, the spinner automatically converts the logo to white and applies a subtle white/purple glow.

### Light Mode

On light backgrounds, the original black GenLayer logo is preserved for maximum contrast and brand recognition.

---

## Available Sizes

The demo includes four common UI sizes:

- **24px** — compact loading states and buttons
- **32px** — small components
- **48px** — standard loading states
- **64px** — larger components and page sections

The primary showcase also demonstrates a larger version for full-page loading states.

---

## Light & Dark Support

The spinner has been designed to work across both light and dark Portal interfaces.

### Light background

The original black GenLayer logo is displayed.

### Dark background

The logo is automatically inverted to white with a subtle glow to maintain visibility.

---

## Project Structure

```text
genlayer-portal-spinner/
├── index.html
├── spinner.css
├── genlayer-logo.svg
├── README.md
└── LICENSE
```

---

## Usage

Include the stylesheet:

```html
<link rel="stylesheet" href="spinner.css">
```

Then add the spinner markup:

```html
<div
  class="genlayer-spinner"
  role="status"
  aria-label="Loading"
>
  <div class="genlayer-spinner__ring">
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>

  <img
    class="genlayer-spinner__logo"
    src="genlayer-logo.svg"
    alt=""
  >
</div>
```

---

## Size Variants

The spinner can be used at different sizes by adding one of the provided modifier classes.

### 24px

```html
<div class="genlayer-spinner genlayer-spinner--24">
  ...
</div>
```

### 32px

```html
<div class="genlayer-spinner genlayer-spinner--32">
  ...
</div>
```

### 48px

```html
<div class="genlayer-spinner genlayer-spinner--48">
  ...
</div>
```

### 64px

```html
<div class="genlayer-spinner genlayer-spinner--64">
  ...
</div>
```

The default showcase spinner uses a larger size for page-level loading states.

---

## Animation

The spinner uses two primary CSS animations.

### Outer Ring

The segmented outer ring rotates continuously:

```css
@keyframes genlayer-spin {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
```

### GenLayer Logo

The GenLayer logo simultaneously rotates and smoothly scales up and down:

```css
@keyframes genlayer-logo-motion {
  0% {
    transform:
      rotate(0deg)
      scale(0.82);

    opacity: 0.85;
  }

  25% {
    transform:
      rotate(90deg)
      scale(0.95);

    opacity: 0.95;
  }

  50% {
    transform:
      rotate(180deg)
      scale(1.18);

    opacity: 1;
  }

  75% {
    transform:
      rotate(270deg)
      scale(0.95);

    opacity: 0.95;
  }

  100% {
    transform:
      rotate(360deg)
      scale(0.82);

    opacity: 0.85;
  }
}
```

This creates a continuous breathing/zooming effect without interrupting the rotation.

---

## Accessibility

The spinner uses:

```html
role="status"
aria-label="Loading"
```

to provide loading-state context for assistive technologies.

It also respects the user's reduced-motion preference:

```css
@media (prefers-reduced-motion: reduce)
```

When reduced motion is preferred, the animation is slowed to create a less intensive loading experience.

---

## Performance

The spinner is intentionally lightweight.

It uses:

- CSS transforms
- CSS opacity
- SVG
- HTML

It does **not** require:

- JavaScript
- animation libraries
- frameworks
- external runtime dependencies

This makes it suitable for loading states that may appear frequently throughout the Portal.

---

## Technology

- HTML5
- CSS3
- SVG

---

## Browser Support

The spinner uses standard CSS animations and transforms supported by modern browsers including:

- Chrome
- Edge
- Firefox
- Safari

---

## Intended Uses

The spinner can be used for:

- Full-page loading
- Portal navigation
- Transaction processing
- Intelligent Contract execution
- Validator/consensus waiting states
- Data fetching
- Button loading states
- Component loading
- Modal loading states

---

## Links

**Live Demo**  
https://devysamhere.github.io/genlayer-portal-spinner/

**Source Code**  
https://github.com/devysamhere/genlayer-portal-spinner

---

## License

The spinner implementation is released under the MIT License.

The GenLayer name, logo, and associated brand assets remain the property of GenLayer and are used here solely for this community design submission.

---

## Community Submission

Created as a community contribution for the **GenLayer Portal Loading Spinner** design request.

The goal is simple:

> Create a small piece of motion that can appear hundreds of times throughout the Portal while remaining smooth, recognizable, lightweight, and unmistakably GenLayer.