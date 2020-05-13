{% comment %} A little snippet to put at the end of each post to direct users to the homepage {% endcomment %}

<div style="border-top-style: dashed; border-top-width: 1px;" markdown="1">
Wenn Sie diesen Artikel mit Interesse gelesen haben, schauen Sie sich die [Übersichtsseite](/CausalCovid-19/) an. 
<ul>
  {% for post in site.related_posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>
</div>

{: .info}
