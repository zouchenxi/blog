# 一、什么是HTML？
***
> **HTML是用来描述网页的一种语言**
- HTML指的是超文本标记语言（**H**yper **T**ext **M**arkup **L**anguage）
- HTML不是一种编程语言，而是一种**标记语言**（markup language）
- 标记语言是一套**标记标签**（markup tag）
- HTML使用**标记标签**来描述网页

重点：HTML是一种标记语言（超文本标记语言）而非编程语言
# 二、HTML、XML、XHTML之间的区别
***

- HTML：超文本标记语言，语法松散、不严格的标记语言
- XML：可扩展标记语言，主要用于存储数据和结构
- XHTML：可扩展超文本标记语言，基于XML，作用与HTML类似，语法更严谨更纯净的HTML版本


 HTML与XHTML最主要的不同：
> - XHTML 元素必须被正确地嵌套
- XHTML 元素必须被关闭
- 标签名必须使用小写字母
- XHTML 文档必须拥有根元素

# 三、HTML语义化
***
#### 1. 什么是语义化
语义化是指根据内容的结构化（内容语义化），选择合适的标签（标签语义化），便于开发者阅读和写出更规范的代码的同时，让浏览器的爬虫和机器更好的解析。

#### 2. 为什么要语义化？
- **有利于SEO**
和搜索引擎建立良好的沟通，有助于爬虫抓取更多的有效信息，爬虫是依赖于标签来确定上下文和各个关键字的权重

- **清晰的页面结构**
语义化的HTML在没有CSS的情况下也能呈现较好的内容结构和代码结构，增强页面的可读性

- **便于团队开发和维护**
在团队中大家遵循同一个标准，使用规范的代码，方便开发和维护，提高开发效率

- **方便其他设备的解析**

# 四、怎样理解内容与样式分离的原则
***
- **HTML——结构**
写HTML的时候先不管样式，重点放在HTML的结构和语义化上，让HTML能体现页面结构和内容
- **CSS——表现**
写完HTML的结构和内容后，再进行CSS样式的编写，减少HTML与CSS契合度（即内容与样式分离）
- **JavaScrip——行为**
写JS的时候，尽量不要用JS去直接操作样式，而是通过给元素添加删除`class`来控制样式变化（即行为分离）

**样式与结构分离的优点：**
> - 浏览器加载网页页面速度变快。分离原则下，页面样式的代码写在了CSS当中，页面体积容量变得更小
- 修改网页样式时，更有效率、更省时间。根据html标签内ID或class的标记，到CSS里找到相应的ID或class，可以快速替换指定位置的样式，不会破坏页面架构和其他部分的样式
- 可以确保网页都能平稳退化。具备CSS支持的浏览器固然可以把网页呈现的美轮美奂，不支持或禁用了CSS功能的浏览器同样可以把网页的内容按照正确的内容结构显示出来

# 五、有哪些常见的meta标签
***
#### 1. meta标签定义和用法
- <meta>元素可提供有关页面的元信息（meta-information），比如针对搜索引擎和更新频度的描述和关键词
- <meta>标签位于文档的头部，不包含任何内容；<meta>标签的属性定义了与文档相关联的名称/值对

#### 2. 常见meta标签用法
```
<meta charset="utf-8">
编码方式
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
双核浏览器
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">
用于移动端的展示合理
<meta name="keywords" content="前端 饥人谷">
网页关键字，利于搜索
<meta name="description" content="最有爱的前端学习社区">
搜索引擎优化
<meta name="keywords" content=""> 
向搜索引擎说明你的网页的关键词  
<meta name="description" content=""> 
告诉搜索引擎你的站点的主要内容  
<meta name="author" content="你的姓名"> 
告诉搜索引擎你的站点的制作的作者  
<meta http-equiv="Content-Type" content="text/html";charset=utf-8"> 
指定字符集  
<meta http-equiv="refresh" content="n;url="> 
定时让网页在指定的时间n内跳转  
<meta http-equiv="pragma" content="no-cache"> 
禁用缓存  
<meta http-equiv="set-cookie" content="Mon,12 May 2001 00:20:00 GMT"> 
cookie设定，如果网页过期，存盘的cookie将被删除。需要注意的也是必须使用GMT时间格式
```
# 六、文档声明的作用?严格模式和混杂模式指什么?<!doctype html> 的作用?
***
#### 1. Doctype作用是什么？
- <!DOCTYPE>声明叫做文件类型定义（DTD）,声明的作用是为了告诉浏览器该文件的类型。让浏览器解析器知道应该用哪个规范来解析文档。
- <!DOCTYPE>声明必须在HTML文档的第一行，这并不是一个HTML标签。

#### 2. 严格模式与混杂模式如何区分？它们有何意义？
**严格模式：**又称标准模式，是指浏览器按照W3C标准解析代码
**混杂模式：**又称怪异模式或兼容模式，是指浏览器用自己的方式解析代码
**如何区分：**浏览器解析时到底使用严格模式还是混杂模式，与网页中的DTD直接相关
> - 如果文档包含严格的 DOCTYPE ，那么它一般以严格模式呈现。**（严格 DTD ——严格模式） **
- 包含过渡 DTD 和 URI 的 DOCTYPE ，也以严格模式呈现，但有过渡 DTD 而没有 URI （统一资源标识符，就是声明最后的地址）会导致页面以混杂模式呈现。**（有 URI 的过渡 DTD ——严格模式；没有 URI 的过渡 DTD ——混杂模式） **
- DOCTYPE 不存在或形式不正确会导致文档以混杂模式呈现。**（DTD不存在或者格式不正确——混杂模式）**
- HTML5 没有 DTD ，因此也就没有严格模式与混杂模式的区别，HTML5 有相对宽松的语法，实现时，已经尽可能大的实现了向后兼容。**（ HTML5 没有严格和混杂之分）**

**意义：严格模式与混杂模式存在的意义与其来源密切相关，如果说只存在严格模式，那么许多旧网站必然受到影响，如果只存在混杂模式，那么会回到当时浏览器大战时的混乱，每个浏览器都有自己的解析模式。**

# 七、浏览器乱码的原因是什么？
***
#### 1. 通用编码方式
- **ASCII**，全称美国标准信息交换代码（American Standard Code for Information Interchange）的缩写, 针对英语设计
- **UTF-8**（8-bit Unicode Transformation Format）是一种针对Unicode的可变长度字符编码，又称万国码。可用于显示中文简体繁体及其它语言（如英文，日文，韩文）
- **GBK**，中国制定的一套汉字编码规则，用2个字节来表示一个汉字，总共可以覆盖2万多个文字
- **ISOLatin-1**，由于ASCII字符集不包括德、法语中的特殊拉丁字符，因此欧洲人发明了ISO 8859-1Latin 1，简称为ISOLatin-1。它对ASCII做了个扩充，涵盖拉丁字母表中特殊语言字符

#### 2. 浏览器乱码的原因
> **乱码产生的根本原因是所保存的编码格式和浏览器解析时的解码格式不匹配导致的**

注：纯粹的英文即时编码方式和解码方式不一致也不会出现乱码问题，那是因为**UTF-8**、**GBK**对英文都是采用1个字节的编码方式，并且使用了相同的码子

#### 3. 如何解决浏览器乱码
- 首先，在文件保存的时候要清楚是用哪种编码方式保存的。
- 如果你的文件是保存为UTF-8格式，那么一定要在html 的 `<head>`里添加`<meta charset="utf-8">`（这句话的意思是告诉浏览器在打开这个页面的时候不要去猜了，直接用utf-8去解码）
-  同理，如果你的文件保存为gbk格式，一定在文件里添加`<meta charset="gbk">`即可

# 八、常见的浏览器有哪些，什么内核

***
浏览器 | 内核 
:---: | :---: 
![](http://upload-images.jianshu.io/upload_images/6125053-b120d29936effade.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240) IE| Trident 
![](http://upload-images.jianshu.io/upload_images/6125053-93923a24b425e5f1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240) Firefox| Gecko  
![](http://upload-images.jianshu.io/upload_images/6125053-ee167722db2b68b5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240) Chrome| Webkit  
![](http://upload-images.jianshu.io/upload_images/6125053-fc7006d73644e3c9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240) Safari| Webkit  
![](http://upload-images.jianshu.io/upload_images/6125053-d160e2be47f36f3a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)Opera | Presto  

# 九、HTML常用标签
***
标签名字 | 标签作用 | 备注 
:---: | :---: |:---:
`<h1-h6>`| 标题标签 | `<h1>标题</h1>`
`<p>`| 段落标签，文本内容 | `<p>段落</p>`
`<a>`| 定义一个超链接 | `<a href="http://www.baidu.com">百度</a>`
`<img>`| 定义图像| `![](tupian.jpg)`
`<div>`| 定义文档中的分区| `<div>文档中分区</div>`
`<button>`|定义按钮 |  `<button>点我</button`
`<iframe>`| 用于嵌入一个页面| `<iframe src="https://jirengu.com/" name="myPage"></iframe>`
`<ol>` `<li>`|定义有序列表 |
`<ul>` `<li>`|定义无序列表 | 
`<dl>` `<dt>` `<dd>`|自定义列表 |
`<table>` `<tr>` `<th>`|定义表格 |