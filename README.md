### iframe 定义

> 能够将另一个 HTML 页面嵌入到当前页

---

### 引入 iframe 常见问题 1

> 引入时显示`http://xxxx.com` 拒绝了我们的连接请求,因为对方服务器在返回头中增加` X-Frame-Options`HTTP 响应头(案例 1、2)

```
    DENY：浏览器拒绝当前页面加载任何Frame页面
    SAMEORIGIN：frame页面的地址只能为同源域名下的页面
    ALLOW-FROM：origin为允许frame加载的页面地址
```

---

### 常用属性

> 1. height : 以 CSS 像素格式，或像素格式，或百分比格式指定 frame 的高度。默认值为 150。
> 2. src : 被嵌套的页面的 URL 地址。
> 3. width : 以 CSS 像素格式，或以像素格式，或以百分比格式指定的 frame 的宽度。默认值是 300。

---

### js 中查找

> `window.top` 返回顶层窗口，即浏览器窗口。  
> `window.parent` 返回父窗口。  
> 注：如果窗口本身就是顶层窗口，top、parent 属性返回的是对自身的引用。

---

### 引入 iframe 常见问题 2

> 弹窗难处理(案例 4)

---

### 跨窗口通信

> 1. 同源策略  
>    [阮一峰 浏览器同源政策及其规避方法](https://www.ruanyifeng.com/blog/2016/04/same-origin-policy.html)  
>  同源策略下可以使用window.frames与window.parent直接使用被嵌套页面和嵌套页面中的函数进行通信  
> 2. 不同源策略