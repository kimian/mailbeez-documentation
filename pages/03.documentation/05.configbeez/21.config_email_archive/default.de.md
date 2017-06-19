---
# http://learn.getgrav.org/content/headers
title: Email Web-Ansicht und Archiv
slug: config_email_archive
routes:
    aliases:
        - /dokumentation/installation/config/config_email_archive
        
# menu: Email Web-Ansicht und Archiv
date: 28-04-2014
published: true
publish_date: 28-04-2014
# unpublish_date: 28-04-2014
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
    code: 'config_email_archive'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2014/04/icon_32.png'
    pro: 'pro'
    cert: 'true'
    price: '79 EUR'
    title_en: 'Web-View and Email Archive'
    teaser_en: 'Enrich you MailBeez Emails with a web-view and archive them'
    title_de: 'Email Archiv und Web-Ansicht'
    teaser_de: 'Erweitern Sie Ihre MailBeez-Emails mit einer Web-Ansicht und archivieren Sie diese.'
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

Mit dem Modul "Email Web-Ansicht und Archiv" erweitern Sie Ihr MailBeez System schnell und einfach um folgende Funktionen

## Web-Ansicht

Platzieren Sie den neuen Platzhalter

```
<a href="{$webversion_url}">Web-Ansicht</a>
```

in Ihrer Haupt- oder auch Inhalts-Vorlage. Der Empfänger wird dann mit Klick auf diesen Link auf eine Web-Seite geleitet, welche die Email als Online-Version zeigt.

## Archiv

Alle Emails werden automatisch in Text- und HTML-Version archiviert und sind komfortable über den Beez-O-Graph aber auch je Kunden im kostenfreien [BeezDesk Kunden Insight](/dokumentation/configbeez/config_customer_insight/) einsehbar - So ist leicht nachvollziehbar, welche Emails den Kunden gesendet worden sind.

Mit Hilfe der integrierten "Aufräum-Funktion" können ältere Einträge regelbasiert gelöscht werden. Dies kann manuell im Modul oder - bei entsprechender Konfiguration - automatisiert erfolgen.

## Konfiguration einer externen Datenbank

In der Standard-Konfiguration wird das Email-Archiv in der Shop-Datenbank gespeichert. 
Je nach Versende-Volumen kann das Archiv trotzt automatisierter Aufräum-Funktion eine Grösse von mehreren GBs erreichen, wodurch sich z.B. Backups der Datenbank erschweren.

Um die Shop-Datenbank nicht zu belasten, kann eine eigene Datenbank für das Email-Archiv konfiguriert werden. Die Schritte hierzu sind recht einfach: Zunächst in der Server-Administration eine neue Datenbank anlegen, dann die Zugangsdaten dieser Datenbank im Modul konfigurieren - fertig. Bei Verbindungsproblemen hilft das Modul mit entsprechenden Hinweisen weiter.

Da es sich bei den Email-Archiv-Daten um nicht kritische Daten handelt, kann auf ein Backup verzichtet werden. Es sollte aber dennoch die automatische Aufräum-Funktion aktiviert werden, um ein unkontrolliertes Anwachsen der Datenbankgrösse zu vermeiden.