---
title: Microsoft Learn - Latihan Dasar-Dasar Azure AI
permalink: index.html
layout: home
---

# Latihan Dasar-Dasar AI Azure

Latihan langsung ini dirancang untuk mendukung konten pelatihan di [Microsoft Learn](https://docs.microsoft.com/training/).

Untuk menyelesaikan latihan ini, Anda harus berlangganan Microsoft Azure Anda dapat mendaftar untuk uji coba gratis di [https://azure.microsoft.com](https://azure.microsoft.com).

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions'" %}
| Latihan |
| ------- | 
{% untuk aktivitas di lab %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
