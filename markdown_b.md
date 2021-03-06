# 代码与代码块

## 行内代码

行内代码, 在一行文字中间写了代码, 在代码的前后, 使用一个反引号包起来, (键盘左处角, esc键下面的那个键). 如, `echo 'hello world'`, 这是很多语言的第一个入门教程.

## 代码块

代码块, 代码块的前后, 用三个反引号包起来, 在前面的三个反引号之后, 可以跟上语言说明是哪种编程语言, 比如说php, 如

```php
//curl请求
$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_SAFE_UPLOAD, false);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);
curl_exec($ch);
curl_close($ch);
echo $res;
exit;
```


# 链接

链接的语法是, 前面一对中括号,里面写链接的标题文字, 后面加一个小括号, 里面写上链接的url地址. 目前暂不支持新窗口打开链接.

## 内嵌式链接

内嵌式链接, 指的是, 链接直接写在链接文字的后面, 需要一次, 写一次.

- 外部链接 [百度](http://www.baidu.com)
- 内部链接 [Markdown 常用标记用法(基础)](markdown_a.md)
- 锚点链接 [Markdown 常用标记用法(基础)之段落](markdown_a.md#段落)

## 引用式链接

引用式链接, 指的是, 写链接标记时, 只写中括号和链接文字, 但链接地址不写, 链接地址写在文档的末尾. 链接文字之后, 建议再加一个中括号, 里面定义一个链接引用地址的别名, 方便在末尾加链接地址时, 用于标明这个地址是哪一处链接的.

在多次用到同一个链接时, 这种方法, 只需写一次链接地址, 可供全文各处进行引用, 修改链接地址时, 只需修改一次即可.

文末的引用链接地址写法, 中括号, 里面对应前文写的链接标题文字, 加上':', 后面接上链接地址.

- 外部链接 [百度][baidu]
- 内部链接 [Markdown 常用标记用法(基础)][markdown_a.md]
- 锚点链接 [Markdown 常用标记用法(基础)之段落][markdown_a.md#段落]

[baidu]:http://www.baidu.com
[markdown_a.md]:markdown_a.md
[markdown_a.md#段落]:markdown_a.md#段落

# 图片

图片标记与链接标记, 几乎一样, 区别就是, 在最前面加一个感叹号'!', 后面也是接一对中括号, 里面写图片alt内容, 再后面也是一对小括号, 里面写上url地址, 然后可以空一格, 再写上 图片的标题, titile 内容. 注意, title内容可不写, 如果写的话, 需要加上双引号

图片的内嵌式链接与引用式链接, 与链接的用法一致, 不再赘述.

- 外部图片 ![百度logo](https://www.baidu.com/img/bd_logo1.png "百度logo")
- 内部图片 ![风景图片](images/fj5.jpg "风景")

# 链接&图片

将图片做为一个链接的内容, 通过点击图片进入到其他链接

[![风景](images/fj8.jpg "图片链接, 点击图片链接到其他页面")](markdown_a.md)


# 列表

## 无序列表

无序列表, 在列表的每一项前, 加一个'-', 加上空格, 就是一个列表项. 如果要多级列表, 下一级列表要在上一级列表的基础上, 加几个空格表示缩进. 空格数有说两个空格的, 也有说四个空格保险的. 经过测试, 有三个空格即可实现. 如:

- 一级无序列表1
   - 二级无序列表1
   - 二级无二序列表2
      - 三级无序列表1
      - 三级无序列表2
- 一级无序列表2
- 一级无序列表3

## 有序列表

有序列表, 与无序列表一样, 只是把'-' 换成对应的数字序号如,'1.','2.', 加上空格, 就是一个列表项. 多级列表, 也是缩进三个空格即可. 如:

1. 一级有序列表1
   1. 二级有序列表1
   2. 二级有序列表2
      1. 三级有序列表1
      2. 三级有序列表2
2. 一级有序列表2
3. 一级有序列表3

# 清单 TO DO LIST

清单,  类似于无序列表, 在选项前加一个小横杠'-', 后面加一对中括号, 加上空格, 后面写上清单选项.

未完成, 中括号中写个空格, 如果完成了, 中括号里写个'x'.

- [x] 跑步
- [x] 自行车
- [ ] 游泳
- [x] 羽毛球
- [ ] 真人CS
- [ ] 篮球

# 表格

表格标记, 主要是以'|', 竖线来起作用. 一个竖线, 后面加内容, 再一个竖线加内容, 这就相当于是一行表格. 

表格可以说由三部分组成, 表头, 对齐标记, 表格行. 表头与表格行写法一样, 只是表头会加粗显示.

对齐标记是紧贴表头的一行, 也是由竖线分隔, 中间加横线或空格都可以. 主要是起到对齐的作用. 左对齐, 则左边起始加':', 右对齐则右边末尾加':', 居中对齐则, 首尾都加':'. 如没加冒号, 默认为左对齐.

|这  |是  |表格  |
|:----|:----:|------:|
|一行一列一行一列一行一列|一行二列|一行三列|
|二行一列|二行二列二行二列二行二列|二行三列|
|三行一列|三行二列|三行三列三行三列三行三列|
