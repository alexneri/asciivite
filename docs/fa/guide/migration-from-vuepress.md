# مهاجرت از VuePress

## پیکربندی

### نوار کناری

نوار کناری دیگر به طور خودکار از frontmatter پر نمی‌شود. شما می‌توانید [frontmatter را خودتان بخوانید](https://github.com/vuejs/vitepress/issues/572#issuecomment-1170116225) تا نوار کناری به طور پویا پر شود. ابزارهای [اضافی برای این منظور](https://github.com/vuejs/vitepress/issues/96) ممکن است در آینده ارائه شود.

## Markdown

### تصاویر

برخلاف VuePress، ویت‌پرس وقتی شما از تصویر استاتیک استفاده می‌کنید، [`base`](./asset-handling#base-url) پیکربندی شما را به طور خودکار مدیریت می‌کند.

بنابراین، اکنون می‌توانید تصاویر را بدون استفاده از تگ `img` نمایش دهید.

```diff
- <img :src="$withBase('/foo.png')" alt="foo">
+ ![foo](/foo.png)
```

::: warning
برای تصاویر پویا، همچنان نیاز به استفاده از `withBase` به طوری که در [راهنمای Base URL](./asset-handling#base-url) نشان داده شده است، دارید.
:::

از عبارت `!<img.*withBase\('(.*)'\).*alt="([^"]*)".*>` برای جستجو و جایگزینی با `![$2]($1)` استفاده کنید تا تمام تصاویر را با سینتکس `![](...)` جایگزین کنید.

---

ادامه دارد...