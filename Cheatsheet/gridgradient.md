# Crazy Things You Can Do with CSS Gradients
Next-level css gradients:

you may think we can just make this with gradient for following div:

```html
<div class="test"></div>
```


<img width="100%" height="200" src="data:image/svg+xml;utf8,
<svg xmlns='http://www.w3.org/2000/svg' width='800' height='200'>
<defs>
<linearGradient id='g' x1='0%' y1='0%' x2='0%' y2='100%'>
<stop offset='0%' style='stop-color:black;'/>
<stop offset='100%' style='stop-color:red;'/>
</linearGradient>
</defs>
<rect width='100%' height='100%' fill='url(%23g)' rx='20'/>
</svg>">



```css
.test {
  height: 200px;
  background-image: linear-gradient(black, red);
}
```
