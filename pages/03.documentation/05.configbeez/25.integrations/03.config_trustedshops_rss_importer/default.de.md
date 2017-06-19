---
# http://learn.getgrav.org/content/headers
title: Trustedshops Integration Suite
slug: config_trustedshops_rss_importer
routes:
    default: /dokumentation/configbeez/config_trustedshops_rss_importer
# menu: Trustedshops Integration Suite
date: 26-10-2011
published: true
publish_date: 26-10-2011
# unpublish_date: 26-10-2011
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
    code: 'config_trustedshops_rss_importer'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/10/icon_328.png'
    pro: 'pro'
    cert: 'true'
    price: '159 EUR'
    title_en: 'Trustedshops Integration Suite'
    teaser_en: 'Integrate your valuable Trustpilot Ratings in MailBeez Campaigs and your Storefront (SEO)'
    title_de: 'Trustedshops Integration Suite'
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

**Händler mit entsprechendem Trustedshops-Vertrag können jetzt die wertvollen Bewertungen noch wirksamer im Onlineshop und sogar in MailBeez Email Kampagnen einsetzen.**

Wie vielen Online Händler haben Sie sich für Trustedshops entschieden, um neuen und auch bestehenden Kunden Sicherheit und Vertrauen zu demonstrieren.

Mit der MailBeez Trustedshops Integration Suite haben Sie jetzt mehr Flexibilität um positive Bewertungen besonders wirkungsvoll im Shop und sogar in von MailBeez generierten Email zu platzieren.

Basierend auf 100% anpassbaren Vorlagen können Sie z.B. 5-Sterne Bewertungen an besonders kritischen Stellen einsetzten, z.B. auf der Seite zur Kontoeröffnung oder auch beim Checkout. Hier hilft eine zufällige, positive Bewertung letzte Zweifel aus den Weg zu räumen.

Da die Bewertungen direkt in das HTML des Shops eingefügt werden, haben diesen einen positiven SEO Effekt – alle Bewertungen können somit von Suchmaschinen erfasst werden.

Durch die nahtlose Integration mit den MailBeez Email Kampagnen können Sie auf einfachste Weise z.B. in Emails zur [Kunden Rückgewinnung](/dokumentation/mailbeez/winback_advanced/ "Winback Advanced") oder auch beim [Kontakt von Kunden ohne Bestellung](/dokumentation/mailbeez/nopurchase_advanced/ "No Purchase Advanced") Ihre positive Bewertungen herausstellen und somit das Kaufverhalten positiv beeinflussen.

Die wichtigsten Funktionen im Überblick:
- Caching des Trustedshops Bewertungs Feed für schnelle Ladezeiten
- Vorlagenbasierte Darstellung der Bewertungen
- Unbeschränkte Anzahl von Vorlagen zur Integration an verschiedenen Stellen, eine Vorlage für Email Integration.
- Auswahl der anzuzeigenden Bewertungen, z.B. “Mindestens 4 Sterne”
- Zufällige oder chronologische Auflistung der Bewertungen
- Einfachste “Drop-In” installation
- Einfachster Funktionsaufruf für die Einbindung der Ausgabe in den Onlineshop

und natürlich:

- Handhabung der Zusatzdaten des Trustedshops Bewertungs Feeds – zeitraubende Anpassungen entfallen damit

### Installation

Modul installieren und Konfigurieren – den RSS Feed konfigurieren wie im Adminbereich des Moduls beschrieben. 
  Mit der integrierten Test-Funktion kann der RSS Feed komfortabel getestet werden.

### Integration der Bewertungen in den Shop:


**Gambio GX**

Die Einbindung erfolgt mit einem overloads-Modul inkl. Beispiel für ein Custom-Modul, welche im Paket enthalten sind. 
  Dann können im Template an beliebiger Stelle per smarty-Tag die Bewertungen ausgegeben werden.


**xt:Commerce, xtc-modified**

Um z.B. die Trustedshops Bewertungen in beliebigen Stellen im Shop-Frontend darstellen zu können, bitte folgende Schritte durchführen:

In der Datei `templates/source/boxes.php` z.B. ganz am Ende vor dem ?> folgendes einfügen:

```
// MailBeez Trustedshops Integration Suite
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_trustedshops_rss_importer/classes/trustedshops_import_rss.php');
// create new instance
$rss = new trustedshops_import_rss();
// generate output (template, number of ratings, min stars, shuffle)
$smarty->assign('tsbox_reviewpage', $rss->output_rss('rss_reviewpage.tpl', 25, 4, 'False') );
$smarty->assign('tsbox_single', $rss->output_rss('rss_reviewpage.tpl', 1, 4, 'True') );
// - MailBeez Trustedshops Integration Suite

```

Hiermit werden die Template-Variablen

```
{$tsbox_reviewpage}
{$tsbox_single}
```

angelegt und basierend auf der Vorlagen `rss_reviewpage.tpl mit formatierten Bewertungen gefüllt.

Um z.B. eine einzelne Bewertung auf der “Kontakt”-Seite darzustellen, folgende Änderung vornehmen:

In der Datei `templates/module/contact_us.html` füge z.B. am Ende ein:

```
{$tsbox_single}
```


Die mitgelieferte DIV/CSS basierende Vorlagee “rss\_reviewpage.tpl” lieferte folgende Ausgabe:

![](Screen_trustedshops_rss_contact_us_gbo.png "trustedshops_rss_email")

Trustedshops Bewertung in der Kontakt-Seite

Mit dem Anlegen und Anpassen verschiedener eigener Vorlagen, z.B. `rss_shoppingcart.tpl` für eine zufällige Bewertung im Einkaufswagen – können die Trustedshops Bewertungen sehr flexibel eingebunden werden.



**osCommerce, ZenCart, CRE Loaded**

Um z.B. die Trustedshops Bewertungen in der “Kontakt” Seite des Shopsystems einzubinden, bitte folgenden Code in die seite “contact\_us.php” einfügen:

```
//include class
require_once(DIR_FS_CATALOG . 'mailhive/configbeez/config_trustedshops_rss_importer/classes/trustedshops_import_rss.php');
// create new instance
$rss = new trustedshops_import_rss();
// generate output (template, number of ratings, min stars, shuffle)
echo $rss->output_rss('rss_reviewpage.tpl', 7, 4, 'True');
```

Die mitgelieferte DIV/CSS basierende Vorlage `rss_reviewpage.tpl` liefert folgende Ausgabe:

![](Screen_trustedshops_rss_contact_us_gbo.png "trustedshops_rss_email")
 

Mit dem Anlegen und Anpassen verschiedener eigener Vorlagen, z.B. `rss_shoppingcart.tpl` für eine zufällige Bewertung im Einkaufswagen – können die Trustedshops Bewertungen sehr flexibel eingebunden werden.

###Einbindung der Trustedshops Bewertungen in MailBeez Kampagnen  
 Mit dem Einfügen eines einfachen Platzhalters in MailBeez Vorlagen können Trustedshops Bewertungen leicht in alle oder ausgewählten von MailBeez generierten Emails angezeigt werden.

![](Screen_trustedshops_rss_email.png "trustedshops_rss_email")

Den Platzhalter finden Sie im gleichnamigen Modul unter "Filter & Hilfsmodule"