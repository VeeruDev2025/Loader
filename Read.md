# 3D Flipping Text Loader Documentation

## Overview

This loader creates a 3D flipping text animation that spells "LOADING" with each letter rotating independently. The animation features Google-inspired colors and a smooth 3D flipping effect.

## Features

- **3D Flipping Animation**: Each letter rotates 360 degrees on the X-axis
- **Google Color Palette**: Uses Google's brand colors (#4285f4, #db4437, #f4b400, #0f9d58) plus complementary colors
- **Staggered Timing**: Letters animate sequentially with 0.1s delay between each
- **Responsive Design**: Centers vertically and horizontally in the viewport
- **Clean Typography**: Uses monospace font for a technical look

## HTML Structure

```html
<div id="box">
  <div>L</div>
  <div>O</div>
  <div>A</div>
  <div>D</div>
  <div>I</div>
  <div>N</div>
  <div>G</div>
</div>
```

## CSS Implementation

```css
#box {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

#box div {
  display: inline-block;
  margin: 5px;
  font-size: 35px;
  font-weight: bold;
  font-family: "Courier New", Courier, monospace;
  animation: 2s obrot linear infinite;
}

/* Animation */
@keyframes obrot {
  0% {
    transform: rotateX(0);
  }
  12.5% {
    transform: rotateX(90deg);
  }
  25% {
    transform: rotateX(180deg);
  }
  37.5% {
    transform: rotateX(270deg);
  }
  50% {
    transform: rotateX(360deg);
  }
  100% {
    transform: rotateX(360deg);
  }
}

/* Color Assignment */
#box div:nth-child(1) {
  color: #db4437;
  animation-delay: 0s;
}
#box div:nth-child(2) {
  color: #4285f4;
  animation-delay: 0.1s;
}
#box div:nth-child(3) {
  color: #f4b400;
  animation-delay: 0.2s;
}
#box div:nth-child(4) {
  color: #0f9d58;
  animation-delay: 0.3s;
}
#box div:nth-child(5) {
  color: #9e69af;
  animation-delay: 0.4s;
}
#box div:nth-child(6) {
  color: #ff6f42;
  animation-delay: 0.5s;
}
#box div:nth-child(7) {
  color: #009688;
  animation-delay: 0.6s;
}
```

## Customization Options

### Change Colors

Modify the color values in the nth-child selectors to create different color schemes:

```css
#box div:nth-child(1) {
  color: #your-color;
}
```

### Adjust Animation

- **Speed**: Change the animation duration (currently 2s)
- **Timing**: Adjust the animation-delay values (currently 0.1s increments)
- **Effect**: Modify the transform properties in the @keyframes

### Size Adjustments

- Change `font-size` to make letters larger/smaller
- Adjust `margin` to change spacing between letters
- Modify the container `height` as needed

## Browser Compatibility

Works on all modern browsers that support CSS3 transforms and animations. For best results, use:

- Chrome 36+
- Firefox 16+
- Safari 9+
- Edge 12+
- Opera 23+

## Performance Notes

- Uses hardware-accelerated CSS transforms for smooth animation
- Lightweight implementation (no JavaScript required)
- Minimal repaints/reflows for optimal performance

## Use Cases

- Loading screens
- Page transitions
- Process indicators
- Loading states in web applications
