1、回滚到页面顶部

```
const goToTop = () => window.scrollTo(0, 0);
goToTop();

```

![image-20210126103956818](C:\Users\86177\AppData\Roaming\Typora\typora-user-images\image-20210126103956818.png)

2、打印

![image-20210126110320217](C:\Users\86177\AppData\Roaming\Typora\typora-user-images\image-20210126110320217.png)

3、平滑滚到屏幕顶部

```
const scrollToTop = () => {
  const c = document.documentElement.scrollTop || document.body.scrollTop;
  if (c > 0) {
    window.requestAnimationFrame(scrollToTop);
    window.scrollTo(0, c - c / 8);
  }
}
scrollToTop()
```

