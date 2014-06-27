---
layout: post
category : tutorial
tagline: "how to write a post"
tags : [Jekyll]
---
{% include JB/setup %}

编写基于jekyll的文章，要注意两点

- 在'_posts'目录下，建立的*.md文件的文件名为 year-month-day-title.md
- 文章的一开头，需要声明内容

具体如下
<pre>
    ---
    layout: post
    title: "此标题可以替换默认英文标题"
    tagline: "副标题"
    description: "摘要，显示在首页"
    category: tech
    tags: [tech, web, jekyll]
    ---
    {% raw %}{% include JB/setup %}{% endraw %}
</pre>

这样就能生成正常的blog文章

------------我是分割线---------------

关于配置jekyll，我的blog主要做了以下改动

1. 修改_config.xml 中的 markdown，改为kramdown
2. 修改_config.xml 中的 disqus 的 shotname，自己注册了一个disqus
3. 其他改动主要针对blog样式，这需要参考jekyll的目录结构，以及jekyll的模板Liquid的语法

Liquid的标签分为两种

- {% raw %} {{ }} {% endraw %} 为输出标签，主要用于变量常量的输出和format
- {% raw %} {% %} {% endraw %} 为tag标签，主要用于 if，for等控制

具体内容参见[此链接](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)
