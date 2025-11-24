# FrissBee Accordion

This repo contains an accordion that is very easy to implement in your own website.

It can be visually adapted to your own site with attributes or CSS `::part()`.

The repo contains all the necessary files and various examples for illustration.

The accordion is programmed in JavaScript with Web Component.

Individual accordions are completely independent of each other.

## Preview

[You can view the demo here](https://accordion.frissbee.de/)

## Implementation

```html
<!DOCTYPE html>
<html lang="de">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- implement the "frissbee-accordion_v.1.1.0.js" file => use "defer" -->
    <script src="./assets/js/frissbee-accordion_v.1.1.0.js" defer></script>
  </head>
  <body>
    <!-- Implement the frissbee-accordion tag and set the title of the accordion with the "acc-title" attribute. -->
    <frissbee-accordion acc-title="My title">
      <!-- Insert the desired HTML within the frissbee-accordion tag. -->
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    </frissbee-accordion>

    <!-- Example with all attributes -->
    <frissbee-accordion
      acc-title="My title"
      color-title="#fff"
      bg-title="#3c91c9"
      bg-text="#f0f0f0"
      border-style="8px solid #fff"
      border-radius="8px"
      margin-bottom="8px"
      title-size="22px"
      title-font-family="Segoe UI"
      padding-acc="8px 40px"
      is-title-bold
      is-active
    >
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    </frissbee-accordion>
  </body>
</html>
```

## Attributes

- `acc-title`
  - => Title of the accordion. **Default:** empty string
- `color-title`
  - => Color of the title text. **Default:** `#444`
- `bg-title`
  - => Background color of the Title. **Default:** `#f1f1f1'`
- `bg-text`
  - => Background color of the text within the `frissbee-accordion` HTML tag. **Default:** `#fff'`
- `border-style`
  - => Style of the border. **Default:** `1px solid #dedede`
- `border-radius`
  - => Radius of the border. **Default:** `0px`
- `margin-bottom`
  - => Bottom distance. **Default:** `0px`
- `title-size`
  - => Size of the title text. **Default:** `16px`
- `title-font-family`
  - => Font family of the title. **Default:** `Verdana, Geneva, Tahoma, sans-serif;`
- `padding-acc`
  - => Inside spacing of the text in the `frissbee-accordion` HTML tag. **Default:** `18px`
- `is-title-bold`
  - => Set the title to bold. **Default:** not set. No value necessary.
- `is-active`
  - => If this attribute is set, the accordion is open when the website is opened. **Default:** not set. No value necessary.

## Functions

The following functions are not necessary for integrating the Accordion into the website. However, if you integrate the Accordion into your own project, they can be used for this purpose.

- `addIsActive()`
  - => opens the accordion
- `removeIsActive()`
  - => closes the accordion
- `addTitleIsBold()`
  - => adds the `is-title-bold` attribute
- `removeTitleIsBold()`
  - => remove the `is-title-bold` attribute
- `setTitle(title)`
  - => sets the title of the accordion
- `setText(text)`
  - => sets the text of the accordion
- `getScrollHeight()`
  - => returns the height of the accordion when it is opened
- `getMaxHeight()`
  - => returns the height of the accordion when it is open
- `setMaxHeight()`
  - => sets the height of the accordion

## Style with CSS `::part()`

### parts:

- `container-accordion`
- `btn-title`
- `container-panel`
- `panel-accordion`

Example:

```css
frissbee-accordion::part(container-accordion) {
  margin-bottom: 18px;
  border: 3px solid #383838;
  border-radius: 8px;
}
frissbee-accordion::part(btn-title) {
  font-family: 'Tahoma';
  color: #383838;
  background-color: #56ca65;
  font-size: 24px;
  padding: 4px 22px;
  font-weight: bold;
}
frissbee-accordion::part(container-panel) {
  background-color: #e9fde7;
}
frissbee-accordion::part(panel-accordion) {
  padding: 22px 22px;
}
```
