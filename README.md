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

It has a header with a theme toggle, a hero section with two buttons, a features section with four cards, and a footer.

The four features are quick entry, a weekly view, offline logging and CSV export. The copy is placeholder text for a product that doesn't exist, and the email address in the footer is a dummy one.

## Responsive layout

The layout is written mobile first and changes at two widths.

| Screen | Features | Hero buttons |
| --- | --- | --- |
| Under 600px | 1 column | Stacked |
| 600px and up | 2 columns | Side by side |
| 900px and up | 4 columns | Side by side, larger hero |

## Theming

Both pages use the same Gruvbox colors, stored as CSS variables in `:root`. The dark values are set under `:root[data-theme="dark"]`.

A small script in the `<head>` sets `data-theme` on the `<html>` element before the page paints. It uses the theme saved in `localStorage` if there is one, and the system light or dark setting otherwise. The landing page has a ◐ button that switches the theme and saves the choice. The front page has no button and follows the saved or system setting.

To change the colors, edit the variables at the top of each `style.css`.

## Changing the content

- Product name and copy: edit `landing/index.html`.
- Features: copy or remove an `<article class="feature">` block. The grid adjusts on its own, though four cards fill the desktop row evenly.
- Front page image: replace `runner-light.png` and `runner-dark.png` with your own. Transparent PNGs work best because they sit on the theme background.
