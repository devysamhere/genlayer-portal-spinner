# GenLayer Portal Spinner

A community-designed animated loading spinner for the GenLayer Portal.

The spinner is designed to be lightweight, recognizable, and suitable for repeated use across loading pages and loading states.

## Features

- Smooth infinite animation
- Official GenLayer logo at the center
- Independent rotating outer ring
- Logo rotation with subtle zoom-in / zoom-out motion
- Works on light and dark backgrounds
- Responsive size variants
- Pure HTML + CSS
- No JavaScript required
- Accessibility support with `prefers-reduced-motion`

## Preview

The demo includes:

- Dark background version
- Light background version
- 24px spinner
- 32px spinner
- 48px spinner
- 64px spinner

## Files

```text
genlayer-portal-spinner/
├── index.html
├── spinner.css
├── genlayer-logo.svg
├── README.md
└── LICENSE

## Usage

Add the spinner markup:

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

<link rel="stylesheet" href="spinner.css">

<div class="genlayer-spinner genlayer-spinner--24">...</div>

<div class="genlayer-spinner genlayer-spinner--32">...</div>

<div class="genlayer-spinner genlayer-spinner--48">...</div>

<div class="genlayer-spinner genlayer-spinner--64">...</div>