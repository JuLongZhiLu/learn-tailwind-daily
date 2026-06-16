### 第 1 天：初识“实用类”（Utility Classes）—— 文本与背景

**💡 核心概念**
Tailwind 的核心思想是**“Utility-First”（实用优先）**。你不必再去写单独的 CSS 文件，而是直接在 JSX 的 `className` 中组合使用预设好的类名（Class）来完成样式。

**🛠 今天学习的类名**
在 Tailwind 中，颜色通常带有一个 **50 到 950 的色阶**（数值越大，颜色越深）。

1. **文本颜色**: `text-{颜色}-{色阶}` （例如：`text-blue-500`, `text-red-600`）
2. **背景颜色**: `bg-{颜色}-{色阶}` （例如：`bg-gray-100`, `bg-black`）
3. **字体大小**: `text-{大小}` （例如：`text-sm` 小号, `text-base` 正常, `text-2xl` 大号, `text-5xl` 特大）
4. **字体粗细**: `font-{粗细}` （例如：`font-normal` 正常, `font-bold` 加粗）

**💻 动手实践**


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



**🎯 今日小挑战（动手试试看）**
在上面的代码基础上，尝试完成以下修改：
1. 把整个背景的颜色改成浅黄色（提示：试试 `bg-yellow-50` 或 `bg-amber-100`）。
2. 把 `<h1>` 标题的字号变得更大（提示：试试 `text-5xl`），并改成绿色（提示：`text-green-500`）。

等你完成了今天的练习，或者随意玩够了这些颜色和大小，随时回复我，我们就可以开启**“第 2 天”**的内容（比如：边距与内边距 Padding & Margin）！
