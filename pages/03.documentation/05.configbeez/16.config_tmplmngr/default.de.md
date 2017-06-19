---
# http://learn.getgrav.org/content/headers
title: Responsive Template Manager
slug: config_tmplmngr
routes:
    aliases:
        - /dokumentation/configbeez/config_tmplmngr
# menu: Responsive Vorlagen Verwaltung
date: 30-06-2011
published: true
publish_date: 30-06-2011
# unpublish_date: 30-06-2011
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
    code: 'config_tmplmngr'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2011/08/icon_321.png'
    pro: 'pro'
    cert: 'true'
    price: '159 EUR'
    title_en: 'Responsive Template Manager'
    teaser_en: 'edit your campaign templates from you MailBeez admin and send responsive Emails'
    title_de: 'Responsive Vorlagen-Verwaltung'
    teaser_de: 'Bearbeite die MailBeez Vorlagen direkt in der Admin und versende responsive Emails'
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

Mit dem visuellen Vorlagen Manager mit Unterstützung für responsive Emails können Sie schnell und einfach direkt aus dem MailBeez System heraus alle Email-Vorlagen bearbeiten und testen!

Der Vorlagen Manager funktioniert mit allen offiziellen (Pro und CE) MailBeez Modulen aber auch mit Eigen-Entwicklungen, welche das MailBeez Vorlagen System nutzen.

Sie brauchen also nie wieder Vorlagen Dateien per FTP downloaden, lokal abspeichern, bearbeiten und dann wieder hochladen um diese dann zu testen.


## Funktionen

- **Komfortabler visueller Editor** macht HTML Kenntnisse überflüssig
- **Mobil-Vorschau** mit verschiedenen Schirmgrössen (z.B. iPhone, iPad)
- Vorlagen **direkt im Layout** bearbeiten und testen.
- **Eigene Vorlagen speichern** und ggf. wieder herstellen
- **Wiederherstellung der Standard-Vorlagen** falls es Probleme gab
- **Kompatibel** mit der Unterstützung für [Mehrsprachigkeit](/dokumentation/configbeez/config_tmplmngr_lng/ "Multilanguage Template Manager")!
- **Nerd-Mode** mit Syntax highlighting gibt alle Freiheiten für fortgeschrittene Anwender
- **Einfachstes updaten von MailBeez** da alle Vorlagen in der Datenbank gespeichert werden
- **Automatischer Import** der Modul -.tpl Dateien.

Der visuelle Editor bietet eine Reihe direkt zugänglicher Funktionen, um die HTML & TXT Version der Email zu bearbeiten und zu testen.

>>>>>Standardmässig wird automatisch eine Text-Version aus der HTML-Vorlage generiert. Eigene in den Modulen definierte TXT-Inhalte werden nur übernommen, wenn auch eine eigene TXT-Hauptvorlage erstellt worden ist.