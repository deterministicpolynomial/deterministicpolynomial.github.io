# Welcome to PrimeProofs!

Mathematics is more than just numbers—it's a world of patterns, logic, and elegant structures waiting to be uncovered. PrimeProofs is a blog dedicated to exploring the beauty of discrete mathematics and theoretical computer science, one proof at a time.

Here, you'll find a collection of theorems, proofs, and intriguing mathematical discoveries spanning topics like combinatorics, graph theory, number theory, logic, and algorithm analysis. Whether you're a student, researcher, or simply a curious mind, this space is for anyone who appreciates the art of rigorous reasoning and the power of abstraction.

{% assign all_posts = site.posts | sort: 'date' %}

<ul>
  {% for post in all_posts %}
    <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
  {% endfor %}
</ul>
