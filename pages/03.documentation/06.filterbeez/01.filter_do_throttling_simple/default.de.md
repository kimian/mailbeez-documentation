---
# http://learn.getgrav.org/content/headers
title: Einfache Drosselung
slug: filter_do_throttling_simple
routes:
    - aliases: /dokumentation/filterbeez/einfache-drosselung
# menu: Einfache Drosselung
date: 08-04-2011
published: true
publish_date: 08-04-2011
# unpublish_date: 08-04-2011
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
    code: 'filter_do_throttling_simple'
    category: [filterbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    pro: 'pro'
    cert: 'true' 
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

**Dieses Filtermodul drosselt den Email Versand von MailBeez.**

>>>>>>Wir empfehlen [Newsletter2Go als Email-System](/dokumentation/configbeez/config_email_engine) zu konfiguieren. Dann brauchen Sie sich über die Einhaltung von Versende-Limits keine Gedanken zu machen.

Einige Hoster schränken den Versand von Emails ein, z.B. maximal 480 Emails pro Stunde. Mit diesem Modul stellen Sie sicher, mit MailBeez immer unter diesem Limit zu bleiben.

Bespiel:
- MailBeez wird von einem Cronjob minütlich ausgeführt
- Der Hoster erlaubt höchsten 30 Emails pro Minute
- Daher muss “Maximal Anzahl Emails per Durchlauf” unter 30 liegen, z.B. 25

Mit dieser Einstellung wird MailBeez den Versand nach 25 Emails anhalten, was nicht länger als 1 minute dauern sollte – also bevor der nächste Durchlauf startet.

