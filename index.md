---
layout: page
title: Ralf's Blog
tagline: Articles about Java and distributed computing
---
{% include JB/setup %}

<div class="tabbable">
     
     <ul class="nav nav-tabs" id="example-tabs">
       <li class="active"><a href="#write_post"  data-toggle="tab">Write_post</a></li>
       <li><a href="#highlight_code"  data-toggle="tab">Highlight Code</a></li>
       <li><a href="#markdown_text" data-toggle="tab">Markdown Text</a></li>
     </ul>
     
     <div class="tab-content">
          <div class="tab-pane active" id ="write_post">
<pre class="prettyprint linenums">
    ---
    layout: post
    title: "此标题可以替换默认英文标题"
    tagline: "副标题"
    description: "摘要，显示在首页"
    category: tech
    tags: [tech, web, jekyll]
    ---
    {{ '{% include JB/setup %}' }}
</pre>

               <p>see these articles for the details:</p>
               <ul>
                    <li><a href="http://kramdown.gettalong.org/quickref.html">[kramdown]</a></li>
                    <li><a href="http://ralfralf.github.io/tutorial/2014/06/26/Jekyll-post-format/">[post format]</a>
                    </li>
               </ul>
                
          </div>
          
          <div class="tab-pane" id ="highlight_code">
               
               <pre class="prettyprint linenums">
                 
     public static void main(String args[]){
     
          System.out.println("Hello world!");
     }
               </pre>
          </div>
          
          
          <div class="tab-pane" id="markdown_text">
               
               <pre class="prettyprint linenums">
      #WEB tech#
      
      -HTML
      -CSS
      -Javascript
                </pre>
               
          </div>
     
     </div>

</div>

{% for post in site.posts %}
  <hr>
  <h3>{{post.title}}</h3>  
  {{post.date|date: "%Y-%m-%d"}}

  {{post.description}}

  {% if post.figure %}
<a href="{{post.url}}"><img src="{{post.figure}}"/></a>
  {% endif %}

  [阅读全文]({{post.url}})
{% endfor %}


