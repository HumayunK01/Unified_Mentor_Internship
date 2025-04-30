# Responsive Portfolio Website

This project demonstrates a modern responsive portfolio website implementation using HTML and CSS. The design ensures optimal viewing and interaction experience across various devices and screen sizes.

## Key Principles Demonstrated

### 1. Mobile-First Meta Tag
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
This meta tag ensures proper scaling on mobile devices by setting the viewport width to match the device width.

### 2. Responsive Grid Layout
```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
}
```
Using CSS Grid with the `repeat()` function and `fr` units creates a flexible, responsive layout that adapts to different screen sizes.

### 3. Media Queries
```css
@media (max-width: 1024px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
```
Media queries enable responsive layout changes at specific breakpoints:
- 1024px: Changes grid to two columns
- 768px: Single column layout and vertical navigation
- 480px: Adjusts typography and spacing for mobile

### 4. Responsive Navigation
```css
nav ul {
  display: flex;
  justify-content: center;
  gap: 2rem;
}

@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    text-align: center;
  }
}
```
The navigation menu uses Flexbox to create a responsive menu that transforms into a vertical layout on mobile devices.

### 5. Fluid Card Design
```css
.card {
  background: white;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  transition: transform 0.3s;
}
```
Cards adapt to container width and feature responsive images and spacing.

## Best Practices Implemented

1. **Mobile-First Approach**: Base styles optimized for mobile with progressive enhancement
2. **Flexible Units**: Using relative units (rem, fr) instead of fixed pixels
3. **Responsive Images**: Images scale properly within their containers
4. **Progressive Enhancement**: Core content remains accessible across all devices
5. **Touch-Friendly**: Adequate spacing and sizing for touch interactions
6. **Performance**: Optimized transitions and animations
7. **Maintainable Code**: Clean, organized CSS with logical breakpoints

## Breakpoint Strategy

1. **Desktop (1024px+)**
   - Three-column grid layout
   - Full navigation menu
   - Maximum content width

2. **Tablet (768px - 1024px)**
   - Two-column grid layout
   - Adjusted spacing
   - Maintained navigation

3. **Mobile (< 768px)**
   - Single column layout
   - Vertical navigation menu
   - Optimized typography
   - Adjusted padding and margins

4. **Small Mobile (< 480px)**
   - Further reduced spacing
   - Smaller font sizes
   - Minimized padding

## How to Test Responsiveness

1. Open the website in a browser
2. Use browser developer tools (F12)
3. Toggle device toolbar (Ctrl+Shift+M)
4. Test different device presets
5. Test orientation changes
6. Manually resize the browser window

## Resources

- [MDN Web Docs - Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Media Queries](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)