# 第 1 天：初识“实用类”（Utility Classes）—— 文本与背景

## **💡 核心概念**
Tailwind 的核心思想是**“Utility-First”（实用优先）**。你不必再去写单独的 CSS 文件，而是直接在 JSX 的 `className` 中组合使用预设好的类名（Class）来完成样式。

## **🛠 今天学习的类名**
在 Tailwind 中，颜色通常带有一个 **50 到 950 的色阶**（数值越大，颜色越深）。

1. **文本颜色**: `text-{颜色}-{色阶}` （例如：`text-blue-500`, `text-red-600`）
2. **背景颜色**: `bg-{颜色}-{色阶}` （例如：`bg-gray-100`, `bg-black`）
3. **字体大小**: `text-{大小}` （例如：`text-sm` 小号, `text-base` 正常, `text-2xl` 大号, `text-5xl` 特大）
4. **字体粗细**: `font-{粗细}` （例如：`font-normal` 正常, `font-bold` 加粗）

## **💻 动手实践**


[React Playground](https://playcode.io/react?utm_source=chatgpt.com)

请把你 React PlayCode 中的 `App.jsx` 里面的内容替换成下面这段代码，看看右侧预览区的变化：

```jsx
import React from 'react';

export default function App() {
  return (
    <div className="bg-slate-100">
      <h1 className="text-3xl font-bold text-blue-600">
        你好，Tailwind！
      </h1>
      <p className="text-base text-slate-700">
        这是我学习 Tailwind 的第一天，直接写 className 太爽了。
      </p>
    </div>
  );
}
```

<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/3a5649f3-cf76-4864-8f03-099d90e86a51" />



## **🎯 今日小挑战（动手试试看）**
在上面的代码基础上，尝试完成以下修改：
1. 把整个背景的颜色改成浅黄色（提示：试试 `bg-yellow-50` 或 `bg-amber-100`）。
2. 把 `<h1>` 标题的字号变得更大（提示：试试 `text-5xl`），并改成绿色（提示：`text-green-500`）。

等你完成了今天的练习，或者随意玩够了这些颜色和大小，随时回复我，我们就可以开启**“第 2 天”**的内容（比如：边距与内边距 Padding & Margin）！

# 扩展知识
为什么Tailwind的字体大小要表示成text-2xl？2xl是什么意思？

这是 Tailwind 设计上的一个很有意思的选择。

很多刚接触 Tailwind 的人都会疑惑：

```html
text-sm
text-lg
text-xl
text-2xl
text-3xl
```

为什么不用：

```html
font-size-24
font-size-32
```

或者：

```html
text-24px
text-32px
```

呢？

---

## xl 是什么意思？

`xl` 是：

```text
Extra Large
超大
```

的缩写。

例如：

```text
sm = Small
md = Medium
lg = Large
xl = Extra Large
```

所以：

```text
text-sm
↓
小字体

text-lg
↓
大字体

text-xl
↓
超大字体
```

---

## 那 2xl 呢？

Tailwind 继续往上扩展：

```text
xl   = Extra Large

2xl  = 2 × Extra Large

3xl  = 3 × Extra Large

4xl  = 4 × Extra Large

...
9xl
```

虽然不是严格意义上的数学乘法：

```text
2xl ≠ xl × 2
```

而只是：

```text
比 xl 更大
```

的命名方式。

---

## 实际对应大小

默认 Tailwind：

| 类名        | 大小   |
| --------- | ---- |
| text-xs   | 12px |
| text-sm   | 14px |
| text-base | 16px |
| text-lg   | 18px |
| text-xl   | 20px |
| text-2xl  | 24px |
| text-3xl  | 30px |
| text-4xl  | 36px |
| text-5xl  | 48px |
| text-6xl  | 60px |

所以：

```html
<h1 class="text-2xl">
```

实际上：

```css
font-size: 24px;
```

---

## 为什么不用 text-24？

这是 Tailwind 的设计哲学。

Tailwind 作者认为：

你写：

```html
text-2xl
```

实际上是在表达：

```text
这是一个比较大的标题
```

而不是：

```text
我要24px
```

---

例如：

```html
<h1 class="text-4xl">
```

你想表达的是：

```text
一级标题
```

而不是：

```text
36px
```

---

## 这叫 Design Token（设计令牌）

现代 UI 设计都喜欢这样：

```text
Primary Color
Secondary Color

Small
Medium
Large

xs
sm
md
lg
xl
```

而不是：

```text
#1677ff

13px

27px
```

---

例如：

```html
text-xl
```

表示：

```text
大标题
```

---

未来如果设计师觉得：

```text
20px 不够大
```

直接改配置：

```js
text-xl = 22px
```

所有页面自动更新。

---

## React 开发者后来为什么喜欢这种命名？

因为你会越来越少关心：

```text
24px
36px
48px
```

而更关心：

```text
标题
副标题
正文
说明文字
```

所以：

```html
<h1 class="text-4xl font-bold">
```

读起来像：

```text
大标题
```

而不是：

```text
字体36像素
```

这也是 Tailwind 整体设计的思想：

> 不要直接操作具体数值，而是使用一套统一的设计尺度（Design Scale）。

所以：

```html
text-2xl
```

本质上可以理解成：

```text
第二级超大字体
```

而不是：

```text
24px
```

虽然默认情况下它恰好对应 24px。

