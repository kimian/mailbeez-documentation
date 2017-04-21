---
# http://learn.getgrav.org/content/headers
title: Email System
slug: config_email_engine
routes:
    aliases:
        - /dokumentation/installation/config_queen/email-engine-configuration
        - /dokumentation/installation/config/config_email_engine
        
# menu: Email Engine Konfiguration
date: 26-03-2012
published: true
publish_date: 26-03-2012
# unpublish_date: 26-03-2012
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

MailBeez gibt Ihnen volle Freiheit zu wählen, wie Sie die Emails versenden wollen:

##Mögliche E-Mail Versand Methoden für MailBeez

1. **Shop (Standard)**: Email-Funktion des Shop-Systems
1. **Newsletter2Go (empfohlen)**: Versand über die zertifizierten Server von Newsletter2Go
1. **SMTP**: Ein beliebiger SMTP Server

###Shop (Standard)

Als Standard-Einstellung nutzt MailBeez die Email Funktion des Shop Systems. Somit wird die ggf. im Shop System konfigurierbare Methode zum Email Versand genutzt.
 
| Vorteile                               | Nachteile 
|----------------------------------------|----------------------------------------------
| keine Konfiguration erforderlich       | ggf. Versende-Limit des Mail-Servers     
| keine zusätzlichen Kosten              | Risiko eines Spam-Ratings auf dem Mail-Server         
|                                        | Zustellraten sind vom Mail-Server abhängig, typisch unter 50%         



###Newsletter2Go (empfohlen)
Newsletter2Go ist ein in Berlin ansässiger Anbieter für den Versand von Emails **mit einer Zustellrate von 99,5%** dank zertifizierter Server:

Newsletter2Go schreibt:

>Versenden Sie über eines der besten Versandsysteme weltweit. Eine Versandgeschwindigkeit von 3 Millionen Emails in der Stunde pro Kunde erfüllt jeden Anspruch. **Newsletter2Go sorgt dafür, dass Ihre Emails nicht von Spam-Filtern geprüft, sondern direkt an die Empfänger zugestellt werden**.

 
| Vorteile                                                   | Nachteile 
|------------------------------------------------------------|----------------------------------------------
| Versand über zertifizierte Server mit 99,5% Zustellrate    | SPF Konfiguration sinnvoll
| Whitelisting für 2,4 Milliarden Emails                     | zusätzliche Kosten, welche aber **durch verbesserte Zustell-Raten gedeckt werden** sollten     
| Keine Drosselung erforderlich                              |  |
| Kein Problem mit Spam-Listen, Blacklist etc.               |  |
| 1000 Email gratis pro Monat                                |  |


[Tutorial zur Einrichtung](/dokumentation/tutorials/newsletter2go-integration-mailbeez)

>>>>>> Im MailBeez System können Sie sich direkt bei Newsletter2Go registrieren. Dabei wird die Integration automatisch konfiguriert und nach Freischaltung Ihres Kontos können Sie sofort MailBeez über die Server von Newsletter2Go versenden lassen.


### SMTP

Mit dieser Option können Sie MailBeez für den Versand über einen beliebigen SMTP Server konfigurieren.

| Vorteile                                    | Nachteile 
|---------------------------------------------|----------------------------------------------
| jeder SMTP Server kann konfiguriert werden  | Konfigurations-Aufwand
| Unterstützung für DKIM                      | Risiko eines Spam-Ratings auf dem Mail-Server    
| keine zusätzlichen Kosten                   | Zustellraten sind vom Mail-Server abhängig, typisch unter 50%  |



Einstellungen für die Verwendung eines Gmail Email-Servers:
```bash
 smtp.gmail.com  
 Auth: true  
 security: ssl  
 Port: 465
```




### Fehler beim Email-Versand <a id="error"></a>

Falls der Versand einer Email über SMTP aus verschiedensten Gründen im Email-Server fehl schlägt, wird diese Email im System mit der `message_id=-1` protokolliert. 

In der System-Status Übersicht wird Ihnen angezeigt, wie viele Fehler beim Email-Versand aufgetreten sind. 

Mit Klick auf das Werkzeug-Symbol können Sie zwischen folgenden Aktionen zur Problembehebung wählen: 

####Neu Starten
Die betroffenen Einträge werden im System gelöscht, so dass diese Emails - je nach Zeitpunkt und Modul-Konfiguration - erneut versendet werden können.

####Ignorieren
Die betroffenen Einträge werden im System markiert, so dass diese Emails nicht erneut versendet werden.


>>>>>>Sollten häufig Fehler beim Versand auftreten, so prüfen Sie bitte die Konfiguration des verwendeten SMTP-Servers. Einige SMTP-Server können z.B. so konfiguriert sein, dass nur bestimmte Absender-Domains zugelassen werden. Bei abweichenden Absender-Domains verweigert der SMTP-Server dann den Versand mit einer Fehlersituation. 