
# HTML Basics Cheat Sheet

---

## 1. What is HTML?
HTML stands for HyperText Markup Language.

It’s the standard language used to create and structure webpages.

HTML uses tags to describe elements like headings, paragraphs, images, links, and more.

Tags tell the browser how to display content.

---

## 2. HTML Document Structure
Every HTML document follows a basic structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Page Title</title>
  </head>
  <body>
    <!-- Visible content here -->
  </body>
</html>
```

**Explanation:**

- `<!DOCTYPE html>`  
  Declares the document as HTML5, the latest HTML standard.

- `<html lang="en">`  
  Root element of the page. The lang attribute defines the page language (English here).

- `<head>`  
  Contains meta-information (metadata) like character encoding, page title, links to stylesheets or scripts.

- `<meta charset="UTF-8" />`  
  Sets character encoding to UTF-8, supporting most characters.

- `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`  
  Makes the page responsive by controlling viewport settings on mobile devices.

- `<title>`  
  The page title shown on the browser tab.

- `<body>`  
  Contains the content visible to users.

---

## 3. HTML Elements and Tags
HTML elements usually have opening and closing tags:  
`<tagname>content</tagname>`

Some tags are self-closing (don’t wrap content):  
`<img src="image.jpg" alt="desc" />`

### Common Tags:

| Tag               | Purpose                       | Example                                      |
|-------------------|------------------------------|----------------------------------------------|
| `<h1>` to `<h6>`  | Headings from largest to smallest | `<h1>Heading 1</h1>`                     |
| `<p>`             | Paragraph text                | `<p>This is a paragraph.</p>`                |
| `<a>`             | Hyperlink                     | `<a href="https://example.com">Link</a>`     |
| `<img>`           | Image                         | `<img src="pic.jpg" alt="Description" />`    |
| `<ul>`, `<ol>`, `<li>` | Lists (unordered and ordered) | `<ul><li>Item 1</li></ul>`              |
| `<div>`           | Generic block container       | `<div class="container"></div>`              |
| `<span>`          | Generic inline container      | `<span style="color:red;">Text</span>`       |
| `<br />`          | Line break                    | `First line<br />Second line`                |
| `<hr />`          | Horizontal rule (line)        | `<hr />`                                     |

---

## 4. Attributes

Attributes provide extra info about elements, placed inside the opening tag.

**Syntax:** `<tag attribute="value">`

### Common Attributes:

| Attribute | Usage                        | Example                                               |
|-----------|------------------------------|-------------------------------------------------------|
| href      | URL for links                | `<a href="https://google.com">Google</a>`             |
| src       | Source URL for images, videos| `<img src="image.png" alt="desc" />`                  |
| alt       | Alternate text for images    | `<img src="pic.jpg" alt="Sunset" />`                  |
| id        | Unique identifier            | `<div id="header"></div>`                             |
| class     | Class name for CSS or JS     | `<p class="intro"></p>`                               |
| style     | Inline CSS styles            | `<p style="color: blue;">Text</p>`                    |
| title     | Tooltip text on hover        | `<abbr title="HyperText Markup Language">HTML</abbr>` |
| target    | Where to open link           | `<a href="#" target="_blank">Link</a>`                |

---

## 5. Semantic HTML Elements

Semantic elements describe the meaning of content, improving SEO and accessibility.

| Element      | Purpose                      | Example                                       |
|--------------|------------------------------|-----------------------------------------------|
| `<header>`   | Page or section header       | `<header><h1>Site Title</h1></header>`        |
| `<nav>`      | Navigation menu              | `<nav><ul><li>Home</li></ul></nav>`           |
| `<main>`     | Main content area            | `<main><article>...</article></main>`         |
| `<section>`  | Section of a page            | `<section><h2>Topic</h2><p>Details</p></section>` |
| `<article>`  | Independent content block    | `<article><h3>Post Title</h3><p>Content</p></article>` |
| `<aside>`    | Sidebar or related content   | `<aside>Related links</aside>`                 |
| `<footer>`   | Page or section footer       | `<footer>Copyright info</footer>`              |

---

## 6. Lists

**Unordered list: Bullets**
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

**Ordered list: Numbers**
```html
<ol>
  <li>First</li>
  <li>Second</li>
</ol>
```

**Description list: Terms and definitions**
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
</dl>
```

---

## 7. Links and Images

**Link syntax:**
```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Visit Example</a>
```
- `target="_blank"` opens link in a new tab.
- `rel="noopener noreferrer"` adds security for new tabs.

**Image syntax:**
```html
<img src="https://via.placeholder.com/150" alt="Placeholder image" />
```
- Always add descriptive alt text for accessibility.

---

## 8. Forms and Input Elements

Used to collect user input and send it to servers.

```html
<form action="/submit" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" />

  <label>Gender:</label>
  <input type="radio" id="male" name="gender" value="male" />
  <label for="male">Male</label>

  <input type="checkbox" id="subscribe" name="subscribe" />
  <label for="subscribe">Subscribe to newsletter</label>

  <button type="submit">Submit</button>
</form>
```

Important tags: `<form>`, `<input>`, `<label>`, `<textarea>`, `<select>`, `<option>`, `<button>`

- `required` attribute makes fields mandatory.

---

## 9. Multimedia Elements

Embed audio and video with controls:

```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg" />
  Your browser does not support the audio element.
</audio>

<video width="320" height="240" controls>
  <source src="video.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>
```

---

## 10. HTML5 APIs and New Elements

**Canvas for drawing graphics:**
```html
<canvas id="myCanvas" width="200" height="100"></canvas>
```

**SVG for vector graphics:**
```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
  <rect x="10" y="10" width="30" height="30" fill="blue" />
  <text x="50" y="90" font-size="12" text-anchor="middle" fill="black">SVG</text>
</svg>
```

**Progress bar:**
```html
<progress value="70" max="100">70%</progress>
```

---

## 11. Accessibility (A11y)

- Add `alt` to all images.
- Link `<label>` elements with form inputs (for attribute matches input id).
- Use semantic elements properly.
- Use ARIA roles when needed to clarify page structure.
- Ensure keyboard navigation (e.g., tabbing through inputs and links).

---

## 12. Best Practices

- Use lowercase for tags and attributes.
- Indent nested elements for readability.
- Close all tags properly.
- Validate your HTML using W3C Validator.
- Separate content (HTML), presentation (CSS), and behavior (JavaScript).
- Avoid deprecated tags like `<font>`, `<center>`, `<big>`.

---

## 13. Example: Complete Simple HTML Page

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Sample Page</title>
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
    <nav>
      <ul>
        <li><a href="#about">About Me</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>About Me</h2>
      <p>Hello! I am learning HTML, CSS, and JavaScript.</p>
    </section>

    <section id="projects">
      <h2>My Projects</h2>
      <ul>
        <li>Portfolio Website</li>
        <li>To-do App</li>
        <li>Blog Platform</li>
      </ul>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <form action="/submit" method="post">
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required />
        <button type="submit">Send</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 My Website</p>
  </footer>
</body>
</html>
```

---
