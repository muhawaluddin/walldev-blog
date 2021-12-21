---
draft: true
date: {{ .Date | time.Format ":date_full" }}
title: "{{ replace .TranslationBaseName "-" " " | title }}"
slug: {{ .BaseFileName }}

tags:
    - Python

categories:
    - Pemrograman


image: ![](/img/hugo-logo.png)
thumbnail: ![](/img/hugo-logo.png)
---
