---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: "home"
---

This is the index file which we will use for the website.
The index file as the name suugests uis 

 {% for post in site.posts%}
  <li><a href="{{post.url}}">{{post.title}}</a></li>
 {%if post.title=="Welcome to Jekyll!"%}
 <h1> 1st post and if called</h1>
 {%else%}
 <h1> Not 1st if and in else now </h1>


    {%endif%}
    {% endfor %}


{%for data in site.data.people%}
{{data.name}}, {{data.Corp}}
{%endfor%}


{% for data in site.static_files%}
{{data.path}} {{data.extname}}{{data.name}}{{data.basename}}
{%endfor%}


{% for file in site.static_files%}
{{file.image}}
{%endfor%}