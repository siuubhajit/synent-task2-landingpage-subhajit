# Pacelog

Pacelog is a made-up training log app for runners. This repo holds a responsive landing page for it, written in plain HTML and CSS with no build step and no dependencies. And this website have light and dark theme.

## Files

```
index.html          front page: runner icon and a link to the landing page
style.css           styles for the front page
runner-light.png    runner icon for the light theme
runner-dark.png     runner icon for the dark theme
landing/
  index.html        the Pacelog landing page
  style.css         styles for the landing page
```

## Running it

Open `index.html` in a browser and click "Pacelog" to reach the landing page. You can also open `landing/index.html` directly. Nothing needs to be installed.

## The landing page

It has a sticky header with a mobile navigation toggle and theme switch, a hero section with two action buttons, a how-it-works section, four feature cards, a runners' reviews section, and a footer.

The four features cover quick entry, weekly summary, offline logging, and CSV export. The copy is placeholder text for a concept project, and the email address in the footer is a dummy address.(All features are dummy and not reponsive we can implement backend afterwards).

## Responsive layout

The layout is built mobile-first and adapts cleanly across different screen sizes.


## Theming

Both pages use CSS custom properties defined in `:root` and `:root[data-theme="dark"]` for easy color management.

An inline script in the `<head>` checks `localStorage` first and falls back to the user's system preferences (`prefers-color-scheme`) to apply the theme without screen flicker. Both the front splash page and the landing page include a toggle button (◐) that switches modes and saves the preference to `localStorage`.

To customize the colors, update the CSS variables at the top of each `style.css` file.

## Changing the content

- Product copy & sections: edit `landing/index.html`.
- Features & reviews: add or remove `<article class="feature">` or `<blockquote>` elements. The CSS grid adjusts automatically.
- Front page graphics: replace `runner-light.png` and `runner-dark.png` with transparent PNGs.