# Jekyll-Search


#### jekyll博客搜索插件

hexo博客搜索插件请前往 [Hexo-Search](https://github.com/androiddevelop/hexo-search)

### 截图

![jekyll-search.jpg](jekyll-search.jpg)

也可以打开[http://codeboy.me](http://codeboy.me)查看效果

### 操作

1. 点击右下角图标进行搜索
2. 双击ctrl键进行搜索或关闭
3. 搜索页面点击右上角关闭按钮关闭搜索试图

### 加入步骤

1. 将search目录放至于博客根目录下，其中search目录结构如下:

		search
		├── cb-footer-add.html
		├── cb-search.json
		├── css
		│   └── cb-search.css
		├── img
		│   ├── cb-close.png
		│   └── cb-search.png
		└── js
		    ├── bootstrap3-typeahead.min.js
		    └── cb-search.js


2. 在 `_include/footer.html` 中的 `</footer>` 前加入 `cb-footer-add.html` 中的内容即可。 


### 注意事项

1.需要事先引入**jquery**与**bootstrap3(js与css文件)**框架，如果没有的话，操作如下:

在`_include/head.html` 中引入以下代码:

```
<link rel="stylesheet" href="//cdn.bootcss.com/bootstrap/3.3.6/css/bootstrap.min.css">
```
在`_include/footer.html` 中引入以下代码:

```
<!-- jQuery -->
<script src="//cdn.bootcss.com/jquery/2.2.2/jquery.min.js"></script>

<!-- Bootstrap Core JavaScript -->
<script src="//cdn.bootcss.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
```
**`bootstrap3-typeahead.min.js` 的引入必须在`jquery.min.js`引入之后，即在`footer.html`中的行数更靠后！**

2.默认联想8个，如果需要更多的话，请检索 `bootstrap3-typeahead.min.js` 中的**items:8**, 将**8**替换成自己需要的数值。

3. 文章标题请不要使用回车等符号，回车等符号会造成json解析错误。

### 更新历史

#### v1.0.2

- 添加错误console输出。

#### v1.0.1

- 增加firefox支持。

#### v1.0.0

 - 支持jekyll中进行文章搜索。

> 有任何问题何以发送邮件到app@codeboy.me进行交流。


