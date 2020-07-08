# Theme Showcase 

## Heading (h2)

### h3

#### h4

##### h5

###### h6

### Heading link

## Image (click to zoom in/out)

```markdown
<!-- new line -->
![space](https://.../nh-pluto-moonlight.jpg)
<!-- new line -->
```

![space](https://www.nasa.gov/sites/default/files/styles/full_width_feature/public/thumbnails/image/nh-pluto-moonlight.jpg)

### Inline image

Not bad.![yes](https://res.smzdm.com/images/emotions/138.png)

### With link

- Travis CI build status: [![build-img](https://img.shields.io/travis/ikeq/hexo-theme-inside.svg?longCache=true&style=flat-square)](https://github.com/ikeq/hexo-theme-inside)
- Lastest release: [![release-img](https://img.shields.io/github/release/ikeq/hexo-theme-inside.svg?longCache=true&style=flat-square)](https://github.com/ikeq/hexo-theme-inside/releases)
- License: [![license-img](https://img.shields.io/github/license/ikeq/hexo-theme-inside.svg?longCache=true&style=flat-square)](https://blog.oniuo.com/LICENSE)

## hr

Below is a **hr**, I guess.

------

Above is a **hr**, I guess.

## List

### Unordered list

- list item
- list item
   - list item
   - list item
      - list item
      - list item
- list item

### Ordered list

1. list item
2. list item
   1. list item
   2. list item
      1. list item
      2. list item
3. list item

### ChecklistA

- [ ] Get up at 7:00 AM
- [ ] Eat breakfast
- [ ] Go to bet before 11:00 PM

## Table

| Hear no evil | Speak no evil | See no evil |
| ------------ | ------------- | ----------- |
| 🙉            | 🙊             | 🙈           |

### Text align

| Hear no evil | Speak no evil | See no evil |
| ------------ | :-----------: | ----------: |
| 🙉            |       🙊       |           🙈 |

### Headless

```
&nbsp; | &nbsp; | &nbsp;
:-----:|:------:|:-:
A      | B      | 🙈
```

|      |      |      |
| ---- | ---- | ---- |
| A    | B    | 🙈    |

### Long table

| Sun With Face | Grinning Face | Smiling Face | Grinning Face With Big Eyes | Smiling Face With Smiling Eyes | Full Moon Face | Grinning Face With Smiling Eyes | Face With Monocle | Cowboy Hat Face | Thinking Face | Face Vomiting |
| ------------- | ------------- | ------------ | --------------------------- | ------------------------------ | -------------- | ------------------------------- | ----------------- | --------------- | ------------- | ------------- |
| 🌞             | 😀             | ☺️            | 😃                           | 😊                              | 🌝              | 😄                               | 🧐                 | 🤠               | 🤔             | 🤮             |

## Blockquote

(https://hexo.io/docs/tag-plugins#Block-Quote)

> Every interaction is both precious and an opportunity to delight.
>
> **Seth Godin**[Welcome to Island Marketing](http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html)

> NEW: DevDocs now comes with syntax highlighting. [http://devdocs.io](http://devdocs.io/)
>
> **@DevDocs**[twitter.com/devdocs/status/356095192085962752](https://twitter.com/devdocs/status/356095192085962752)

## Code Block

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

### With caption

(https://hexo.io/docs/tag-plugins#Code-Block)

```
_.compactUnderscore.js_.compact([0, 1, false, 2, '', 3]);
// [1, 2, 3]
```

## Gist

(https://hexo.io/docs/tag-plugins#Gist)

## JSFiddle

(https://hexo.io/docs/tag-plugins#jsFiddle)



## script

```javascript
stars: <span id="stargazers_count"></span>

<script>
fetch('https://api.github.com/repos/ikeq/hexo-theme-inside')
  .then(res => res.json())
  .then(json => {
    document.getElementById('stargazers_count').innerHTML = json.stargazers_count || json.message;
  });
</script>
```

stars: 362

For the lastest ES grammar and code minification.
Run the following command in the root directory of Hexo (not `themes/inside`):

```sh
npm install babel-core babel-preset-env html-minifier terser --save
```

## Canvas

Syntax：

```mathematica
{% canvas [width] [height] %}
ctx.fillStyle = 'red';
ctx.fillRect(0, 0, w, h);
{% endcanvas %}
```

width is default to `300`, height is default to `150`，also the following constants are available in the scope:

| constant |                          |
| -------- | ------------------------ |
| ctx      | CanvasRenderingContext2D |
| w        | Canvas width             |
| h        | Canvas height            |

For example:

```mathematica
{% canvas 100 100 %}
const r = w / 2;
ctx.fillStyle = 'antiquewhite';
ctx.arc(r, r, r, 0, Math.PI * 2);
ctx.fill();
{% endcanvas %}
```



## MathJax (SSR)

When $a^2+b^2=c^2$, there are two solutions to and they are



## Code Color

```python
init i=1
 if i=0{
   then i++
 }
```



