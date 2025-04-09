# Responsive Web Design Principles

This project demonstrates key principles of responsive web design through a practical example. Responsive web design ensures that websites look and function well across various devices and screen sizes.

## Key Principles Demonstrated

### 1. Viewport Meta Tag
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
This essential meta tag ensures the website scales properly on mobile devices by setting the viewport width to the device width.

### 2. Fluid Grid Layout
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}
```
Using CSS Grid with relative units (fr) creates a flexible layout that adapts to different screen sizes.

### 3. Media Queries
```css
@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
  }
  nav {
    flex-direction: column;
  }
}
```
Media queries allow us to apply different styles based on screen size breakpoints:
- 768px: Changes grid to single column and navigation to vertical layout
- 480px: Adjusts font sizes and padding for smaller screens

### 4. Flexible Navigation
```css
nav {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
```
The navigation uses Flexbox to create a responsive menu that wraps on smaller screens.

### 5. Responsive Typography
```css
@media (max-width: 480px) {
  header {
    font-size: 20px;
  }
  nav a {
    font-size: 14px;
  }
}
```
Font sizes adjust based on screen size to maintain readability.

## Best Practices Implemented

1. **Mobile-First Approach**: The base styles work on mobile, with enhancements for larger screens
2. **Relative Units**: Using relative units (fr, %) instead of fixed pixels
3. **Flexible Images**: Images scale with their containers
4. **Breakpoint Strategy**: Logical breakpoints at 768px and 480px
5. **Touch-Friendly**: Adequate spacing and sizing for touch interactions

## How to Test Responsiveness

1. Open the website in a browser
2. Use browser developer tools (F12)
3. Toggle device toolbar (Ctrl+Shift+M)
4. Test different device sizes
5. Alternatively, manually resize the browser window

## Resources

- [MDN Web Docs - Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
- [CSS-Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [W3Schools - Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp) 