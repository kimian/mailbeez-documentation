---
# http://learn.getgrav.org/content/headers
title: BeezDesk CRM Kunden Insight
slug: config_customer_insight
# menu: BeezDesk Kunden Insight
date: 22-03-2013
published: true
publish_date: 22-03-2013
# unpublish_date: 22-03-2013
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
    tag: [core]
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

Das erweiterbare BeezDesk CRM Kunden Insight Modul hilft Ihnen, mit einer kunden-zentrischen Ansicht der relevanten Daten aus Ihrem Shop **das Verständnis über Ihre Kunden sowie Ihren Kunden-Service zu verbessern**.

Die modulare Kunden-Insight Ansicht kann von jeder Admin-Seite mit Kunden-Informationen (Kunden, Bestellungen) geöffnet werden, während das BeezDesk CRM Pad schnell von jeder Seite aus erreicht werden kann.

Entwickler können leicht die Kunden-Insight Ansicht mit Modulen erweitern, welche beispielsweise kunden-relatierte Daten aus Dritt-Systemen einbinden und somit die Entwicklungs-Aufwände auf ein Minimum reduzieren. Dabei bleibt das System voll update-fähig, da keine Kern-Dateien verändert werden brauchen.

Die Kunden-Insight Ansicht gibt Ihnen einen sofortigen Überblick aller Bestellungen, gekaufter Produkte usw. zu einem Kunden und kann zu einem voll ausgestatteten, professionellen Multichannel Kunden Support System für Email, LiveChat, Facebook, Twitter, Telefone sowie Formulare, Knowledgebase, Foren und Vorschlag-Tafeln erweitert werden. Dies erlaubt Shop-Betreibern, alle modernen Kommunikations-Kanäle zu konsolidieren sowie die Kunden-Service Prozesse zu optimieren.

[mehr zum BeezDesk CRM](https://www.beezdesk.de)

>>>>>[plugin:content-inject](/content_blocks/hint_preintegration)


### Installation

Um das BeezDesk CRM Pad sowie den BeezDesk Kunden-Insight Button auf allen Seiten der Shop-Administration einzubinden, bitte folgendes durchführen:


**Alle Systeme**

öffne 

`(shop)/<admin-dir>/includes/footer.php`

vor dem schliessenden PHP Tag `?>`  folgenden Code einfügen

```
// BOF: Mailbeez Customer Insight
define('MH_DIR_FS_CATALOG', (substr(DIR_FS_CATALOG, -1) != '/') ? DIR_FS_CATALOG . '/' : DIR_FS_CATALOG);
@include(MH_DIR_FS_CATALOG . '/mailhive/configbeez/config_customer_insight/includes/admin_footer_include.php');
// EOF: Mailbeez Customer Insight
```




Weitere Installations-Anweisungen:


**Modified-Shop**

öffne

 
`(shop)/<admin-dir>/start.php`


vor dem schliessenden HTML Tag `</body>` folgenden Code einfügen:

```
<?php
// BOF: Mailbeez Customer Insight
define('MH_DIR_FS_CATALOG', (substr(DIR_FS_CATALOG, -1) != '/') ? DIR_FS_CATALOG . '/' : DIR_FS_CATALOG);
@include(MH_DIR_FS_CATALOG . '/mailhive/configbeez/config_customer_insight/includes/admin_footer_include.php');
// EOF: Mailbeez Customer Insight
?>
```



**Zencart**

öffne

 
`(shop)/<admin-dir>/index.php`


vor dem schliessenden HTML Tag `</body>` folgenden Code einfügen:

```
<?php
// BOF: Mailbeez Customer Insight
define('MH_DIR_FS_CATALOG', (substr(DIR_FS_CATALOG, -1) != '/') ? DIR_FS_CATALOG . '/' : DIR_FS_CATALOG);
@include(MH_DIR_FS_CATALOG . '/mailhive/configbeez/config_customer_insight/includes/admin_footer_include.php');
// EOF: Mailbeez Customer Insight
?>
```
