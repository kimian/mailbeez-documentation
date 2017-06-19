---
# http://learn.getgrav.org/content/headers
title: MailBeez automatisch ausführen
slug: config_cron_simple
# menu: MailBeez automatisch ausführen
date: 05-07-2011
published: true
publish_date: 05-07-2011
# unpublish_date: 05-07-2011
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
    code: 'config_cron_simple'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/08/icon_cron_32.png'
    pro: 'pro'
    cert: 'true'
    price: '19 EUR'
    title_en: 'Run MailBeez Automatically'
    teaser_en: 'do some magic'
    title_de: 'MailBeez automatisch ausf&uuml;hren'
    teaser_de: 'Die einfache L&ouml;sung, um MailBeez zu automatisieren'
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

>>>>>Die Einrichtung eines "echten" Cronjobs ist die beste Methode zur Automatisierung. Dieses Modul ist eine einfach zu nutzende Alternative


**Ein einfaches, aber sehr praktisches Modul, um MailBeez automatisch auszuführen – ohne sich mit der Einrichtung eines Cronjobs befassen zu müssen**

Mit diesem einfachen Modul können Sie sich die Mühe sparen, einen Cronjob einzurichten, um MailBeez zu automatisieren. Dieses Modul nutzt den Besucher-Traffic auf Ihrem Shop, um MailBeez so oft wie gewünscht auszuführen. Für MailBeez Benutzer, die schnell das System automatisieren wollen, oder welche sich nicht mit der Einrichtung eines Cronjobs beschäftigen wollen, ist dies sehr praktisch.

**Einfach und schnell**  
 Mit Hilfe von Zeitstempel-Caches wird die zusätzliche Last auf Ihrem Server sehr gering gehalten. Durch den Einsatz von moderner AJAX Technologie wird der Besucher in Ihrem Shop nichts von der Ausführung des Modules merken: Der MailBeez Versand wird erst angestossen, nach dem die Seite vollständig geladen worden ist.

Um mit diesem Modul zu beginnen, sind neben der einfachen “Drop-In” Installation des neuen Konfigurationsmodules nur sehr einfache Anpassungen an den Shop-Dateien erforderlich.

## Konfiguration:

Die Konfiguration ist sehr einfach und selbsterklärend:

**Zeitraum zwischen den Ausführungen von MailBeez (Stunden)**  
 Geben Sie ein, wieviele Stunden zwischen der Ausführung von MailBeez vergehen sollen.


## Installation

>>>>>[plugin:content-inject](/content_blocks/hint_preintegration)


####Gambio 2.x und Modified-Shop 1.x
Öffne Datei `includes/application_bottom.php` und finde die Zeile 

`echo '</body></html>';`

davor folgenden code einfuegen:
```php
// MailBeez
if (defined('MAILBEEZ_CRON_SIMPLE_STATUS') && MAILBEEZ_CRON_SIMPLE_STATUS == 'True') {
    require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_cron_simple/includes/cron_simple_inc.php');
}
// - MailBeez
```

Um Einträge wie "/mailhive.php?cron_simple=1" in der Who-Is-Online Tabelle zu vermeiden, bitte die Datei `inc/xtc_update_whos_online.inc.php` wie folgt modifizieren:

Finde

```php
$wo_last_page_url = addslashes(getenv('REQUEST_URI'));
```

danach folgendes einfügen:

```php
// MailBeez
// avoid /mailhive.php?cron_simple=1 in who is online table
if (preg_match("/mailhive.php/", $wo_last_page_url)) {
   return false;
}
// - MailBeez
```


####Zencart
Öffne Datei  `<store-root>/includes/modules/footer.php` und vor dem schliessenden `?>` PHP-Tag folgendes einfügen:

```PHP
// MailBeez
if (defined('MAILBEEZ_CRON_SIMPLE_STATUS') && MAILBEEZ_CRON_SIMPLE_STATUS == 'True') {
    require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_cron_simple/includes/cron_simple_inc.php');
}
// - MailBeez

```
Um Einträge wie "/mailhive.php?cron_simple=1" in der Who-Is-Online Tabelle zu vermeiden, bitte die Datei `<store-root>/includes/functions/whos_online.php` wie folgt modifizieren:


Finde

```php
$wo_last_page_url = (...)');
```

danach folgendes einfügen:

```php
// MailBeez
// avoid /mailhive.php?cron_simple=1 in who is online table
if (preg_match("/mailhive.php/", $wo_last_page_url)) {
   return false;
}
// - MailBeez
``` 


####osCommerce
Öffne Datei `<store-root>/includes/footer.php` und vor dem schliessenden `?>` PHP-Tag folgendes einfügen:

```PHP
// MailBeez
if (defined('MAILBEEZ_CRON_SIMPLE_STATUS') && MAILBEEZ_CRON_SIMPLE_STATUS == 'True') {
    require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_cron_simple/includes/cron_simple_inc.php');
}
// - MailBeez

```
Um Einträge wie "/mailhive.php?cron_simple=1" in der Who-Is-Online Tabelle zu vermeiden, bitte die Datei  `<store-root>/includes/functions/whos_online.php` wie folgt modifizieren:


Finde
```php
$wo_last_page_url = getenv('REQUEST_URI');
```

danach folgendes einfügen:

```php
// MailBeez
// avoid /mailhive.php?cron_simple=1 in who is online table
if (preg_match("/mailhive.php/", $wo_last_page_url)) {
   return false;
}
// - MailBeez
``` 


