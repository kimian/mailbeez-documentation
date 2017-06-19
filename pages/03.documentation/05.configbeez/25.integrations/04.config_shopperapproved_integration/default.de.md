---
# http://learn.getgrav.org/content/headers
title: ShopperApproved Integration Suite
slug: config_shopperapproved_integration
routes:
    default: /dokumentation/configbeez/config_shopperapproved_integration
# menu: ShopperApproved Integration Suite
date: 03-05-2011
published: true
publish_date: 03-05-2011
# unpublish_date: 03-05-2011
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
    code: 'config_shopperapproved_integration'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/03/top_64.png'
    pro: 'pro'
    cert: 'true'
    price: '159 EUR'
    title_en: 'ShopperApproved Integration Suite'
    teaser_en: 'Integrate your valuable ShopperApproved Ratings in MailBeez Campaigs and your Storefront (SEO)'
    title_de: 'ShopperApproved Integration Suite'
    teaser_de: 'Integrieren Sie Ihre wertvollen Bewertungen in MailBeez Kampagnen und den Shop (SEO)'
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

**Händler mit entsprechendem ShopperApproved-Vertrag können jetzt die wertvollen Bewertungen - Shop- & Produkt-Bewertungen - noch wirksamer im Onlineshop und sogar in MailBeez Email Kampagnen einsetzen.**

Wie vielen Online Händler haben Sie sich für ShopperApproved entschieden, um neuen und auch bestehenden Kunden Sicherheit und Vertrauen zu demonstrieren.

Mit der MailBeez ShopperApproved Integration Suite haben Sie jetzt mehr Flexibilität um positive Bewertungen besonders wirkungsvoll im Shop und sogar in von MailBeez generierten Email zu platzieren.

Basierend auf 100% anpassbaren Vorlagen können Sie z.B. 5-Sterne Bewertungen an besonders kritischen Stellen einsetzten, z.B. auf der Seite zur Kontoeröffnung oder auch beim Checkout. Hier hilft eine zufällige, positive Bewertung letzte Zweifel aus den Weg zu räumen.

Da die Bewertungen direkt in das HTML des Shops eingefügt werden, haben diesen einen positiven SEO Effekt – alle Bewertungen können somit von Suchmaschinen erfasst werden.

Durch die nahtlose Integration mit den MailBeez Email Kampagnen können Sie auf einfachste Weise z.B. in Emails zur [Kunden Rückgewinnung](/dokumentation/mailbeez/winback_advanced/ "Winback Advanced") oder auch beim [Kontakt von Kunden ohne Bestellung](/dokumentation/mailbeez/nopurchase_advanced/ "No Purchase Advanced") Ihre positive Bewertungen herausstellen und somit das Kaufverhalten positiv beeinflussen.

Die wichtigsten Funktionen im Überblick:

- Caching des ShopperApproved Bewertunges-Feed für schnelle Ladezeiten
- Vorlagenbasierte Darstellung der Bewertungen
- Unbeschränkte Anzahl von Vorlagen zur Integration an verschiedenen Stellen, eine Vorlage für Email Integration.
- Auswahl der anzuzeigenden Bewertungen, z.B. “Mindestens 4 Sterne”
- Zufällige oder chronologische Auflistung der Bewertungen
- Einfachste “Drop-In” Installation
- Einfachster Funktionsaufruf für die Einbindung der Ausgabe in den Onlineshop


### Installation

Modul installieren und Konfigurieren – wie im Adminbereich des Moduls beschrieben.  


### Integration der Bewertungen in den Shop

Eigene Vorlagen können im Verzeichnis 
`/mailhive/configbeez/config_shopperapproved_integration/templates/` 
basierend auf den dort vorhandenen Grundvorlagen angelegt werden.


**xt:Commerce, xtc-modified, Gambio GX**  
Um z.B. die ShopperApproved Bewertungen in beliebigen Stellen im Shop-Frontend darstellen zu können, bitte folgende Schritte durchführen:

In der Datei `templates/<dein template>/source/boxes.php`

z.B. ganz am Ende vor dem ?> folgendes einfügen:

```
// MailBeez ShopperApproved Integration Suite
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_shopperapproved_integration/classes/mh_shopperapproved_integration.php');
$widget = new mh_shopperapproved_integration();

// generate output ($template, $items_limit, $min_stars, $random, $min_chars_comment)
$smarty->assign('sabox_reviewpage', $widget->output('default_storefront.html.tpl', 20, 4, true, 10));
$smarty->assign('sabox_single', $widget->output('default_storefront.html.tpl', 20, 4, true, 10) );
// - MailBeez ShopperApproved Integration Suite
```


Hiermit werden die Template-Variablen

```
{$sabox_reviewpage}
{$sabox_single}
```

angelegt und basierend auf der Vorlagen `default_storefront.html.tpl` mit formatierten Bewertungen gefüllt.

Um z.B. eine einzelne Bewertung auf der “Kontakt”-Seite darzustellen, folgende Änderung vornehmen:

In der Datei `templates/<dein template>/module/contact_us.html` füge z.B. am Ende ein:
```
{$sabox_single}
```
 

**osCommerce, ZenCart, CRE Loaded**  
Um z.B. die ShopperApproved Bewertungen in der “Kontakt” Seite des Shopsystems einzubinden, bitte folgenden Code in die seite “contact_us.php” einfügen:

```
//include class
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_shopperapproved_integration/classes/mh_shopperapproved_integration.php');
$widget = new mh_shopperapproved_integration();

// generate output ($template, $items_limit, $min_stars, $random, $min_chars_comment)
echo $widget->output('default_storefront.html.tpl', 20, 4, true, 10);

```



Mit dem Anlegen und Anpassen verschiedener eigener Vorlagen, z.B. `my_shoppingcart.html.tpl` für eine zufällige Bewertung im Einkaufwagen – können die ShopperApproved Bewertungen sehr flexibel eingebunden werden.

**Einbindung der ShopperApproved Bewertungen in MailBeez Kampagnen:**  
Mit dem leichten Einfügen eines einfachen Platzhalters in MailBeez Vorlagen können ShopperApproved Bewertungen in alle oder ausgewählten von MailBeez generierten Emails angezeigt werden. Mehr hierzu auf der Seite zum Hilfsmodule [ShopperApproved Bewertungen in Emails](/dokumentation/filterbeez/filter_add_shopperapproved/ "ShopperApproved Bewertungen in Emails").

Mit Hilfe der ShopperApproved Integration Suite wird so z.B. das beliebte und effektive Modul “Kunden ohne Kauf” (Nopurchase) mit positiven Kundenstimmen aufgewerten. Dies passiert voll automatisch und kann mit einem einfachen Platzhalter eingebunden werden – natürlich in jedem MailBeez Modul und in jeder MailBeez Email Kampagne.
