---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: page-fullwidth
header: no

#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
title: "Advanced Compiler Design (UCSD CSE231)"
---

**Prof**: Joe Gibbs Politz - <code>jpolitz@eng.ucsd.edu</code> -  [jpolitz.github.io](https://jpolitz.github.io)

**Staff**:

- Yousef Alhessi - <code>yalhessi@eng.ucsd.edu</code> -  [yalhessi.github.io](https://yalhessi.github.io/)
- Kamran Alipour - <code>kalipour@eng.ucsd.edu</code> -  [kamranalipour.github.io](https://kamranalipour.github.io/)
- Vignesh Gokul

## Basics

- Lectures: Tue/Thu, 11-12:30, Center 214
- Assignment submission/grades: [https://www.gradescope.com/courses/222971](https://www.gradescope.com/courses/222971)
- Piazza: [https://piazza.com/class/l19qaxisql23rt](https://piazza.com/class/l19qaxisql23rt)

## Material and Schedule

<ul class="material">
    {% for post in site.categories.week reversed %}
    <li class="{% if post.current %}current{% else %}gray{% endif %}">
    <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    <ul>
    <li>Readings
    <ul>
      {% for reading in post.readings %}
      <li><a href="{{ reading.url }}">{{ reading.name }}</a></li>
      {% endfor %}
    </ul>
    </li>
    <li>Due Dates
    <ul>
      {% for todo in post.todos %}
      <li><a href="{{ todo.url }}">{{ todo.name }}</a> - Due {{ todo.due-date }}</li>
      {% endfor %}
    </ul>
    </li>
    </ul>
    </li>
    {% endfor %}
</ul>

## Course Calendar

This calendar shows rooms for scheduled in-person lecture and office hours.

<iframe src="https://calendar.google.com/calendar/embed?src=c_7e2gtpsag8juqtr68d7khv0940%40group.calendar.google.com&ctz=America%2FLos_Angeles" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
