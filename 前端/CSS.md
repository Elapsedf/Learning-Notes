# 翁恺

## 1

**HTML表达结构，CSS表达形式！**



```html
1，可以外部加css文件
2，在head加
<head>
    <style>
        p {background-color:gray;}
    </style>
</head>
3，在段落加
<body>
    <p style="background-color:yellow;">(名字：值)
        
    </p>
</body>

```



##  2.1 背景样式

**transparent(透明色，默认色！和白色有区别！)**

##RRGGBB(每一种颜色的值最大为255，即取值为0-255，即一个字节，对应到十进制就是00-FF)

```html
<body style="background-color:grey;">(body的背景, 也可以用RGB定义，或者##RRGGBB， rgb(255,255,0))（纯红+纯绿）
<p style="background-color:rgba(255,255,0,0.5)"> (最后一个为a通道！即透明度，当a=1是不透明)
	    
</p>
    
```

**透明度的使用！**

```html
<body style="background-img:url(hands1440.jpg); background-repeat:no-repeat(repeat-x/y);	
             background-position:center(top/top right右上/100px 100px);
             background-attachment:fixed">	(背景不滚动！)
    <p style="background-color:rgba(255,255,0,0.5)"> (此时透明度可以不盖住底部的背景！)
        
    </p>
</body>
```

## 3.1文本样式

```html
<body>
    <p style="red"> 
        5-13星期六，半夜
    </p>
    <p style="text-indent:-2em,padding=2pm; line-height:2">(首行缩进，em：当前字体的倍数，pt：印刷的磅，缩进可以是负的,padding:悬挂缩进, line-height:行间距)
       
    </p>
    <p style="text-align:center"
</body>
```

