# Crazy Things You Can Do with CSS Gradients
Next-level css gradients:

you may think we can just make this with gradient:

```html
...

css
...


Markdown همه‌ی بلاک‌ها رو **عمودی (زیر هم)** رندر می‌کنه و هیچ مفهومی از layout نداره.

---

## ✅ راه‌حل عملی تو GitHub: استفاده از HTML داخل Markdown

GitHub اجازه می‌ده HTML خام داخل `README.md` بنویسی.

### مثال: HTML و CSS کنار هم

```html
<table>
  <tr>
    <td>
```html
<div class="box">Hello</div>

</td>
<td>

css
.box {
  color: red;
}

</td>
  </tr>
</table>


✅ نتیجه: دو تا code block **کنار هم** نمایش داده می‌شن.

---

## ✅ روش تمیزتر با `<div>` و flex (محدود ولی کار می‌کنه)

```html
<div style="display:flex; gap:16px;">

<div>
```html
<button>Click</button>

</div>

<div>

css
button {
  background: black;
  color: white;
}

</div>

</div>


📌 GitHub:
- `style` inline رو قبول می‌کنه
- فایل جداگانه CSS قبول نمی‌کنه
- بعضی propertyها محدودن ولی `flex` کار می‌کنه

---

## ⚠️ محدودیت‌های GitHub Markdown
✅ HTML inline → مجاز  
❌ `<script>` → بلاک می‌شه  
❌ CSS خارجی → بلاک  
⚠️ بعضی styleها ignore می‌شن

---

## ✅ راه ساده‌تر (بدون HTML)
اگر کنار هم بودن **خیلی مهم نیست**:
- یکی رو عنوان بده
- یا از table استفاده کن (حتی بدون code block)

```md
| HTML | CSS |
|------|-----|
| `<div></div>` | `.box {}` |
