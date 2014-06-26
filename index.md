---
layout: page
title: Ralf's Blog
tagline: Articles about Java and distributed computing
---
{% include JB/setup %}

<div class="tabbable">
     
     <ul class="nav nav-tabs" id="example-tabs">
       <li class="active"><a href="#highlight_code"  data-toggle="tab">Highlight Code</a></li>
       <li><a href="#Markdown_text" data-toggle="tab">Markdown Text</a></li>
     </ul>
     
     <div class="tab-content">
          
          <div class="tab-pane active" id ="highlight_code">
               <h5>Highlight Code</h5>
               <pre class="prettyprint linenums">
                 
     public static void main(String args[]){
     
          System.out.println("Hello world!");
     }
               </pre>
          </div>
          
          
          <div class="tab-pane" id="Markdown_text">
               <h5>MarkDown text</h5>
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


