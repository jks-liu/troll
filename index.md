---
layout: page
title: Welcome to machine learning
tagline: You can find everything here
---
{% include JB/setup %}

> (Machine learning gives) computers the ability to learn without being explicitly programmed.
>
> -- <cite>Arthur Samuel in 1959</cite>

> A computer program is said to learn from experience _E_ with respect to some class of tasks _T_ and performance measure _P_ if its performance at tasks in _T_, as measured by _P_, improves with experience _E_.
>
> -- <cite>Tom M. Mitchell</cite>

## Articles

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
