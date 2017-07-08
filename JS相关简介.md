## 1. 解析型语言和编译型语言的主要差别是什么？
- **编译型语言**
需通过编译器将源代码编译成机器码，之后才能执行的语言。一般需经过编译、链接这两个步骤。编译是把源代码编译成机器码，链接是把各个模块的机器码和依赖库串连起来生成可执行文件。

- **解释型语言**
解释性语言的程序不需要编译，相比编译型语言省了道工序，解释性语言在运行程序的时候才逐行翻译。
## 2. 有哪几种在网页中应用 JS 的方法？
- **内部JavaScript——在`<script>` 标签内添加脚本**

```
<script>
  document.body.scrollTop = 100;
</script>
```

- **外部JavaScript——通过` <script>` 标签的 src 属性引入脚本**

```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <title>JavaScript</title>
</head>
<body>
  <h1>JavaScript 是最好的编程语言。</h1>
  <script src="https://cdn.bootcss.com/jquery/3.2.1/jquery.js"></script>
  <script src="app.js"></script>
</body>
</html>
```

- **内联JavaScript——直接在HTML标签中插入js代码**
```
<button onclick="alert('清除成功!')">清除缓存</button>
```

## 3. 为什么推荐把 script 标签都放在页面底部？
有助于提高网页加载速度，提升页面性能，确保在脚本执行前页面已经完成了渲染。
> 浏览器渲染HTML文件是从上往下渲染的。即先执行head标签里的内容，再执行body标签里的，一行行渲染下去。无论当前 JavaScript 代码是内嵌还是在外链文件中，页面的下载和渲染都必须停下来等待脚本执行完成。JavaScript 执行过程耗时越久，浏览器等待响应用户输入的时间就越长。所以JS尽量放底部可以有一定的性能优化效果。
## 4. 写注释的主要目的是什么？
能够让阅读者（代码完成若干长时间后的自己、新接手这份代码的同行、协同工作的伙伴、调用你接口的人）清晰地理解每段程序的意图，更好的管理代码，利于维护。
## 5. ECMAScript 是什么？跟 JavaScript 有什么关系？
- ECMAScript 是 JavaScript 语言的规范，它规定了 JavaScript 语言的行为和支持特性，各个浏览器厂商根据这份规范实现自己的 JavaScript 引擎。

- JavaScript是ECMAScript的实现。
