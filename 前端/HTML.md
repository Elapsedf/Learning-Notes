# 1

```html
<!DOCTYPE html> （说明html类型为html5）
<html>
<head>
    配置
    样式表
    不是用来显示的
    <title>我的标题</title>
    <meta charset=utf-8>	unicode，（编码形式，gbk国标码，但有的不一定支持）
</head>
<body>
正文，用于显示，
我的第一个HTML页面
</body>
</html>
```



txt：保存类型：所有类型，再改为html

# 2

## 2.1段落

浏览器会**忽略空格，换行**，会当成一个空格

```html
<body>
    <hgroup>
    <h1> 第一章</h1>		第一级标题（最多可以做6级）（单独成行，可以不用加<br>）
        <h2> 第二章</h2>
    </hgroup>
<p>	表示段落的开始
    表明这是段落，paragraph，而若要空两格，则要在样式表内修改！
</p>
<br>插入分行符，用于段内分行，浏览器默认不空行，而p会空行，但是可在样式表内修改！
没有</br>,因为br自己是一个东西
也有<br /> (可以不加/ ！)
<wbr>decorated</wbr>	(对于英文可以被分开)
</body>
```

**表达==是什么==，而不是表达长成什么样**

**html写结构，css写样式**

**css（样式表）**

标记有内在逻辑意义

## 2.2字体样式

```html
<b>永远</b> (加粗，对中文支持不是很好)
<i>结束</i> (斜体，可以与加粗叠加)
<tt>evening</tt> (印刷字体)
<small>big</small>	(变小)
<del>聊条一</del><ins>藤条一</ins>
不是单纯加删除线，而是表明一种结构，删除某种东西，加入某种东西，怎么实现是浏览器的事
<s></s>表示不被提倡使用，过时的！
a<sup>2</sup>+b<sub>0</sub>	(sup上标，sub下标)
<mark>南方庄园</mark>	(高亮)
```

**html表示的是结构！！！**

## 2.3短语格式

```html
<body>
    <em>em强调</em>
    <strong>strong（着重强调）</strong>
    <dfn>定义definition</dfn>
    <code>code代码（不是大段代码）</code>
    <samp>samp例子代码</samp>	(与code区别，可能视觉效果不同，由css决定)
    <kbd>kbd用户输入</kbd>
    <var>variable变量</var>
    <cite>cite引用</cite>
</body>
```

# 3

## 3.1特殊格式

```html
<body>
    <pre>(不格式化！按原本显示)
    int main(){
    	printf()
    }
    </pre>
    
    <address>	(表示地址)
        <blockquote>	(大缩进且可嵌套)
            Rm 401 CKP West Ring<br>
            <q>	(小引用)
                玉泉 Camps <br>
            </q>     
            浙江 U
        </blockquote>
    </address>
</body>
```

## 3.2属性

```html
<hr width=50% align=left size=10> (分割线，没有对应的结束 align(左对齐) size粗细)
关于属性，html5可以不加" "
关于上面的属性，提倡用css做
<abbr title="中华人名共和国">PRC</abbr>(表示PRC是缩写)
<p title="第一节" >
    所有的标记都可以加title，帮助显示注释！
</p>
<bdo dir=rtl>舞厅被装饰成<bdi>南方庄园的风格</bdi></bdo>		(rtl:从左向右排)
(小于号？)
a&lt;2(lt->less than)
&lt;(小于号) &gt;(大于号)
&amp;('&')
&nbsp;(non breakable space)
L&uuml;	(吕音标上有两小点)
L&UUml;()
```

# 4

## 4.1列表

```html
<ul>(unorder list)
    <li>红茶</li>	(list item,有点像latex)
    <li>咖啡</li>
</ul>
<ol start=-1/0>(order list)
    <li>咖啡:
    	<ul>
            <li>不加糖</li>	(可嵌套)
            <li>不加奶</li>
        </ul>
    </li>
</ol>
<dl>(definition list)
    <dt>方糖</dt>
    <dd>方的糖，甜的</dd>
</dl>
```

## 4.2 图片

**图片是一个字符！**

所以与其他字符是连在一起！

```html
<img src="mama.jpg" alt="mama" width= "50%" height="200" />
(/可不加， src为source, alt为alternative，即图片加载过慢，可以先显示文字)
<iframe src="http://news.163.com">
    可以将别的网站实时加载过来！
</iframe>                                                   
```

**图片与文字的关系：cSS解决！**

## 4.3 链接

```html
<a href="http://news.163.com" target=_blank>网易新闻</a>	(打开新窗口，还有不同的target)
<a href="you.html">你的网页</a>
<a href="#here">网易新闻</a> (可以前往某一个页面的段落)
<a href="you.html#here" >网易新闻</a>(前往you.html #here处)
<body>
    <p id="here">
        here
    <img src="mama.jpg" alt="mama" width= "50%" height="200" usemap="#map"/>	(映射！！)
        <map name="map">
        	<area shape ="rect" coords="0,0,50,50" href="http://news.163.com" alt="news" />
            <area shape="circle" coords="75.75,25" href="http://www.163.com" alt="home" />
        </map>
    </p>
</body>
```

(href：超文本引用，如果没有**协议**开头，则会在本地查找)

## 4.4表格

```html
<p>
    <table border=1>(画格子线)
        <caption>表格</caption>（表格的名字）
        <thead>（真正意义的表头，由thead提示）
            
        <tr>
            <th>OS</th>(table head,表头)
            <th>Chinese</th>
            <th>French</th>
        </tr>
        </thead>
        <tbody>(表格body)
        <tr>	(table row,里面的内容属于一行)
            <td>ios 5</td>
            <td>yes</td>
            <td>yes</td>
        </tr>
        <tr>
            <td colspan="3">windows</td>(该单元格占据三个格子，沿水平方向延展)
            <td></td>
            <td></td>
        </tr>
</tbody>
<tfoot>
    脚注!
</tfoot>
</table>
</p>
```

一个表格也是一个字符！

