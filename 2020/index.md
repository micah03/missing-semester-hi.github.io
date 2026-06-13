---
layout: page
title: "2020 व्याख्यान"
description: >
  Missing Semester, MIT IAP 2020 के व्याख्यान नोट्स और वीडियो।
permalink: /hi/2020/
phony: true
---

<ul class="double-spaced">
  {% assign lectures = site['2020'] | sort: 'date' %}
  {% for lecture in lectures %}
    {% if lecture.phony != true %}
      <li>
        <strong>{{ lecture.date | date: '%-m/%-d' }}</strong>:
        {% if lecture.ready %}
          <a href="{{ lecture.url }}">{{ lecture.title }}</a>
        {% elsif lecture.noclass %}
          {{ lecture.title }} [कक्षा नहीं]
        {% else %}
          {{ lecture.title }} [जल्द आ रहा है]
        {% endif %}
        {% if lecture.details %}
          <br>
          ({{ lecture.details }})
        {% endif %}
      </li>
    {% endif %}
  {% endfor %}
</ul>

व्याख्यानों की वीडियो रिकॉर्डिंग [YouTube पर उपलब्ध हैं](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuloKGG59rS43e29ro7I57J)।

# MIT से आगे

हमने यह कक्षा MIT के बाहर भी साझा की है, ताकि और लोग इन संसाधनों का लाभ उठा सकें। इसके बारे में चर्चा और पोस्ट यहाँ देखी जा सकती हैं:

 - [Hacker News](https://news.ycombinator.com/item?id=22226380)
 - [Lobsters](https://lobste.rs/s/ti1k98/missing_semester_your_cs_education_mit)
 - [r/learnprogramming](https://www.reddit.com/r/learnprogramming/comments/eyagda/the_missing_semester_of_your_cs_education_mit/)
 - [r/programming](https://www.reddit.com/r/programming/comments/eyagcd/the_missing_semester_of_your_cs_education_mit/)
 - [Twitter](https://twitter.com/jonhoo/status/1224383452591509507)
 - [YouTube](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuloKGG59rS43e29ro7I57J)

# आभार

हम Elaine Mello, Jim Cain, और [MIT Open Learning](https://openlearning.mit.edu/) का आभार व्यक्त करते हैं, जिनकी मदद से हम व्याख्यान वीडियो रिकॉर्ड कर पाए; Anthony Zolnik और [MIT AeroAstro](https://aeroastro.mit.edu/) का A/V उपकरणों के लिए; तथा Brandi Adams और [MIT EECS](https://www.eecs.mit.edu/) का इस कक्षा के समर्थन के लिए।