# چطوری داخل المنت افکت و الگو های گراذینت دار درستت کنیم ؟

باید سه تا چیز بهتون یاد بدم

### 1) ساخت box-shadow داخلی
میتونید همونطور که سایه به بیرون میدید
از داخل هم سایه تعریف کنید با این ساختار:
```css
box-shadow: inset  /*رنگ*/  /*شروع نشر*/  /*شعاع بلور*/  /*جایگاه عمودی*/  /*جایگاه افقی*/;
```
مثال:
```css
box-shadow: inset 10px 0 10px 0 black;
```
همه ی value ها مثل shadow هستن فقط اولش کلمه inset قرار میگیره

<br />
<br />
<br />

---

<br />
<br />
<br />

### 2) ساخت radial-gradient (گرادینت گرد)
```css
background-image: radial-gradient(/*اندازه*/  /*شگل*/  at  /*رنگ*/  , /*رنگ*/  , /*جایگاه*/); 
```
#### به جای هر value چی میتونیم بنویسیم ؟
- شکل:
    - عبارت های `circle` یا `ellipse` به معنای دایره و بیضی
- اندازه:
    - مثلا برای `40px` ،`circle` یا `%100`. نشون دهنده اندازه گرادینت گردی که ساخته میشه
    - مثلا برای `50px 30px` ،`ellipse` یا `%50 %10`. نشون دهنده طول و عرض بیضی
- جایگاه: 
    - استفاده از کلمات کلیدی مثل `center top` یا `center` یا `left bottom`
    - و یا تعریف جایگاه دقیق افقی و عمودی مثل `%10 %20` که نشون دهنده فاصله از چپ و بالای المنت هست
- رنگ: 
    - مثل بقیه رنگ ها



مثال:
```css
background-image: radial-gradient(circle 70% at center, black, transparent);
```
تو این مثال یه دایره گرادینتی به اندازه `%70` المنت و در مرکز المنت ساختیم که از مرکز رنگ مشکی داره و به سمت بی شفاف شدن میره

<br />
<br />
<br />

---

<br />
<br />
<br />

### 3) نحوه اعمال چند مقدار به یک المنت
مبشه تو این دو `property` همزمان به یک المنت چند استایل اعمال کرد

مثال برای `shadow`:
```css
box-shadow:
    10px 10px 0 red,
    -10px -10px 0 blue,
    inset 0 0 10px black;
```
تو این مثال ما به یک المنت سه تا `shadow` دادیم که دو تاش خارجی و یکیش داخلی بود
>[!NOTE]
>نکته: بین `value` ها حتما باید از ` , ` (کاما | comma) استفاده کرد و در پایان از ` ; ` (سمیکالن | semicolon) استفاده کرد برای تایین اینکه اون `property` تموم شده.<br>
>مهم نیست که همه رو تو یک خط بنویسیم یا اینکه مثل مثال بالا. این سبک نوشتن فقظ برای خوانایی بهتره.

<br />
<br />

مثال برای `background`:
```css
bakground:
    radial-gradient(circle at left top, black, transparent 60%),
    radial-gradient(circle at right bottom, white, transparent 30%),
    red;
```
تو این مثال ما به یک المنت سه تا پس زمینه دادیم. دو تا گرادینت گرد و یک رنگ ثابت.
چون به گرادینت ها سایز ندادیم به صورت پیش فرض به اندازه کل المنت هستن و ما با تایین ` % ` برای رنگ دوم (`transparent`) ، اندازه دایره های گرادینت دار رو کنترل کزدیم.
>[!NOTE]
>نکته: ما از ویژگیِ(property) `background` استفاده کردیم و نه `background-image` یا `background-color`.<br>
دلیلش اینه که `background` خالی به ما اجازه میده هر چیزی رو داخلش تعریف کنیم مثل<br>
>`linear-gradient()` , `radial-gradient()` , `#hexcode` , `rgb()` , `colorname` و حتی `url(path)` و ما رو محدود به استفاده از فقط property های `background-image` یا `background-color` نمیکنه.

<br />
<br />
<br />

---

<br />
<br />
<br />

مثال زیر یک نمونه کامل استفاده از این افکت هاست:
```html
<!-- index.html-->
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Glowing Blood Card</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div class="card">
            <p>BLOOD CARD</p>
        </div>
    </body>
</html>
```



```css
/* style.css */
body {
    margin: 0;
    padding: 0;
    font-family: lato;
    background-color: #f5f5f5;
}

.card {
    margin: 300px auto;
    width: 200px;
    height: 100px;
    border-radius: 20px;
    background:
        radial-gradient(circle 80px at 10% 20%, #2e2e3060, transparent),
        radial-gradient(circle 70px at 90% 80%, #f5f5f560, transparent),
        #c51d34;
        /* #c51d34cc; */
    box-shadow:
    10px 5px 20px #232330b2,
    -10px -5px 20px #c51d3480,
    inset 0 0 10px 2px #891a3b;
    position: relative;
    transform: scale(2);
}

.card p {
    color: #f5f5f5;
    margin: 0;
    position: absolute;
    width: 100%;
    text-align: center;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}
```

<center>
    
کپی و بررسی کنید

</center>
