---
# http://learn.getgrav.org/content/headers
title: Gambio GX 2.x
slug: basic-installation-gambio-gx-2
# menu: Gambio GX 2
date: 15-06-2011
published: true
publish_date: 15-06-2011
# unpublish_date: 15-06-2011
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
    tag: [ftp]
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

>>>>**MailBeez ist ab Gambio 2.3 vorintegriert**<br>wenn Sie Gambio 2.3+ nutzen, bitte MailBeez über das Admin Menü per Klick installieren. Die folgenden Schritte dürfen nicht ausgeführt werden.

- - - - - -

MailBeez arbeitet problemlos mit *Gambio GX 2.x*.

Die Installation ist in wenigen Schritten erledigt:
- Die neuen Dateien übertragen
- Menü-Eintrag anlegen (frühe Gambio 2 Versionen)
- Zugriffs-Rechte für den Admin vergeben (halb automatisch)
- MailBeez per Button-Klick installieren

MailBeez verwaltet eigene Tabellen - die vorhandenen Shop-Tabellen werden nicht verändert.


## Schritt 1: Neue Dateien

[plugin:content-inject](/content_blocks/download_installer)


folgende Dateien und Ordner aus dem entpackten Zip-Archiv auf den Shop-Server übertragen:

### MailBeez Installer

```bash
admin/mailbeez.php
mailhive/
mailhive.php


```


### Integration

folgende Dateien und Ordner aus dem entpackten Zip-Archiv


```bash 
/extra files/extras_gambio2.x 


```


auf den Shop-Server übertragen:

```bash
Menue
/system/conf/admin_menu/menu_mailbeez.xml
/admin/includes/mailbeez/images/mailbeez_gambio_icon.png

CRM Pad und BeezDesk Kunden Insight
/system/overloads/AdminApplicationBottomExtenderComponent/BeezDesk.inc.php

Dynamische Erweiterung des MailBeez Menues
/system/overloads/AdminApplicationTopExtenderComponent/MailBeezAdminApplicationTopExtender.inc.php

Einbindung des clicktrackers
/system/overloads/ApplicationTopExtenderComponent/MailBeezAnalyticsClicktracker.inc.php

Einbindung der Shopbewertungs-Box
/system/overloads/ApplicationTopExtenderComponent/MailBeezShopvotingDefault.inc

Frontend-Hook fuer MailBeez automatisch ausfuehren und MailBeez BigData Tracking
/system/overloads/ApplicationBottomExtenderComponent/MailBeezExtender.inc.php



```



## Schritt 2 - Menü-Eintrag anlegen

#### Gambio GX2 frühe Version

folgende Datei öffnen:

```bash 
admin/includes/column_left.php  


```


finde

``` 
' . BOX_CUSTOMERS_STATUS . '<span style="font-family: Georgia, 'Times New Roman', 'Bitstream Charter', Times, serif; font-size: 13px; line-height: 19px;">;


```


Danach in einer neuen Zeile folgendes einfügen:



``` 
if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['mailbeez'] == '1')) 
    echo '<ul>
            <li><a id="BOX_MAILBEEZ" href="' . xtc_href_link('mailbeez.php') . '"> MailBeez</a></li>
          </ul>';

```



Dies platziert den Menü-Eintrag "MailBeez" im Abschnitt "Kunden"

#### Gambio GX2 mit Service Pack

Wenn der obige Eintrag nicht zu finden ist, ist Service Pack 1.1 installiert. Dann sollte der Menü-Eintrag bereits mit Hilfe der Integrations-Dateien angelegt werden.

Wenn dies auch nach Schritt 3 nicht funktioniert, bitte den Menü-Eintrag wie folgt manuell anlegen:

folgende Datei öffnen:

 
```
admin/includes/column_left.php  

```



finde


```
# SAMPLE ITEM:

```



darüber folgenden Code in eine neue Zeile einfügen


```
if (($_SESSION['customers_status']['customers_status_id'] == '0') && ($admin_access['module_newsletter'] == '1')) 
    echo '<ul>
            <li><a id="BOX_MAILBEEZ" href="' . xtc_href_link('mailbeez.php') . '">MailBeez</a></li>
          </ul>';


```


## Schritt 3 - Zugriffsrechte vergeben

einmalig


```
http://(shop)/mailhive.php


```


im Browser aufrufen.

Hierdurch werden die erforderlichen Admin-Rechten für den HAUPT-Admin vergeben.

Nach einem erneuten Login und leeren des Seiten-Caches wird MailBeez im Abschnitt "Zusatzmodule" erscheinen.

Falls erforderlich dann Zugriffs-Rechte im Gambio-Admin System für weitere Admin-user vergeben


[plugin:content-inject](/content_blocks/run_installer)