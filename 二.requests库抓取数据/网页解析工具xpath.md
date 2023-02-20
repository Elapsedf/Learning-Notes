## Xpath

**是什么： 一种解析网页的工具**

**为什么：对比正则表达式 更加方便**

**原理:根据网页的结构规律，解析数据**

**安装：**     pip install  lxml

#### 用法：

* 定位标签       
  * 使用xpath表达式
* 获取文本


#### 语法总结

* **常用**

| **表达式**  | **描述**                        |
| -------- | ----------------------------- |
| nodename | 选取当前节点的所有nodename子节点          |
| /        | 从根节点选取    下一级                 |
| //       | 从匹配选择的当前节点选择文档中的节点，而不考虑它们的位置。 |
| .        | 选取当前节点                        |
| ..       | 选取当前节点的父节点                    |
| @        | 选取属性                          |



```python
with  open('网页文本.html','r',encoding='utf-8')  as f:
    text=f.read()

html=etree.HTML(text)  #将text 变成 xpath对象


tags=html.xpath("/html/body") # /一个表示根路径 从根路径开始 下一级
print(tags)  #形式是列表
print(tags[0].text) #  .text  可以直接获取到文本

text=tags[0].xpath("./text()")  # 1  . 代表的是当前标签   2 标签/text() 获取到标签下的数据
print(text)

text=html.xpath("//body/text()")  #// 不考虑路径
print(text)


text=html.xpath("//span[@class='link'][2]/a/text()")  #// 标签后 [] 中 @ 可以根据属性筛选  []中有索引可以选择标签的序号 1 是第一个
print(text)
text=html.xpath("//span[@id='tl']/a/text()")  #有 id  使用id  直接定位
print(text)

text=html.xpath("//span[@id='tl']/a/@href")  # @属性  可以获取属性值
print(text)
```

