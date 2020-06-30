### 关于 Markdown

Markdown 是用来编写结构化文档的一种纯文本格式，它使我们在双手不离开键盘的情况下，可以对文本进行一定程度的格式排版。你可以在 [这篇文章](https://sspai.com/post/36610) 中快速入门 Markdown。

由于目前还没有一个权威机构对 Markdown 的语法进行规范，各应用厂商制作时遵循的 Markdown 语法也是不尽相同的。其中比较受到认可的是 [GFM 标准](https://github.github.com/gfm/)，它是由著名代码托管网站 [GitHub](https://github.com/) 所制定的。Typora 主要使用的也是 GFM 标准。同时，你还可以在 `文件 - 偏好设置 - Markdown 语法偏好 - 严格模式` 中将标准设置为「更严格地遵循 GFM 标准」。具体内容你可以在官方的 [这篇文档](http://support.typora.io/Strict-Mode/) 中查看。

![img](https://cdn.sspai.com/2019/05/24/a35f8fd5e9d968edfe5a0b02b54d0881.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1)

#### 智能标点

我认为「智能标点」是比较有趣的一点。它可以自动帮你将不是很美观的直引号 `"` `'` 转化为更美观的弯引号 `“` `‘` `’` `”`。具体内容你可以在官方的 [这篇文档](http://support.typora.io/SmartyPants/) 中查看。关于直弯引号在 macOS 上如何输入你也可以看 [这篇文章](https://sspai.com/post/38342)。

#### 代码支持

```javascript
class Utils {
  animate(element: Element, attr: string, change: { from: number, to: number, duration?: number }, onEnd?: () => void) {
    if (change.from = = change.to) return;

    if (!change.duration)
      element[attr] = change.to;

    const easing = (t, b, c, d) => c * ((t = t / d - 1) * t * t + 1) + b,
      { from, to } = change,
      during = Math.ceil((change.duration || 300) / 17) || 1;

    let start = 0,
      instance = null;

    step();

    function step() {
      const value = Math.ceil(easing(start, from, to - from, during));

      start++;
      if (start <= during) {
        element[attr] = value;
        instance = requestAnimationFrame(step);
      }
      else {
        if (onEnd) onEnd();
        cancelAnimationFrame(instance);
      }
    }
  }
}
```

