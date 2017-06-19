---
# http://learn.getgrav.org/content/headers
title: Newsletter Profi
slug: newsletter
routes:
    aliases:
        - /dokumentation/mailbeez/mb_newsletter
# menu: Newsletter Profi
date: 11-08-2011
published: true
publish_date: 11-08-2011
# unpublish_date: 11-08-2011
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
    tag: [pro,coupon]
module:
    code: 'mb_newsletter'
    category: [mailbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/10/icon_32.png'
    pro: 'pro'
    cert: 'true'
    price: '179 EUR'
    title_en: 'Newsletter Advanced'
    teaser_en: 'The Newsletter Module for MailBeez, with Segmentation, Coupons and more'
    title_de: 'Newsletter Profi'
    teaser_de: 'Das Newsletter Module für MailBeez, mit Segmentierung, Gutscheinen und mehr'
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

Das MailBeez Newsletter Profi Modul ist eine grundlegende Neu-Entwicklung und ein neu-gedachter Ansatz eines mit dem Shop-System voll integrierten Newsletter Systems.

[plugin:content-inject](/content_blocks/pro_responsive_template)

Die Standard-Newsletter Funktion von osCommerce, Gambio, ModifiedShop & Zencart ist rudimentär und zeigt in der Praxis eine Vielzahl an Schwächen. Einige der System-Anbieter raten von dem Einsatz dieser Standard-Funktionen ab.

Mit dem MailBeez Newsletter Profi-Modul wird diese Lücke geschlossen und Shopbetreiber können nun endlich zuverlässig professionelle Newsletter direkt aus dem Shopsystem versenden. Da das MailBeez Newsletter Profi Modul direkt in das Shopsystem eingebettet ist, müssen keine Daten exportiert oder importiert werden. Es kann sofort ein Newsletter an z.B. alle Kunden mit einem aktiven Newsletter-Abo versendet werden.

[plugin:youtube](https://www.youtube.com/watch?v=Azs3fV7MD60)    


Das Erstellen von Newslettern wird mit dem MailBeez Newsletter Profi Modul denkbar einfach gemacht: der Visuelle Editor ermöglicht das Verfassen von professionellen Newslettern, welche bestmöglich in den wichtigsten Email-Programmen dargestellt werden. In Kombination mit der [Responsive Vorlagen-Verwaltung](/dokumentation/configbeez/config_tmplmngr) können auch mobil-freundliche Newsletter erstellt werden, welche optimal auf z.B. iPhones dargestellt werden.


#### Freie Wahl des Email-Servers

Die Öffnungs- und Konvertierungs-Raten Ihrer Newsletter hängen stark vom versendenden Email-Server ab. MailBeez bietet Ihnen die freie Wahl, ob Sie über die Email-Funktion Ihres Shop-Servers, einen SMTP Server oder aber zertifizierten Server unseres Partners Newsletter2Go versenden möchten ([mehr zur Konfiguration des Email-Systems](/dokumentation/configbeez/config_email_engine)).

#### Mächtige Segmentierungs-Möglichkeiten

Dank der tiefen Integration von MailBeez mit dem Shopsystem kann das Newsletter Profi-Modul auf alle vorhandenen Daten zugreifen. Die eingebaute Segmentierungs-Engine erlaubt es Ihnen, Kunden nach Kauf-Verhalten und weiteren Parametern (Geographie, Demographie) personalisiert zu erreichen!

Die freie Kombinierbarkeit der Segmentierungsregeln eröffnen eine Vielzahl von Möglichkeiten, zielgerichtete Newsletter zu versenden:

##### Beispiele


**Upsell / Cross-Sell**

- Segmentierung: Kunden, welche Produkt A aber nicht Produkt B gekauft haben
- Gutschein: freie Versandkosten innerhalb von 7 Tagen

**Produkt-Warnhinweis / Rückruf an alle betroffenen Kunden**

- Segmentierung: Kunden, welche Produkt X gekauft habe + Umgehung des Newsletter-Abo



**Einmalige Weihnachtsgeschäfts-Kunden vom letzten Jahr**

- Segmentierung: 1 Kauf im Zeitraum 1. Oktober 2012 bis 31. Dezember 2012
- Gutschein: 10%, gültig 14 Tage

**Feiertags-Newsletter an alle Kunden**

- Vorprogrammierung des Versende-Datums
- keine weitere Segmentierung

**Willkommens-Newsletter Serie**

- Segmentierung: Kunde seit mindestens / höchstens Tagen


### Funktionen


**Vereinheitlichte Kontakte: Kunden und Interessenten**

- Saubere Unterscheidung zwischen Kunde und Interessent
- Erkennung, ob eine Email-Adresse zu einem Kunden oder Interessenten gehört
- vollständige Unterstützung bei Konvertierung von Interessent zu Kunde


**Themenbereiche**

- Anlegen, bearbeiten und Löschen von Themenbereichen
- unbegrenzte Anzahl an Themenbereichen
- öffentlich und nicht-öffentliche Themenbereiche
- automatische Zuordnung von Themenbereichen über die Anmeldeformular-API
- Empfänger können die Zuordnung zu öffentlichen Themenbereichen selbst konfigurieren, 


**Listen**

- Anlegen, bearbeiten und Löschen von Empfängerlisten
- unbegrenzte Anzahl an Empfängerlisten
- Liste-Quellen: Shop-Kunden mit Abo, Alle Shop-Kunden, Interessenten
- Segmentierung der Listen nach folgend aufgeführten Kriterien
- Testen von Segmentierungen


**Segmentierungs-Möglichkeiten**

Kunden
- Geografisch: Land, Bundesland, Plz
- Kunde: Geschlecht, Kunde seit mindestens / höchstens Tagen, Kunden-Gruppe: erfordert [Kundengruppen-Filter](/dokumentation/filterbeez/filter_check_group)
- Produkte: gekaufte Produkte (Whitelist & Blacklist)
- Kategorien: gekaufte Produkte (Whitelist & Blacklist)
- Bestellungen: max. Anzahl Bestellungen, letzte Bestellung nach Datum & vor Datum
- Listen basierend auf Quelle "Shop-Kunden mit Abo": Konfiguration von Ländern, für die ein Newsletter Abo nicht erforderlich ist
- Themenbereiche

Interessenten
- Themenbereiche

**Kampagnen**

- Anlegen, bearbeiten und Löschen von Kampagnen
- unbegrenzte Anzahl an Kampagnen
- eine Kampagne kann unbegrenzt viele Newsletter enthalten
- Zuweisen einer Standard-Liste (kann auf Newsletter ebene überschrieben werden)

**Newsletter**

- Aktiv von Datum bis Datum
- Auswahl eine Liste (oder Kampagnen-Standard)
- Auswahl einer Gutschein-Vorlage
- Konfiguration der Gutschein-Gültigkeit in Tagen

**Gutscheine**

- basiert auf dem MailBeez Gutschein-Generator
- Anlegen von Gutschein-Vorlagen mit allen zur Verfügung stehenden Optionen
- automatische Generierung von personalisierten Gutscheinen
- Gültigkeit in Tagen und Gutschein-Code-Länge konfigurierbar

**Statistiken**

- Volle Integration mit MailBeez Analytics bzw. Google Analytics
- Auswertung von Öffnen, Click, Bestellung



**Weitere Informationen finden Sie auf**

- [MailBeez Newsletter API](/dokumentation/configbeez/config_api/mb_newsletter_api).
- [Tutorial: Erstellen eines Newsletter Anmeldeformulars](/dokumentation/tutorials/erstellen-eines-newsletter-anmeldeformulars).
-



### Versendeprozess

Newsletter können entweder manuell oder automatisiert versendet werden. Pro Aufruf der Versende-Funktion wird die als "Stapel Grösse" konfigurierte Anzahl an Emails versendet. Somit ist die Versende-Funktion entsprechend oft aufzurufen, bis die gesamte Anzahl an Emails versendet worden ist.

**Konfigurations-Beispiel für automatisches Versenden:**

Einrichtung eines Cronjobs (z.B. alle 5 Minuten), welches ausschliesslich anstehende Newsletter versendet:

 
    wget -O - -q -t 1 <cronurl>\&module=mb_newsletter


Stapel-Grösse:

 
    100 Emails


Einfache Drosselung (Zusatzmodul):

 
    3600 Emails pro Stunde


Pro Aufruf des Versendeprozesses werden also 100 Emails versendet, etwa 1 Email pro Sekunde. Der Cronjob startet den Versendeprozess alle 5 Minuten (12x pro Stunde), somit werden 1200 Emails pro Stunde versendet.

In Abhängigkeit des zur Verfügung stehenden Mail-Servers kann der Mailversand beschleunigt werden oder muss ggf. weiter gedrosselt werden.

Durch die Drosselung und die Begrenzung der Anzahl mit Hilfe der Stapel-Grösse können Limits von Hostern bzw. den Email-Server eingehalten werden sowie das Risiko von Spam-Ratings reduziert werden.



### Empfohlene Module

Folgende Module bieten relevante Funktionen zur Optimierung des Newsletter-Versandes:

- [Einfache Drosselung](/dokumentation/mailbeez/filter_do_throttling_simple) 
- [Bouncehive Rückläufer-Verarbeitung](/dokumentation/configbeez/config_bouncehive_advanced)
- [Kundengruppen-Filter](/dokumentation/mailbeez/filter_check_group)


### geplante Weiterentwicklungen

- DONE: "Interessenten Funktion": Besucher können sich für den Newsletter eintragen. Wenn aus den Besucher Kunden werden, wird dies natürlich erkannt. Somit können leicht verschiedene Newsletter für Interessenten und Kunden versendet werden.
- weitere Email-Vorlagen
- weitere Inhaltsbereichs-Vorlagen
- MailBeez Template-Tags per Button einfügen (aktuell nur für firstname & lastname)
- automatische Erstellung von Produktdarstellungen
- personalisierte Inhalte
