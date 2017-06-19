---
title: Shopauskunft
slug: shopauskunft
routes:
    default: /dokumentation/mailbeez/shopauskunft
date: 10-01-2011
published: true
publish_date: 10-01-2011
template: docs
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category:
        - docs
    tag:
        - ce
module:
    code: shopauskunft
    category:
        - mailbeez
    compatiblity:
        - comp_osc
        - comp_cre
        - comp_digi
        - comp_zencart
        - comp_xtc
        - comp_xtcm2        
        - comp_gambio
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/03/sa.png'
    pro: ''
    cert: ''
    price: ''
    title_en: Shopauskunft
    teaser_en: ''
    title_de: Shopauskunft
    teaser_de: 'Kunden automatisch um Bewertungen auf Shopauskunft.de bitten'
    author: MailBeez.com
author:
    name: admin
metadata:
    author: admin
---

**Bewertungs Email-Modul für Deutschlands großes Online-Shop-Bewertungsportal Shopauskunft.de.**

###Kostenlos und automatisiert mehr Bewertungen auf Shopauskunft.de

Mit diesem kostenlosen Community (CE) Modul “Shopauskunft” können Sie basierend auf einem Bestell-Status Ihre Kunden um die Abgabe einer Bewertung bei Shopauskunft.de bitten - Dabei ist konfigurierbar, welche Informationen neben der Bestell-Nr. über den individuell generierten Bewertungs-Link an Shopauskunft.de übermittelt wird.

Und natürlich können Sie leicht konfigurieren, wie viele Tage nach Bestellung diese Email versendet werden soll und wie weit in die Vergangenheit Sie Ihre Kunden um Bewertung bitten möchten. Somit können Sie sowohl laufend Ihre neue Kunden aber auch Ihre Bestandskunden aus der Vergangenheit erreichen.

Die Email ist mit Hilfe von Vorlagen [frei gestaltbar](/dokumentation/schnelleinstieg#schritt-3-gestalten-sie-die-vorlagen-nach-ihren-wunschen), so dass Sie Ihren Kunden mit Emails passend zum Shopdesign kontaktieren können.

Erfahrungsgemäss geben 5-10% der kontaktierten Kunden gerne eine Bewertung ab - und wer nicht mehr kontaktiert werden möchte, kann dies mit Klick auf den Opt-Out-Link schnell und einfach kundtun.

###Es geht noch besser mit der Pro-Version

Mit den [Profi-Tarifen](https://apps.mailbeez.de/plans) (ab 9,99Eur monatlich) von MailBeez erhalten Sie neben einer Vielzahl von - eben - Profi-Funktionen wie z.B. dem visuellen Editor für [responsive (mobil-freundliche) Emails](https://www.mailbeez.de/dokumentation/responsive-emails) auch die Profi-Version der Integration mit Shopauskunft.de, welche aus folgenden 3 Funktionsmodulen besteht:

- [Bitte um Bewertung - Profi](/dokumentation/mailbeez/shopauskunft_advanced)
- [Shopauskunft Integration](/dokumentation/configbeez/config_shopauskunft_integration)
- [Gutschein nach Bewertung](/dokumentation/mailbeez/coupon_review_shopauskunft)

-----

[<img src="https://www.shopauskunft.de/cache/res/logo.png" style="float:right">](http://www.shopauskunft.de/shops/funktionsweise)
### Shopauskunft: Das Qualitäts-Siegel für Kundenvertrauen  
SHOPAUSKUNFT verhilft Ihrem Shop mittels Kundenbewertungen zu mehr nachhaltigem Kundenvertrauen und dem damit verbundenen Umsatz.

**Ihre Vorteile**

- Steigerung der Vertrauenswürdigkeit
- Steigerung der Konversionsrate
- Steigerung des Warenkorbvolumens
- Kundenbindung
- Aktive Nutzung von Beschwerdemanagement
- Wandelung von unzufriedenen zu Wiederholungskäufern
- Nutzung der zufriedenen Kunden als Referenz und somit als Werbung für Ihren Shop
- Analyse der Stärken und Schwächen Ihres Shops aus Sicht der Kunden durch unsere aufbereiteten Daten
- Integration Ihres Shops in Deutschlands größtes Portal für Online-Shop-Bewertungen
- Suchmaschinenoptimierung mittels Verlinkung bei und durch SHOPAUSKUNFT


<div style="text-align: center; margin-bottom: 80px;">
<a href="https://www.shopauskunft.de/leistungspakete" target="_blank" class="button">Jetzt Shop registrieren</a>
</div>
  
-----

### Konfiguration des Modules:

**Aktiviere Shopauskunft Modul**  
 Möchten Sie Ihre Kunden zur Bewertung auf Shopauskunft.de auffordern?  
 Hier legen Sie fest, ob Sie das Module aktiv einsetzen wollen.

**Bestell Status**  
 Eine Bestellung muss diesen gewählten Bestell-Status haben, damit das Modul eine Bewertungsaufforderung an den Kunden verschickt.

Wenn Sie möchten, so können Sie in Ihrem System einen neuen Status z.B. “Shopbewertung OK” einführen und damit kontrollieren, welche Kunden eine Aufforderung zur Bewertung erhalten sollen.

**Anzahl Tage nach Abschluss der Bestellung**  
 Bitte geben Sie die Anzahl der Tage an, die vergangen sind, seit dem die Bestellung auf den gewählten Bestell-Status gesetzt wurde.

Stellen Sie sicher, dass nach Ablauf dieser Zeitraumes die Bestellung auch tatsächlich beim Kunden angekommen ist. Der zeitliche Abstand zwischen Lieferung und Aufforderung der Bewertung sollte aber so kurz wie möglich sein.

**Anzahl der Tage, nach denen eine Bestellung ignoriert wird**  
 Bitte geben Sie die Anzahl der Tage an, nach denen Sie Bestellungen bei der Prüfung ignorieren wollen

Hiermit legen Sie fest, wie “weit in die Vergangenheit” das Modul blicken soll. Wenn MailBeez täglich ausgeführt wird (z.B. automatisch per Cronjob) braucht diese Zahl nur etwas grösser als “Anzahl Tage nach Abschluss der Bestellung” sein.

***TIPP: **Wenn Sie gerade auf Shopauskunft.de gestartet sind, können Sie sehr einfach Ihre Kunden der z.B. letzten 6 Monate zur Bewertung auffordern. So können Sie innerhalb weniger Tage eine – abhängig von der Grösse Ihres Shops – beachtliche Anzahl von Bewertungen einsammeln.  
*

Gehen Sie so vor:

- Stellen Sie den Zeitraum auf z.B. 5 und 180 Tage und führen Sie das Modul aus.  
 Hiermit erhalten die Kunden mit Bestellungsversand in der Zeitspanne von vor 5 Tagen bis 6 Monaten genau EINE Aufforderung für die Bestellung mit der “grössten” Bestellnummer – auch wenn mehrere Bestellung im Zeitraum vorliegen.
- Jetzt den Zeitraum auf z.B. 5 und 10 stellen.  
 Somit wird fortlaufend beim jedem Durchlauf von MailBeez geprüft, ob neue Bestellung mit einem Versanddatum vor 5 bis 10 Tagen vorliegen und ggf. eine Aufforderung verschickt.  
 Voraussetzung: die Bestell-Nummern sind chronologisch – das Modul verschickt nur dann eine neue Aufforderung, falls für den Kunden eine Bestellung mit höherer Bestell-Nummber als beim letzten Aufforderungsversand vorliegt.

Das MailBeez Framework stellt sicher, dass jeder Kunde pro Bestellung nur 1 Email erhält, auch wenn das Modul mehrfach täglich ausgeführt wird.

**Shopauskunft Händler ID**  
 Bitte geben Sie Ihre individuelle Shopauskunft Händler ID ein – Sie erhalten diese ID von Shopauskunft.de

**Optional**  
 Optionale Parameter – wählen Sie, welche optionalen Parameter Sie an Shopauskunft übermitteln wollen:

- KUNDENEMAIL
- USERNAME
- BESTELLDATUM
- LIEFERDATUM
- WARENWERT
- ZAHLUNGSWEISE
- VORNAME
- NACHNAME

**Absender email Adresse**  
 Die Email-Adresse wird als Absender der Aufforderung zur Bewertung verwendet.

**Absender Name**  
 Dieser Name wird als Absender der Aufforderung zur Bewertung verwendet.

**Sortier-Reihenfolge**  
 Sortier-Reihenfolge der Module im MailBeez Admin. Von Niedrig nach Hoch. Hat keine Bedeutung für die Funktion.

**Email Vorlage**  
 Sie können die Email Ihrem Shop Design, Kundenkreis und Bedürfnissen anpassen.

Die Email wird aus einer Rahmen-Vorlage (txt und html), einer Inhalts-Vorlage (txt und html) sowie einer Betreff-Vorlage generiert.  
 Alle Vorlagen sind in Text-Dateien definiert und können leicht mit einem üblichen Editor angepasst werden.

Rahmen-Vorlagen – werden von allen MailBeez Modulen genutzt (falls nicht anders konfiguriert)

- (shop-root)/mailhive/common/templates/email\_html.tpl (html version)
- (shop-root)/mailhive/common/templates/email\_txt.tpl (txt version)

Inhalts-Vorlagen

- (shop-root)/mailhive/mailbeez/shopauskunft/email/body\_html.tpl (html version)
- (shop-root)/mailhive/mailbeez/shopauskunft/email/body\_txt.tpl (txt version)

Betreff-Vorlage

- (shop-root)/mailhive/mailbeez/shopauskunft/email/subject.tpl

