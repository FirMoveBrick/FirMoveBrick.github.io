
入学以来，搭建个人博客是我如果以来想实现的愿望之一，原因是看着那些想当程序员的师兄师姐们都有属于自己的个人博客。

我曾使用过WordPrass搭建个人博客

但最后权衡利弊，选择Github pages + Hexo 搭建个人博客。

### 如何使用Github pages + Hexo？
如何使用Github pages + Hexo搭建个人博客，在这里小编是阅读朋友写的个人博客[使用 Github pages + Hexo 建立个人博客网站](https://github.com/Longgererer/Longgererer.github.io/blob/master/README.md)，十分有帮助
### Hexo模板挑选
可以在上面寻找自己喜欢的模板，该网站是官网主题站[Hexo](https://hexo.io)

小编在这里用的是[liuyib](https://github.com/liuyib/hexo-theme-stun)的hexo-theme-stun主题模板，感谢作者提供的主题，小编很喜欢。

这个链接是这个模板的使用手册[hexo-theme-stun](https://liuyib.github.io/hexo-theme-stun/zh-CN/)
### 如何编写Hexo的MD文档
在这里，小编推荐直接看[Hexo官方文档](https://hexo.io/zh-cn/docs/)就好，多写多看就会
### 写MarkDown文档建议
1. 将文章的 Markdown 文件用英文命名，然后将 Front-Matter 中的 title 设为文章的中文名字
    > 如果文章路径存在中文，可能出现评论丢失的问题。
2. 小编在本地测试博客的时候，没有什么太大问题，但是部署到github.io就出现问题了
问题是文章图片显示不出来，原因是路径错误。
    > 小编在这里建议大家，使用一款从剪贴板直接上传图像到[sm.ms](https://sm.ms)的VS code插件。可以直接生成MD文件需要的格式和路径（十分好用）
### 如何将部署到GitHub上?
在根目录下输入如下命令:
`hexo clean`
`hexo g`
会生成一个名为public的文件夹
之后将public文件夹中的文件全部复制到该仓库存放的文件夹下
接着使用GitHub DeskTop软件上传到github就行了
### hexo-theme-stun主题
小编在这里要特别介绍hexo-theme-stun主题里面的**Bootstrap** 标注
**语法如下**
```markdown
{% note [type] [no-icon] %}
**header text**

any text
{% endnote %}
```
标签内可以是任意文字，支持 Markdown 和 HTML 语法

**参数：**
 [type]：标注类型 —— default（不履行）、success（成功）、 warning（警告）、danger（危险）
 
 [no-icon]：是否显示 ICON（是否显示图标）
 
 **举例：**
 ```markdown
 <!-- header icon -->
 {% note success %}
 **Success**
 
 This is success note.
 {% endnote %}
 
 <!-- header no-icon -->
 {% note success no-icon %}
 **Success**
 
 This is success note.
 {% endnote %}
 
 <!-- no-header icon -->
 {% note success %}
 This is success note.
 {% endnote %}
 
 <!-- no-header no-icon -->
 {% note success no-icon %}
 This is success note.
 {% endnote %}
 ```
 **部分效果如下**
 ![效果图](https://i.loli.net/2019/09/27/bI4ARfy8BzhWmEs.png)