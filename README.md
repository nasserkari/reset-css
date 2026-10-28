# reset css

A foundational stylesheet for modern web development

## Why reset.css

- Consistent styling in every browser
- No dependencies, just one CSS file
- Low specificity, easy to override
- Predictable sizing with border-box
- Images and media scale by default
- Respects `reduced-motion-preferences`

## Usage

Save the [source](#source) as `reset.css` and load it before your other styles.

```html
<link rel="stylesheet" href="reset.css" />
```

You can also import it from css, js, jsx, ts or tsx

```css
/* css */
@import "./reset.css";
```

```js
// js, jsx, ts or tsx
import "./reset.css";
```

Put it in a layer so your own styles always win.

```css
@layer reset, token, base, components;

@import "./reset.css" layer(reset);
```

```css
@layer reset {
  /* paste reset.css here */
}
```

## Source

```css
*,
::after,
::before,
::backdrop,
::file-selector-button {
  margin: 0;
  padding: 0;
  border: 0 solid;
  box-sizing: border-box;
}

:root,
:host {
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: transparent;
}

html {
  -webkit-text-size-adjust: 100%;
  text-size-adjust: 100%;
  scrollbar-gutter: stable;
}

body {
  min-height: 100vh;
  min-height: 100dvh;
  line-height: 1.5;
  overflow-wrap: break-word;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: inherit;
  font-weight: inherit;
}

a {
  color: inherit;
  text-decoration: inherit;
}

abbr[title] {
  border-bottom: none;
  text-decoration: underline;
}

b,
strong {
  font-weight: bolder;
}

small {
  font-size: 80%;
}

sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sub {
  bottom: -0.25em;
}

sup {
  top: -0.5em;
}

pre,
code,
kbd,
samp {
  font-family: monospace;
  font-size: 1em;
}

ol,
ul,
menu {
  list-style: none;
}

img,
svg,
video,
canvas,
picture,
audio,
iframe,
embed,
object {
  display: block;
}

img,
svg,
video,
canvas,
picture {
  max-width: 100%;
  height: auto;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

button,
input,
optgroup,
select,
textarea,
::file-selector-button {
  font-family: inherit;
  font-size: 100%;
  line-height: 1.15;
  margin: 0;
}

button,
[type="button"],
[type="reset"],
[type="submit"] {
  appearance: button;
}

::file-selector-button {
  margin-inline-end: 4px;
}

textarea {
  resize: vertical;
}

:-moz-focusring {
  outline: auto;
}

@media (prefers-reduced-motion: no-preference) {
  html {
    scroll-behavior: smooth;
    interpolate-size: allow-keywords;
  }
}

@media (prefers-reduced-motion: reduce) {

  *,
  *::before,
  *::after {
    animation: none !important;
    transition: none !important;
  }
}
```
