---
# http://learn.getgrav.org/content/headers
title: Gutschein Generator
slug: config_coupon_engine
routes:
    default: /dokumentation/configbeez/config_coupon_engine
    aliases:
        - /dokumentation/configbeez/gutschein-generator
        
# menu: Gutschein Generator
date: 10-04-2012
published: true
publish_date: 10-04-2012
# unpublish_date: 10-04-2012
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
    code: 'pro'
    category: [pro]
    compatiblity: [comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]   
    pro: 'pro'

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

Eine Übersicht der unterstützen Shopsysteme findet sich auf [MailBeez Kompatibilität](/dokumentation/kompatibilitat/).


Der MailBeez Gutschein-Generator wird als Untermodul von allen MailBeez Modulen verwendet, welche personalisierte Gutscheine generieren und versenden.


###Vorteile von personalisierten Gutscheinen
Im Vergleich zu herkömmlichen, gemeinsamen Gutschein-Codes (z.B. "GEBURTSTAG") haben personalisierte Gutschein folgende Vorteile:

- **Kein ungewünschter viraler Effekt**: Sie können konfigurieren, wie oft der Gutschein verwendet werden kann
- **Dringlichkeit durch Verfalls-Datum**: Jeder generierte Gutschein bekommt eine Gültigkeit von z.B. 14 Tagen ab Versende-Datum. Damit wird das Gefühl der Dringlichkeit erzeugt und es werden mehr Gutscheine (=mehr Bestellungen) verwendet. Zudem kann mit Hilfe des Modules [Gutschein-Ablauf Erinnerung](/dokumentation/mailbeez/coupon_expire) an den Verfall des Gutscheines erinnert werden - was wiederum zur Verbesserung der Konversion beiträgt
- **Nachvollziehbarkeit**: Das System speichert, welcher Kunden welchen Gutschein-Code in welcher Email bekommen hat. Somit können Sie nachvollziehen, welche Emails und Gutscheine die gewünschte Wirkung zeigen.



###Vorlagen-Gutscheine

Der Gutschein-Generator generiert personalisierte Gutscheine basierend auf **Vorlagen-Gutscheinen**, welche im jeweiligen Modul zugeordnet werden. Ein **Vorlagen-Gutschein** ist ein "normaler" Gutschein, kennzeichnet sich aber dadurch, dass der Gutschein-**CODE** mit der Zeichenfolgen `template_` beginnen muss.

>>>>>>Lassen Sie sich den Ablauf direkt in Ihrem Shop-System von dem Lehrgang zum Anlegen von Vorlagen-Gutscheinen zeigen
 
**Beispiel "[Geburtstags-Email mit Gutschein](/dokumentation/mailbeez/coupon_birthday)"**:

Zunächst einen Gutschein mit

CODE = `template_geburtstag`

und den gewünschten Werten (z.B. 10% Rabatt bei 20Eur Mindest-Bestellwert) anlegen - das Gültigkeitsdatum hat keine Bedeutung.

Im Modul [Geburtstags-Email mit Gutschein](/dokumentation/mailbeez/coupon_birthday) dann diesen Vorlagen-Gutschein konfigurieren (speichern nicht vergessen).

Bei der Generierung von Geburtstags-Emails wird dann für jeden Empfänger ein personaliserter Gutschein basierend auf dem Vorlagen-Gutschein generiert. Dabei wird ein zufälliger Gutschein-Code angelegt und das Ablauf-Datum entsprechend der Konfiguration gesetzt (z.B. 14 Tage ab Datum des Email-Versandes).

Sie können die Konfiguration mit Hilfe einer Simulation testen: Im Simulations-Modus das Modul ausführen. Dabei werden "echte" Emails mit "echten" Gutscheinen generiert, allerdings nicht an den Kunden sondern an die hinterlegte Email-Adresse gesendet. Sie können dann den Wert des Gutscheines prüfen und diesen auch bei einer Test-Bestellung verwenden.




###Hilfs-Funktionen
 
In diesem Modul finden Sie einer Reihe von Hilfs-Funktionen zur Verwaltung von Gutscheinen:

**Gutschein Suche**: Finden Sie einen Gutschein zum bearbeiten, diese Funktion steht auch als [Dashboard-Widget](/dokumentation/dashboardbeez/dashboard_coupon_admin) zur Verfügung.

**Simulations Gutscheine löschen**: Beim Ausführen von Simulationen werden "echte" Gutschein generiert. Mit dem Button können Sie leicht alle diese Gutscheine wieder aus dem System entfernen

**Verfallene Gutscheine löschen**: Als "Aufräum-Funktion" können Sie hier alte, verfallene Gutscheine aus der Datenbank löschen.

**Zuordnung reparieren**: In einigen Fällen fehlt die Zuordnung von Gutscheinen zur den Emails, in denen der Gutschein versendet worden ist. Diese Zuordnung können Sie hiermit reparieren.


>>>>>**Bitte beachten**: Je Modul kann die Gutschein-Code Länge konfiguriert werden. Lange Codes (z.B. 8 oder 10 Zeichen) lassen sich sehr schnell generieren. Bei kurzen Codes und bereits vielen vorhandenen Gutscheinen muss das System ggf. "lange probieren" bis ein freier Code gefunden werden kann. Dies kann zu einem Abbruch (Time-Out) des Versende-Prozesses führen.

## osCommerce Gutschein System Unterstützung

Als “Mutter aller eCommerce Systeme" ist osCommerce als sauberes Kern-System angelegt und besitzt kein Gutschein System.  
 Wahrscheinlich haben Sie bereits ein Gutschein System in osCommerce installiert. MailBeez unterstützt eine Reihe von Gutschein-Systemen wie nachfolgend aufgelistet. Die Tabellen-Namen helfen, das installierte System zu identifizieren.

Falls Sie noch kein Gutschein-System installiert haben, sollten Sie ein CCGV basiertes addon wählen.

#### CCGV basierte Gutschein Systeme

Es gibt eine Reihe von Gutschein Systemen, welche vom “CCGV” Addon abstammen. 

wie z.B.:

- [http://addons.oscommerce.com/info/4135](http://addons.oscommerce.com/info/4135)  
- [http://addons.oscommerce.com/info/282](http://addons.oscommerce.com/info/282)  
- [http://addons.oscommerce.com/info/8002](http://addons.oscommerce.com/info/8002)  
- [http://addons.oscommerce.com/info/9020](http://addons.oscommerce.com/info/9020) (osc 2.3.3.4)

Die verschiedenen Addons nutzen nahezu die gleiche Tabellen-Struktur.

**Tabellen**:

Wenn Sie ein CCGV basiertes Gutschein System nutzen, sollten Sie folgende Tabellen in der Tabellen-Definition finden:

```
TABLE_COUPONS
TABLE_COUPONS_DESCRIPTION
TABLE_COUPON_EMAIL_TRACK
TABLE_COUPON_REDEEM_TRACK
TABLE_COUPON_RESTRICT
 
```

#### Discount Coupon Codes

[http://addons.oscommerce.com/info/4269](http://addons.oscommerce.com/info/4269)

**Tabellen**:

Wenn Sie ein DCC basiertes Gutschein System nutzen, sollten Sie folgende Tabellen in der Tabellen-Definition finden:

```
TABLE_DISCOUNT_COUPONS
TABLE_DISCOUNT_COUPONS_TO_ORDERS
TABLE_DISCOUNT_COUPONS_TO_CATEGORIES
TABLE_DISCOUNT_COUPONS_TO_PRODUCTS
TABLE_DISCOUNT_COUPONS_TO_MANUFACTURERS
TABLE_DISCOUNT_COUPONS_TO_CUSTOMERS
TABLE_DISCOUNT_COUPONS_TO_ZONES

```

#### Discount Coupons by high-quality-php-coding.com

[http://high-quality-php-coding.com](http://high-quality-php-coding.com)

**Tabellen**:

Wenn Sie ein DC basiertes Gutschein System nutzen, sollten Sie folgende Tabellen in der Tabellen-Definition finden:  

```
TABLE_DISCOUNT_CODES
TABLE_CUSTOMERS_TO_DISCOUNT_CODES

```


Falls Sie den Fork **Discount Codes BS** 
<http://addons.oscommerce.com/info/9460> nutzen, ist folgendes zu beachten:

Dieses Modul nutzt nicht die üblichen Konstanten, um Tabellen-Namen zu definieren. Daher bitte eine neue Datei

`/mailhive/common/local/dc.php` 

mit folgendem Inhalt anlegen:

```php
<?php
define('TABLE_DISCOUNT_CODES', 'discount_codes');
define('TABLE_CUSTOMERS_TO_DISCOUNT_CODES', 'customers_to_discount_codes');
define('FILENAME_DISCOUNT_CODES', 'discount_codes.php');
```

Hierdurch werden die fehlenden Konstanten definiert.
