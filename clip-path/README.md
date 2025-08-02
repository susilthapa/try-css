# 🎨 clip-path: path() Shape Example

This project demonstrates how to use the CSS `clip-path: path()` function to create a custom clipped UI shape — specifically, a horizontal bar with a notch on the top-left corner. It's a practical technique for crafting visually distinctive components using only CSS.

---

## 📐 What is `clip-path: path()`?

`clip-path: path()` is a CSS feature that lets you define complex, **SVG-style paths** to clip (mask) elements. Anything outside the defined path becomes invisible, allowing you to make non-rectangular shapes like polygons, curves, and notches.

---

## 🧩 CSS Code Example

```css
.fancy-card {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  padding: 20px;
  box-sizing: border-box;
  clip-path: path(
    "M 10,40 L 70,40 A 10,10 0,0,0 80,30 L 80,10 A 10,10 0,0,1 90,0 L 170,0 A 10,10 0,0,1 180,10 L 180,190 A 10,10 0,0,1 170,200 L 10,200 A 10,10 0,0,1 0,190 L 0,50 A 10,10 0,0,1 10,40 Z"
  );
}
```

| Command                 | Meaning                                                            |
| ----------------------- | ------------------------------------------------------------------ |
| `M 10,40`               | Move to point (10, 40) — starting near the top-left, but indented  |
| `L 70,40`               | Line to the right up to (70, 40) — the top edge before the notch   |
| `A 10,10 0,0,0 80,30`   | Arc with radius 10 to (80, 30) — curves down into the notch        |
| `L 80,10`               | Vertical line up into notch                                        |
| `A 10,10 0,0,1 90,0`    | Arc to (90, 0) — smooth top edge transition from notch to full top |
| `L 170,0`               | Horizontal line to the top-right corner                            |
| `A 10,10 0,0,1 180,10`  | Rounded top-right corner                                           |
| `L 180,190`             | Vertical line down the right side                                  |
| `A 10,10 0,0,1 170,200` | Rounded bottom-right corner                                        |
| `L 10,200`              | Line all the way to bottom-left                                    |
| `A 10,10 0,0,1 0,190`   | Rounded bottom-left corner                                         |
| `L 0,50`                | Vertical line upward to the left notch                             |
| `A 10,10 0,0,1 10,40`   | Arc to close the notch transition                                  |
| `Z`                     | Close the path (connects back to `M 10,40`)                        |

### Sources

1. https://prismic.io/blog/css-hover-effects
