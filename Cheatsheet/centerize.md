# Centering element simple:

#### using `transform` property
```html
<div class="parent">
  <div class="child"></div>
</div>
```

```css
.parent {
  position: relative;
}
.child {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

---

#### using `flex` (initial)
```css
.parent {
  display: flex;
  align-items: center;
  justify-content: center;
}
```
