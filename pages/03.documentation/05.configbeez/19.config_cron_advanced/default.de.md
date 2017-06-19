---
# http://learn.getgrav.org/content/headers
title: Zeitsteuerung
slug: config_cron_advanced
# menu: MailBeez automatisch ausführen - Profi
date: 02-12-2013
published: true
publish_date: 02-12-2013
# unpublish_date: 02-12-2013
template: docs
# theme: false
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category: [docs]
    tag: [pro]
module:
    code: 'config_cron_advanced'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2013/12/icon_cron_64.png'
    pro: 'pro'
    cert: 'true'
    price: '99 EUR'
    title_en: 'Run MailBeez Automatically Advanced'
    teaser_en: 'Add automation and powerful time control - also great in combination with traditional cronjobs'
    title_de: 'MailBeez automatisch ausführen - Profi'
    teaser_de: 'Automatisierung und volle Zeitkontrolle - auch gerade in Kombination mit traditionellen Cronjobs'
    author: 'MailBeez.com'
# added collection selector

author:
    name: admin
metadata:
    author: admin
#      description: Your page description goes here
#      keywords: HTML, CSS, XML, JavaScript
#      robots: noindex, nofollow
#      og:
#          title: The Rock
#          type: video.movie
#          url: http://www.imdb.com/title/tt0117500/
#          image: http://ia.media-imdb.com/images/rock.jpg
#  cache_enable: false
#  last_modified: true
---

Mit dem "Zeitsteuerung" Modul erhalten Sie volle Kontrolle über den Versende-Zeitpunkt jedes Modules.

**Vorteile**

- Sie können einfach kontrollieren, an welchen Wochentagen und zu welcher Stunde die jeweiligen Emails versendet werden.  
Z.B. können Sie eine Willkommens-Email, in der Sie Ihre schnelle Hilfe anbieten, nur während Ihrer Geschäftszeiten versenden.
- Reduzierung der Server-Last.  
Abhängig von Ihrem Server, Anzahl der MailBeez Module und Konfiguration kann der Versende-Prozess die Grenzen Ihres Servers erreichen. Mit Hilfe dieses Modules können Sie die Ausführung der einzelnen Module aufteilen und somit die Last reduzieren.



**Einrichtung:**

Das Modul "Zeitsteuerung" enthält die Automatik-Funktion des "[MailBeez automatisch ausführen](/dokumentation/configbeez/config_cron_simple)" Modules, um den Traffic auf der Website zur Ausführung des Versende Prozesses zu nutzen. Dies passiert asynchron, d.h. die Ladezeiten werden nicht negativ beeinflusst.

**Für beste Zuverlässigkeit bitte einen traditionellen Cronjob einrichten, welche die MailBeez Cronjob-URL z.B. alle 5 Minuten ausführt und dann in dem Modul einfach und flexible die Zeitsteuerung je Modul konfigurieren.**
 
Somit sind die Ausführungs-Zeiten nicht vom Besucher-Traffic abhängig.
