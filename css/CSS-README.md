
# CSS Basics Cheat Sheet

## What is CSS?

CSS stands for **Cascading Style Sheets**.  
It is used to style and layout web pages—to change colors, fonts, spacing, positioning, and more.

---

## How CSS Works

- **HTML** builds the structure/content.
- **CSS** makes it look nice.

### Ways to Add CSS

1. **Inline (inside HTML tag):**
    ```html
    <p style="color: blue;">This is blue text.</p>
    ```

2. **Internal (in `<style>` tag inside `<head>`):**
    ```html
    <head>
      <style>
        p {
          color: blue;
        }
      </style>
    </head>
    ```

3. **External (best way):**
    - Create a file called `style.css`.
    - Link it in your HTML:
      ```html
      <link rel="stylesheet" href="style.css" />
      ```

---

## CSS Syntax

```css
selector {
  property: value;
}
```

**Example:**
```css
h1 {
  color: red;
  font-size: 36px;
}
```
This will make all `<h1>` tags red and big.

---

## Common CSS Properties

| Property      | What it Does            | Example                |
|---------------|------------------------|------------------------|
| color         | Text color              | `color: green;`        |
| background    | Background color/image  | `background: yellow;`  |
| font-size     | Text size               | `font-size: 20px;`     |
| font-family   | Font type               | `font-family: Arial;`  |
| margin        | Space outside element   | `margin: 10px;`        |
| padding       | Space inside element    | `padding: 15px;`       |
| border        | Border around element   | `border: 1px solid;`   |
| width/height  | Size of element         | `width: 300px;`        |
| text-align    | Aligns text             | `text-align: center;`  |

---

## CSS Selectors

- **Element Selector**
    ```css
    p { color: red; }
    ```
- **Class Selector**
    ```css
    .intro { font-weight: bold; }
    ```
    Use in HTML: `<p class="intro">Hello!</p>`
- **ID Selector**
    ```css
    #header { background: #333; color: white; }
    ```
    Use in HTML: `<div id="header">...</div>`
- **Group Selector**
    ```css
    h1, h2, h3 { font-family: Arial; }
    ```

---

## Example: Simple HTML + CSS

**index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>CSS Example</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <h1>Welcome!</h1>
  <p class="intro">CSS makes web pages beautiful.</p>
</body>
</html>
```

**style.css**
```css
body {
  background: #f9f9f9;
}

h1 {
  color: #4CAF50;
  text-align: center;
}

.intro {
  font-size: 22px;
  color: #333;
  text-align: center;
}
```

---
