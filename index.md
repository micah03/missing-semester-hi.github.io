---
layout: page
title: आपके CS शिक्षा का मिसिंग सेमेस्टर
description: >
  ऐसे शक्तिशाली टूल्स सीखें जो आपको एक अधिक उत्पादक कंप्यूटर वैज्ञानिक और प्रोग्रामर बनाएंगे।
subtitle: "2026"
nositetitle: true
---

कंप्यूटर विज्ञान के पाठ्यक्रम आपको ऑपरेटिंग सिस्टम से लेकर मशीन लर्निंग तक कई उन्नत विषय सिखाते हैं, लेकिन एक महत्वपूर्ण विषय अक्सर छूट जाता है और विद्यार्थियों को उसे खुद समझना पड़ता है: अपने टूल्स में दक्षता। हम आपको कमांड-लाइन का उपयोग करना, एक शक्तिशाली टेक्स्ट एडिटर इस्तेमाल करना, वर्ज़न कंट्रोल सिस्टम्स की उन्नत सुविधाएँ अपनाना, और बहुत कुछ सिखाएँगे।

अपनी पढ़ाई के दौरान छात्र इन टूल्स के साथ सैकड़ों घंटे, और अपने करियर में हज़ारों घंटे, बिताते हैं। इसलिए अनुभव को जितना संभव हो उतना सहज और सरल बनाना समझदारी है। इन टूल्स में दक्षता न केवल आपको अपने टूल्स को अपने हिसाब से ढालने में कम समय खर्च करने देती है, बल्कि पहले असंभव लगने वाली समस्याएँ हल करने में भी मदद करती है।

आजकल सॉफ़्टवेयर इंजीनियरिंग के कई पहलू AI-सक्षम और AI-वर्धित टूल्स तथा कार्यप्रवाहों के कारण तेज़ी से बदल रहे हैं। जब इनका उचित उपयोग किया जाए और उनकी सीमाओं को समझा जाए, तो ये कंप्यूटर विज्ञान के अभ्यासकर्ताओं के लिए बड़े लाभ दे सकते हैं; इसलिए इनके बारे में व्यावहारिक समझ विकसित करना उपयोगी है। चूँकि AI एक क्रॉस-फ़ंक्शनल सक्षमकारी तकनीक है, इसलिए इसके लिए कोई अलग से AI व्याख्यान नहीं है; इसके बजाय हमने नवीनतम प्रासंगिक AI टूल्स और तकनीकों का उपयोग हर व्याख्यान में सीधे शामिल किया है।

इस कक्षा के पीछे की प्रेरणा के बारे में [यहाँ पढ़ें](/about/)।

# पाठ्यक्रम-सूची

<ul>
{% assign lectures = site['2026'] | sort: 'date' %}
{% for lecture in lectures %}
    {% if lecture.phony != true %}
        <li>
        <strong>{{ lecture.date | date: '%-m/%-d/%y' }}</strong>:
        {% if lecture.ready %}
            <a href="{{ lecture.url }}">{{ lecture.title }}</a>
        {% else %}
            {{ lecture.title }} {% if lecture.noclass %}[कोई कक्षा नहीं]{% endif %}
        {% endif %}
        </li>
    {% endif %}
{% endfor %}
</ul>

## पिछले वर्षों के विशेष विषय

हम जो विषय पढ़ाते हैं वे साल-दर-साल बदलते रहते हैं। जिन विद्यार्थियों को वर्षों के दौरान पढ़ाए गए पूरे विषय-संग्रह में रुचि है, उनके लिए हमने पिछले वर्षों के वे विषय भी दिखाए हैं जिन्हें 2026 में शामिल नहीं किया गया।

{% assign sorted_collections = site.collections | sort: 'label' | pop | reverse %}
<ul>
{% for collection in sorted_collections %}
    {% assign grouped_lectures = site[collection.label] | group_by: 'date' | sort: 'name' %}
    {% for group in grouped_lectures %}
        {% assign sorted_lectures = group.items | sort: 'order' %}
        {% for lecture in sorted_lectures %}
            {% if lecture.special == true %}
                <li>
                    <strong>{{ lecture.date | date: '%-m/%-d/%y' }}</strong>:
                    <a href="{{ lecture.url }}">{{ lecture.title }}</a>
                </li>
            {% endif %}
        {% endfor %}
    {% endfor %}
{% endfor %}
</ul>

# सामान्य जानकारी

**शिक्षकगण**: यह कक्षा Anish, Jon, और Jose द्वारा संयुक्त रूप से पढ़ाई जाती है।<br>
**प्रश्न**: हमें [missing-semester@mit.edu](mailto:missing-semester@mit.edu) पर ईमेल करें।<br>
**चर्चा**: [OSSU Discord](https://ossu.dev/#community) (Piazza की तरह `#missing-semester-forum` का उपयोग करें, और कक्षा/शिक्षकों से बात करने के लिए `#missing-semester` चैनल का उपयोग करें)।

# MIT से आगे

हमने यह कक्षा MIT के बाहर भी साझा की है, ताकि और लोग इन संसाधनों का लाभ उठा सकें। इसके बारे में चर्चा और पोस्ट यहाँ देखी जा सकती हैं:

 - Hacker News ([2026](https://news.ycombinator.com/item?id=47124171), [2020](https://news.ycombinator.com/item?id=22226380), [2019](https://news.ycombinator.com/item?id=19078281))
 - Lobsters ([2026](https://lobste.rs/s/q4ykw7/missing_semester_your_cs_education_2026), [2020](https://lobste.rs/s/ti1k98/missing_semester_your_cs_education_mit), [2019](https://lobste.rs/s/h6157x/mit_hacker_tools_lecture_series_on))
 - r/learnprogramming ([2026](https://www.reddit.com/r/learnprogramming/comments/1r93yk6/the_missing_semester_of_your_cs_education_2026/), [2020](https://www.reddit.com/r/learnprogramming/comments/eyagda/the_missing_semester_of_your_cs_education_mit/), [2019](https://www.reddit.com/r/learnprogramming/comments/an42uu/mit_hacker_tools_a_lecture_series_on_programmer/))
 - r/programming ([2020](https://www.reddit.com/r/programming/comments/eyagcd/the_missing_semester_of_your_cs_education_mit/), [2019](https://www.reddit.com/r/programming/comments/an3xki/mit_hacker_tools_a_lecture_series_on_programmer/))
 - X ([2026](https://x.com/anishathalye/status/2024521145777848588), [2020](https://twitter.com/jonhoo/status/1224383452591509507), [2019](https://x.com/jonhoo/status/1090323977766137858))
 - Bluesky ([2026](https://bsky.app/profile/jonhoo.eu/post/3mfa2bhyuj22i))
 - Mastodon ([2026](https://fosstodon.org/@jonhoo/116098318361854057))
 - LinkedIn ([2026](https://www.linkedin.com/posts/anishathalye_i-returned-to-mit-during-iap-january-term-activity-7430285026933522433-Ehr9))
 - YouTube ([2026](https://www.youtube.com/playlist?list=PLyzOVJj3bHQunmnnTXrNbZnBaCA-ieK4L), [2020](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuloKGG59rS43e29ro7I57J), [2019](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuiujH1lpn8cA9dsyulbYRv))

# अनुवाद

{% comment %} keep these in alphabetical order {% endcomment %}

- [Arabic](https://missing-semester-ar.github.io/)
- [Bengali](https://missing-semester-bn.github.io/)
- [Chinese (Simplified)](https://missing-semester-cn.github.io/)
- [Chinese (Traditional, Taiwan)](https://missing-semester-tw.github.io/)
- [German](https://missing-semester-de.github.io/)
- [Hindi](https://micah03.github.io/missing-semester-hi.github.io/)
- [Italian](https://missing-semester-it.github.io/)
- [Japanese](https://missing-semester-jp.github.io/)
- [Kannada](https://missing-semester-kn.github.io/)
- [Korean](https://missing-semester-kr.github.io/)
- [Persian](https://missing-semester-fa.github.io/)
- [Portuguese](https://missing-semester-pt.github.io/)
- [Russian](https://missing-semester-rus.github.io/)
- [Serbian](https://netboxify.com/missing-semester/)
- [Spanish](https://missing-semester-esp.github.io/)
- [Swedish](https://den-saknade-terminen.l10n.se/)
- [Telugu](https://micah03.github.io/missing-semester-te.github.io/)
- [Thai](https://missing-semester-th.github.io/)
- [Turkish](https://missing-semester-tr.github.io/)
- [Vietnamese](https://missing-semester-vn.github.io/)

ध्यान दें: ये समुदाय द्वारा किए गए बाहरी अनुवाद हैं। हमने इन्हें जाँचा या सत्यापित नहीं किया है।

क्या आपने इस कक्षा के नोट्स का अनुवाद बनाया है? इसे सूची में जोड़ने के लिए एक [pull request](https://github.com/missing-semester/missing-semester/pulls) भेजें।