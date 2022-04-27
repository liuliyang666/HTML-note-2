# HTML常用标签

## 一. a标签的用法

### 属性：

* href

* target
 
* download

* rel
  
### 作用：

* 跳转外部页面；

* 跳转内部锚点；

* 跳转到邮箱或电话。
  
### a 的 href 的取值：

1. 网址：选用 `//google.com` 的网址，因为是无协议网址，最高级，会自动选择适用 `https` 还是 `http` 。
   
2. 路径

* `/a/b/c` 以及 `a/b/c`;

* `index.html` 以及 `./index.html`

之前说的路径都是基于文件，当我们使用http之后就不是文件了。当我们开启http服务后，就不是硬盘的根目录，而是你在哪里开启的服务哪里就是你的根目录。

注意：绝对不要双击打开html,一旦双击绝对路径就错了。

3. 伪协议

* javascript ：代码

  ``` <a href="javascript:;"> </a>```

* mailto ：邮箱
  
  ``` <a href="mailto:邮箱"> </a>```

* Tel ：电话
  
  ```<a href="tel:电话号码"> </a>```

### a 的 target 的取值：

1.内置名字

* `_blank` ：在空白页打开，浏览器总在一个新打开、未命名的窗口中载入目标文档
  
* `_top` ：这个目标使得文档载入包含这个超链接的窗口，用 _top 目标将会清除所有被包含的框架并将文档载入整个浏览器窗口。
  
* `parent` ：这个目标使得文档载入父窗口或者包含来超链接引用的框架的框架集。如果这个引用是在窗口或者在顶级框架中，那么它与目标 _self 等效。
  
* `self` ：这个目标的值对所有没有指定目标的`<a>` 标签是 默认目标，它使得目标文档载入并显示在相同的框架或者窗口中作为源文档。（注意：谷歌不允许用iframe指向 `_self` ）

2.程序员命名

* windows 的 name

* iframe 的 name

## 二. table 标签的用法

### table 相关的标签

* table：里面只能有我们用的thead、tbody、tfoot这三个标签
  
* thead：表格的头部
  
* tbody：表格的身体
  
* tfoot：表格的尾部
  
* tr：`table row` 表示 table 里面的一行
  
* td：`table data` 表示表格里的数据
  
* th：表示表格的表头

```
<body>
    <table>
        <thead>
            <tr>
                <th>英语</th>
                <th>翻译</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>hyper</td>
                <td>超级</td>
            </tr>
            <tr>
                <td>target</td>
                <td>目标</td>
            </tr>
            <tr>
                <td>reference</td>
                <td>引用</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td>空</td>
                <td>空</td>
            </tr>
        </tfoot>
    </table>
</body>
```

### 相关的样式

* table-layout：有默认值 `auto`自动表格布局算法，和 `fixed` 通过表格宽度来设置的。

* border-collapse：`border-collapse` 默认值为 `separate`，即每个td单元格都有独⽴的边框；collapse表⽰相邻单元格共⽤⼀个边框，此时 border-spacing 将不起作⽤，设置为 `collapse`单元格间距将消失。

* border-spacing：控制单元格之间的距离，一般改为0.
  
  ```
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        table{
            width: 600px;
            table-layout: auto;
            border-spacing: 0px;
            border-collapse: collapse;
        }
        td,
        th{
            border: 1px solid blue;
        }
    </style>
  </head>

  ```

## img标签

```<img scr="..." alt="...">```

### 作用：

* 发出 get 请求，展示一张照片。

### 属性：

* alt / height / width /src

`alt` :图片加载失败时，用文字来提示用户。

`height` / `width`：不用写px，写高度宽度自定义；写宽度，高度自定义。（不能让图片变形，只写任意一个。）

### 事件

* onload / onerror 

监听图片是否加载成功。

### 响应式

* max-width: 100%

适应手机上的显示

### 可替换元素

* 考试可能会问，被问概率30%

## 其他感想

* 在学习HTML时，还是得多记，多看，多操作；不懂就问。