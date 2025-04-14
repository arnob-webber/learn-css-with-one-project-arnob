<h1>Learn CSS with one single project.</h1>


### **1. Introduction to CSS**
#### What is CSS?
CSS (Cascading Style Sheets) is a language used to style and format HTML documents. It controls how elements look on a webpage, including colors, fonts, spacing, and layout etc.

#### How CSS Works:
- CSS applies styles to HTML elements using rules.
- A CSS rule consists of:
  - **Selector**: Targets an HTML element ( `h1`, `.class`, `#id`).
  - **Declaration Block**: Contains one or more declarations inside curly braces `{}`.
    - Each declaration has a **property** (`color`) and a **value** (`red`).

Example:
```css
h1 {
  color: blue;
  font-size: 24px;
}
```

#### Linking CSS to HTML:
There are three ways to apply CSS:
1. **Inline CSS** (not recommended for large projects):
   ```html
   <h1 style="color: red;">Hello World</h1>
   ```
2. **Internal CSS** (within `<style>` tags in the `<head>` section):
   ```html
   <style>
     h1 {
       color: green;
     }
   </style>
   ```
3. **External CSS** (recommended for reusability):
   - Create a file named `styles.css`:
     ```css
     h1 {
       color: purple;
     }
     ```
   - Link it in your HTML:
     ```html
     <link rel="stylesheet" href="styles.css">
     ```

---

### **2. Selectors & Syntax**
Selectors determine which HTML elements are styled. Here are the main types:

#### Element Selector:
Targets all instances of an HTML element.
```css
p {
  color: teal;
}
```

#### Class Selector:
Applies styles to elements with a specific class (`class="example"`).
```css
.example {
  background-color: yellow;
}
```

#### ID Selector:
Applies styles to a single element with a unique ID (`id="unique"`).
```css
#unique {
  border: 2px solid black;
}
```

#### Combinators:
Combine selectors for more precise targeting:
- **Descendant Selector**: `div p` targets `<p>` inside `<div>`.
- **Child Selector**: `div > p` targets direct children `<p>` of `<div>`.
- **Adjacent Sibling**: `h1 + p` targets `<p>` immediately after `<h1>`.

#### Pseudo-Classes & Pseudo-Elements:
- **Pseudo-Classes**: Target specific states of an element (`:hover`).
  ```css
  a:hover {
    color: orange;
  }
  ```
- **Pseudo-Elements**: Style specific parts of an element (`::first-line`).
  ```css
  p::first-line {
    font-weight: bold;
  }
  ```

---

### **3. Box Model**
Every HTML element is treated as a box with four layers:
1. **Content**: The actual text or image.
2. **Padding**: Space between content and border.
3. **Border**: Surrounds padding and content.
4. **Margin**: Space outside the border.

Example:
```css
div {
  width: 200px;
  padding: 10px;
  border: 5px solid black;
  margin: 20px;
}
```

You can also use `box-sizing: border-box;` to include padding and border in the element's total width/height.

---

### **4. Colors & Units**
#### Colors:
- **Hexadecimal**: `#RRGGBB` (e.g., `#ff5733`).
- **RGB**: `rgb(255, 87, 51)`.
- **HSL**: `hsl(9, 100%, 60%)`.

#### Units:
- **Absolute Units**: `px` (pixels), `pt` (points).
- **Relative Units**:
  - `em`: Relative to parent's font size.
  - `rem`: Relative to root (`<html>`) font size.
  - `%`: Percentage of parent's size.
  - `vh`/`vw`: Viewport height/width percentage.

---

### **5. Typography**
Control text appearance:
```css
body {
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.5;
  text-align: center;
  letter-spacing: 2px;
}
```

---

### **6. Positioning & Display**
#### Positioning:
- `static`: Default position.
- `relative`: Positioned relative to its normal position.
- `absolute`: Positioned relative to the nearest positioned ancestor.
- `fixed`: Stays fixed relative to the viewport.
- `sticky`: Toggles between `relative` and `fixed`.

#### Display:
- `block`: Takes up full width (`<div>`).
- `inline`: Takes up only necessary width (`<span>`).
- `flex`: Enables flexible layouts.
- `grid`: Enables grid-based layouts.

---

### **7. Flexbox**
Flexbox is ideal for one-dimensional layouts (rows or columns).

Example:
```css
.container {
  display: flex;
  justify-content: space-between; /* Horizontal alignment */
  align-items: center; /* Vertical alignment */
}
```

---

### **8. Grid Layout**
Grid is perfect for two-dimensional layouts (rows and columns).

Example:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /* Three equal columns */
  gap: 10px; /* Spacing between items */
}
```

---

### **9. Responsive Design**
Make your site adapt to different screen sizes:
- Use **media queries**:
  ```css
  @media (max-width: 768px) {
    body {
      font-size: 14px;
    }
  }
  ```
- Use **viewport units** (`vw`, `vh`) and **mobile-first design** principles.

---

### **10. Transitions & Animations**
#### Transitions:
Smooth changes between states:
```css
button {
  transition: background-color 0.3s ease;
}
button:hover {
  background-color: blue;
}
```

#### Animations:
Use `@keyframes` for complex animations:
```css
@keyframes slide {
  from { transform: translateX(0); }
  to { transform: translateX(100px); }
}
.box {
  animation: slide 2s infinite;
}
```

---

### **11. Transforms**
Modify elements visually:
```css
img {
  transform: rotate(45deg) scale(1.5);
}
```

---

### **12. Z-Index & Stacking Context**
Control overlapping elements:
```css
.box1 {
  z-index: 2;
  position: relative;
}
.box2 {
  z-index: 1;
  position: relative;
}
```

---

### **13. Pseudo-Elements & Classes**
Style specific parts of elements:
```css
p::first-letter {
  font-size: 2em;
}
p::after {
  content: " (End)";
}
```

---

### **14. Variables & Functions**
#### Variables:
Reusable values:
```css
:root {
  --primary-color: #3498db;
}
button {
  background-color: var(--primary-color);
}
```

#### Functions:
Dynamic calculations:
```css
div {
  width: calc(100% - 20px);
}
```

---
