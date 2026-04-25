# Default styles with css variables:

we can use default style inside css through this way
```css
:root {
  --primary-color: #9fef00;
  --bg-color: #1c1c1c;
  --border: 1px solid #fefefe;
}

div {
  color: var(--primary-color);
  background-color: var(--bg-color);
  border: var(--border);
}
```
