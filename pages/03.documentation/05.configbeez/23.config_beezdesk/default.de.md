---
# http://learn.getgrav.org/content/headers
title: BeezDesk CRM Integration
slug: config_beezdesk
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
    tag: [pro]
# added collection selector

author:
    name: admin
metadata:
    author: admin
module:
    code: 'config_beezdesk'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2014/04/icon_32.png'
    pro: 'pro'
    cert: 'true'
----------------

Auf dieser Seite wird die Integration des Shop-Systems mit BeezDesk CRM beschrieben
[mehr zum BeezDesk CRM](https://www.beezdesk.de)



## Installation

Kunden des BeezDesk CRM Ticketsystemes können dieses Modul mit Hilfe des MailBeez CloudLoaders installieren und aktualisieren. 


In jedem Master- und Slave-Shop muss MailBeez installiert und der passende API-Key unter `MailBeez > Konfiguration > MailBeez Cloudloader` hinterlegt werden.

Den API-Key für eine Master- oder Slave-Shop können Sie in Ihrem Kundenbereich auf <https://apps.mailbeez.de> finden bzw. erstellen. 
Neue Domains dort bitte unter `Übersicht > Tarife > BeezDesk > Details zeigen > Domain hinzufügen` anlegen. Dann den API-Key kopieren und unter `MailBeez > Konfiguration > MailBeez Cloudloader` einfügen. Danach sollten Sie den passenden Tarif in der Übersicht finden.

### Integration in das Admin-System

Bitte folgen Sie der [Anleitung zur Einbindung von BeezDesk CRM Kunden Insight](/dokumentation/configbeez/config_customer_insight). Sobald das BeezDesk System erfolgreich installiert und konfiguiert ist, werden Sie die neuen Kommunikations-Funktionen im Kunden Insight finden.

### Cronjobs

####BeezDesk Service Aufgaben

Im Installations-Verlauf wird Ihnen eine Cronjob-Url mitgeteilt, bitten richten Sie eine Cronjob ein, der diese Url z.B. alle 5Min aufruft.


####Synchronisierung von Nachrichten
Neue Nachrichten in BeezDesk erscheinen erst nach Ausführung des BeezDesk Service Modules in der Shop-Administration.

Bitte stellen Sie sicher, dass die **BeezDesk Service Module** unter `MailBeez > MailBeez Module` installiert sind.

Die Cronjob-Url finden Sie im entsprechenden Modul, diese ist wie folgt aufgebaut.

`<shop-url>/mailhive.php?m=service_beezdesk_sync&ma=sync` 


Bitte richten Sie einen Cronjob ein, der diese Service-Url alle 5Min aufruft. Die Einrichtung von Cronjobs ist bei den verschiedenen Hosting-Anbietern unterschiedlich gelöst - Bitte kontaktieren Sie ggf. den Support Ihres Hosting-Anbieters.

>>>>**Wichtig:** In Crontab `\&` statt `&` nutzen, sonst wird der URL Parameter nicht korrekt übergeben:

`wget -O - -q -t 1 <shop-url>/mailhive.php?m=service_beezdesk_sync\&ma=sync`


### Einbindung des Kontakt / Chat Widgets

>>>>> folgender Schritt ist nur bei Shop-Systemen ohne Vorintegration von MailBeez erforderlich


**Code-Block**

```
<?php
    if (defined('MAILBEEZ_BEEZDESK_CHAT_WIDGET_ID') && MAILBEEZ_BEEZDESK_CHAT_WIDGET_ID != '') {
        // Beezdesk Chat
        $beezdesk_button_id = MAILBEEZ_BEEZDESK_CHAT_WIDGET_ID;
        if (file_exists('mailhive/configbeez/config_beezdesk/includes/beezdesk_chat.php')) {
            include('mailhive/configbeez/config_beezdesk/includes/beezdesk_chat.php');
        }
        // Beezdesk Chat
    }
?>
```


#### ZenCart
Bitte den Code-Block in die Datei `/includes/modules/footer.php` einfügen


#### andere Shop-Systeme
Bitte den Code-Block in die Datei `/includes/footer.php` einfügen


## Konfiguration

Wenn Sie nur einen Shop anbinden wollen, konfigurieren Sie diesen bitten als **Master**. 
 
Bei Anbindung mehrerer Shops, muss ein Shop als **Master** und alle anderen Shops als **Slave** konfiguriert werden.

Das Konfigurations-Modul finden Sie unter `MailBeez > Konfiguration > BeezDesk Anbindung`.

### Master

Die Konfiguration das Master-Shops verbindet MailBeez mit BeezDesk. Bitten folgen Sie den Konfigurations-Möglichkeiten im Modul.


### Slave


Die Slave-Shops werden mit dem Master-Shop verbunden. Nach erfolgreicher Konfiguration meldet sich der Slave-Shop zur Freigabe im Master-Shop an.

Dann bitte im Master-Shop den Slaveshop freigeben und zuvor im BeezDesk konfigurierte Abteilungen zuweisen.
