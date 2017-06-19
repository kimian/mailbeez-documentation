---
# http://learn.getgrav.org/content/headers
title: Editor und Bildgenerator
slug: config_editor
routes:
    default: /dokumentation/configbeez/config_editor
    
# menu: Visueller Editor
date: 06-04-2017
published: true
publish_date: 24-03-2014
# unpublish_date: 24-03-2014
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
    code: 'pro'
    category: [pro]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]   
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

Das Modul "Visueller Editor" wird als Bestandteil verschiedener Module, z.B. dem Newsletter-Modul und der Vorlagen-Verwaltung mitgeliefert.

Es bietet folgende Konfigurations-Möglichkeiten:


**Ausgangsverzeichnis für Bilderverwaltung**

Hier kann ein zum Shop-Hauptverzeichnis relativer Pfad angegeben werden. Der Bild-Browser wird dann ausgehenden von diesem Verzeichnis geöffnet.

Pfad-Angabe relativ zum Shop-Hauptverzeichnis  
 Bei leerem Pfad: Alle Unterverzeichnis im Shop sind zugänglich


**Ausgangsverzeichnis für Bild-Cache**

Hier kann ein zum Shop-Hauptverzeichnis relativer Pfad angegeben werden. Der MailBeez Bildgenerator schreibt Bild-Dateien in dieses Verzeichnis. Dieser Cache kann vollständig regeniert werden.
 
Bei Änderung des Cache-Pfades wird der Cache automatisch umgeschrieben, allerdings sollte der alte Pfad mit der darin enthaltenen .htaccess Datei erhalten bleiben, um das Generieren von Bildern in früher versendeten Emails zu ermöglichen.


**Mobil-Editor Breitenangaben**

Als Unterstützung für die Bearbeitung von responsive E-Mails kann der Editor in verschiedene Breiten eingerichtet werden.

Bitte diese Angabe nur ändern wenn dies wirklich erforderlich ist

**Mobil-Editor Breite 1**: Breite für Ansicht 1, z.B. 320px

**Mobil-Editor Breite 2**: Breite für Ansicht 2, z.B. 480px

**Mobil-Editor Breite 3**: Breite für Ansicht 3, z.B. 600px