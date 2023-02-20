![图灵logo](scrapy_img/图灵logo.png)

# 纵横中文网站数据抓取

### 需求说明

* 目的  拿到小说数据  同步到自己网站上
* 网址  https://book.zongheng.com/store/c0/c0/b0/u0/p1/v0/s1/t0/u0/i1/ALL.html
* 目标数据
  * 作者
  * 书名
  * 字数
  * 目录
  * 内容

### 代码实现

#### 	requests测试抓取

* https://book.zongheng.com/store/c0/c0/b0/u0/p1/v0/s1/t0/u0/i1/ALL.html

  * 得到书名 和二级url
  * 作者

* https://book.zongheng.com/book/1256660.html

  * 作者
  * 书名
  * 字数
  * 目录url  三级url

* https://book.zongheng.com/showchapter/1256660.html

  * 目录
  * 内容url

* https://book.zongheng.com/chapter/1256660/70643075.html

  * 内容

    ![图灵logo](scrapy_img/图灵logo.png)

  #### scrapy 工程化实现

* 存储字段

  * 作者
  * 书名
  * 书url
  * 字数
  * 目录
  * 目录url
  * 内容
  * 内容url

  ​

  ​

  ​