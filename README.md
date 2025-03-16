# CSS-basic-to-advance

**CSS Guide: From Basic to Advanced**

---

## **1. Introduction to CSS**
### **What is CSS?**
CSS (Cascading Style Sheets) is a language used to describe the presentation of a document written in HTML or XML. CSS allows you to control the layout, colors, fonts, and responsiveness of a webpage.

### **How CSS Works**
CSS applies styles using selectors to target elements and define their properties. It helps separate content from presentation, allowing for more maintainable and scalable designs.

Example:
```css
h1 {
  color: blue; /* Sets the text color to blue */
  font-size: 24px; /* Increases font size */
}
```

### **Types of CSS**
- **Inline CSS** - Applied directly to an element using the `style` attribute.
- **Internal CSS** - Defined within a `<style>` tag in the HTML document.
- **External CSS** - Stored in a separate `.css` file and linked via `<link>` in the HTML.

---

## **2. CSS Selectors**
### **Basic Selectors**
Selectors allow targeting of HTML elements for styling.

- **Element Selector:** Targets HTML elements (e.g., `p`, `h1`, `div`).
- **Class Selector (`.`):** Targets elements with a specific class.
- **ID Selector (`#`):** Targets a unique element with a specific ID.
- **Universal Selector (`*`):** Targets all elements.

Example:
```css
p {
  color: red; /* All <p> elements will be red */
}
.class-name {
  font-size: 16px; /* All elements with this class will have 16px font */
}
#unique-id {
  background-color: yellow; /* Only the element with this ID will have a yellow background */
}
```

### **Combinators**
Combinators define relationships between selectors:
- **Descendant Selector (` `):** Targets elements inside another element.
- **Child Selector (`>`):** Targets direct child elements.
- **Adjacent Sibling Selector (`+`):** Targets the next sibling.
- **General Sibling Selector (`~`):** Targets all siblings.

Example:
```css
div p { color: blue; }  /* All <p> inside <div> */
div > p { color: green; } /* Direct child <p> */
h1 + p { font-weight: bold; } /* First <p> after <h1> */
```

---

## **3. CSS Box Model**
### **Theory**
The CSS Box Model describes how elements are structured and how spacing and borders affect layout. It consists of:
1. **Content** - The text or images inside an element.
2. **Padding** - Space between content and border.
3. **Border** - The surrounding edge of an element.
4. **Margin** - Space outside the border, separating elements.

Example:
```css
div {
  width: 200px;
  padding: 20px; /* Adds space inside the border */
  border: 5px solid black; /* Adds a black border */
  margin: 10px; /* Creates space outside the element */
}
```

---

## **4. CSS Positioning**
### **Theory**
CSS positioning controls where elements appear in the document.

- **Static** (default): Normal document flow.
- **Relative**: Positioned relative to its normal position.
- **Absolute**: Positioned relative to its nearest positioned ancestor.
- **Fixed**: Stays fixed in the viewport.
- **Sticky**: Toggles between relative and fixed.

Example:
```css
.fixed-box {
  position: fixed;
  top: 10px; /* Stays at 10px from the top of the viewport */
  right: 10px;
}
```

---

## **5. CSS Flexbox**
### **Theory**
Flexbox is a layout model that allows flexible alignment and distribution of elements.

- **`display: flex;`**: Enables flex container.
- **`justify-content`**: Aligns items along the main axis.
- **`align-items`**: Aligns items along the cross axis.
- **`flex-wrap`**: Controls wrapping of items.

Example:
```css
.flex-container {
  display: flex;
  justify-content: center; /* Centers items horizontally */
  align-items: center; /* Centers items vertically */
}
```

---

## **6. CSS Grid**
### **Theory**
CSS Grid is a two-dimensional layout system for structuring web pages.

- **`display: grid;`**: Enables grid container.
- **`grid-template-columns`**: Defines column layout.
- **`grid-template-rows`**: Defines row layout.
- **`gap`**: Sets spacing between grid items.

Example:
```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 10px;
}
```

---

## **7. CSS Animations & Transitions**
### **Theory**
CSS animations and transitions allow elements to change styles smoothly over time.

### **Transitions**
```css
div {
  transition: background-color 0.5s ease; /* Changes color smoothly over 0.5 seconds */
}
```

### **Animations**
```css
@keyframes example {
  from { opacity: 0; }
  to { opacity: 1; }
}

div {
  animation: example 2s infinite; /* Makes the element fade in and out */
}
```

---

## **8. Responsive Design**
### **Theory**
Responsive design ensures that web pages look good on all devices by adjusting layout dynamically.

### **Media Queries**
```css
@media (max-width: 600px) {
  body {
    background-color: lightgray;
  }
}
```

---

## **9. Advanced CSS Features**
### **CSS Variables**
```css
:root {
  --main-color: blue;
}

h1 {
  color: var(--main-color); /* Uses the CSS variable */
}
```

### **CSS Grid & Flexbox Combination**
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  display: flex;
}
```

---

## **10. CSS Pseudo-Classes & Pseudo-Elements**
### **Theory**
Pseudo-classes and pseudo-elements allow styling of elements based on state or specific parts of content.

### **Pseudo-Classes**
```css
a:hover {
  color: red; /* Changes link color when hovered */
}
```
### **Pseudo-Elements**
```css
p::first-letter {
  font-size: 30px; /* Enlarges the first letter of the paragraph */
}
```
**CSS Guide: From Basic to Advanced**

---

## **11. CSS Overflow**
### **Theory**
The `overflow` property controls how content is displayed when it exceeds the dimensions of its container.
- `visible` (default): Content overflows and is visible.
- `hidden`: Content that overflows is clipped.
- `scroll`: Adds a scrollbar to view the hidden content.
- `auto`: Adds a scrollbar only when necessary.

Example:
```css
div {
  width: 200px;
  height: 100px;
  overflow: scroll; /* Adds a scrollbar if content exceeds dimensions */
}
```

---

## **12. CSS Opacity**
### **Theory**
The `opacity` property controls the transparency of an element.
- `1` (default): Fully visible.
- `0`: Fully transparent.
- Values between `0` and `1` make the element semi-transparent.

Example:
```css
div {
  opacity: 0.5; /* Makes the element 50% transparent */
}
```

---

## **13. CSS Z-Index**
### **Theory**
The `z-index` property controls the stack order of overlapping elements.
- Higher values bring elements to the front.
- Works only on positioned elements (`relative`, `absolute`, `fixed`).

Example:
```css
div {
  position: absolute;
  z-index: 10; /* Higher value brings this element forward */
}
```

---

## **14. CSS Transform**
### **Theory**
The `transform` property applies 2D or 3D transformations like scaling, rotating, translating, and skewing elements.

Example:
```css
div {
  transform: rotate(45deg); /* Rotates the element 45 degrees */
}
```

---

## **15. CSS Transition**
### **Theory**
Transitions allow smooth changes between CSS property values.

Example:
```css
div {
  transition: background-color 0.5s ease-in-out;
}
div:hover {
  background-color: red; /* Changes color smoothly on hover */
}
```

---

## **16. CSS Animation**
### **Theory**
CSS animations allow complex animations using keyframes.

Example:
```css
@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

div {
  animation: fade-in 2s ease-in-out;
}
```

---

## **17. CSS Object-Fit**
### **Theory**
The `object-fit` property defines how images and videos fit inside a container.
- `fill` (default): Stretches content to fit.
- `contain`: Fits content within without cropping.
- `cover`: Fills the container while maintaining aspect ratio.

Example:
```css
img {
  width: 100%;
  height: 200px;
  object-fit: cover; /* Ensures the image covers the container */
}
```

---

## **18. CSS Filter**
### **Theory**
The `filter` property applies graphical effects like blur, brightness, contrast, etc.

Example:
```css
img {
  filter: grayscale(100%); /* Converts image to black and white */
}
```

---

## **19. CSS Clip-Path**
### **Theory**
The `clip-path` property clips an element to a specific shape.

Example:
```css
div {
  clip-path: circle(50%); /* Clips the element into a circle */
}
```

---

## **20. CSS Grid Auto-Fit & Auto-Fill**
### **Theory**
- `auto-fit`: Fits content dynamically within available space.
- `auto-fill`: Creates as many columns/rows as possible within the container.

Example:
```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  gap: 10px;
}
```

---

## **21. CSS Writing Mode**
### **Theory**
The `writing-mode` property controls the text flow direction.
- `horizontal-tb` (default): Left to right.
- `vertical-rl`: Top to bottom, right to left.
- `vertical-lr`: Top to bottom, left to right.

Example:
```css
p {
  writing-mode: vertical-rl;
}
```

---

## **22. CSS Scroll Snap**
### **Theory**
The `scroll-snap-type` property defines scroll behavior.

Example:
```css
.scroll-container {
  scroll-snap-type: y mandatory;
}
.scroll-item {
  scroll-snap-align: start;
}
```

---

## **23. CSS Masking**
### **Theory**
The `mask-image` property defines transparency masks.

Example:
```css
div {
  mask-image: url('mask.png');
}
```

---

## **24. CSS Aspect Ratio**
### **Theory**
The `aspect-ratio` property maintains a set width-to-height ratio.

Example:
```css
div {
  aspect-ratio: 16 / 9;
}
```

---

## **25. CSS Grid Areas**
### **Theory**
The `grid-template-areas` property defines layout areas.

Example:
```css
.grid-container {
  display: grid;
  grid-template-areas: 'header header' 'sidebar content';
}
.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
```

---


