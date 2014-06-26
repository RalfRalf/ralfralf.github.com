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
~~~~~~
    ---
    layout: post
    title: "此标题可以替换默认英文标题"
    tagline: "副标题"
    description: "摘要，显示在首页"
    category: tech
    tags: [tech, web, jekyll]
    ---
    {% include JB/setup %}
~~~~~~

这样就能生成正常的blog文章

