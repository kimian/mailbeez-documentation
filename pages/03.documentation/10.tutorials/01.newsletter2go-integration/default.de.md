---
# http://learn.getgrav.org/content/headers
title: Newsletter2Go Integration
slug: newsletter2go-integration-mailbeez
published: true
template: tutorial

visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category: [docs]
    tag: [ce]
---

[TOC]

## Funktionsumfang
MailBeez enthält eine leistungsfähige Integration mit Newsletter2Go, welche dem Shopbetreiber alle Freiheiten für ein professionelles Email Marketing eröffnen.



###Aus Sicht von MailBeez
Emails werden in MailBeez erstellt, generiert und dann zum Versand an Newsletter2Go übergeben:

- **Email Versand**  
  alle von MailBeez generierten Emails werden über eine Schnittstelle zum sofortigen Versand an Newsletter2Go übergeben. Hierdurch werden bestmögliche Zustellraten erzielt.
- **Bounce-Handling**  
  Rückläufer aufgrund ungültiger Email-Adressen werden vom Newsletter2Go-System verarbeitet und über ein Schnittstelle an MailBeez zurückgemeldet, so dass diese Email-Adressen in Zukunft ausgeschlossen werden.
  
  
###Aus Sicht von Newsletter2Go
Alle Email-Adressen aus dem Shop können nach Newsletter2Go importiert werden. Dort werden Newsletter erstellt und versendet:

- **Empfänger-Import**  
  Die Email-Adressen aller Kunden im Shop werden an Newsletter2Go übergeben
- **Abmeldungen**  
  Klick auf Abmelde-Links in Newsletter2Go Emails werden an MailBeez zurückgemeldet
- **Produkt-Information**  
  Der Produkt-Assistent im Newsletter2Go Editor kann alle Produkt-Informationen aus dem Shop einlesen.


##Mögliche Szenarien

1. **Newsletter in Newsletter2Go erstellen und versenden**  
  Hierbei nutzt Newsletter2Go die Schnittstelle zum Empfänger-Import & Einlesen von Produkt-Informationen aus dem Shop-System heraus.
1. **Automatik-Emails und Newsletter in MailBeez erstellen und über Newsletter2Go versenden**  
  Hierbei übergibt MailBeez die generierten Emails an Newsletter2Go zum Versand mit bestmöglichen Zustellraten. Ungültige Email-Adressen werden in MailBeez markiert.
1. **Kombination aus 1. & 2.**  
   Traditionelle Newsletter werden in Newsletter2Go erstellt und versendet, während MailBeez z.B. Emails zur Bitte um Produktbewertung generiert.

##Einrichtung der Integration

### 1. MailBeez installieren
Fall Sie noch nicht MailBeez installiert haben, bitte zunächst das kostenlose Grundsystem installieren.

Folgen Sie hierzu der Installationsanleitung für Ihr Shopsystem.

Die mit <b class='label label-integrated'></b> markierten Shop-Systeme haben **MailBeez bereits vorintegriert**, hier ist die Grundinstallation mit wenigen Klicks erledigt.

[ui-accordion independent=true open=none]
[ui-accordion-item title="<b class='label label-integrated'></b> Gambio 3.x"]
Dank der Vorintegration von MailBeez in Gambio 3.x kann das kostenlose Grundsystem mit wenigen Klicks installiert werden. 

Hierzu bitte unter `Module > Module-Center` die Integration `MailBeez` aktivieren und dann über den neuen Menüpunkt `MailBeez` das Grundsystem installieren.

[/ui-accordion-item]
[ui-accordion-item title="<b class='label label-integrated'></b> Gambio 2.5+"]

Dank der Vorintegration von MailBeez in Gambio 2.5+ kann das kostenlose Grundsystem mit wenigen Klicks installiert werden. 

Hierzu bitte unter `Module > Module-Center` die Integration `MailBeez` aktivieren und dann über den neuen Menüpunkt `MailBeez` das Grundsystem installieren.

[/ui-accordion-item]
[ui-accordion-item title="<b class='label label-integrated'></b> Gambio 2.3+"]
Dank der Vorintegration von MailBeez in Gambio 2.3+ kann das kostenlose Grundsystem mit wenigen Klicks installiert werden. 

Hierzu bitte in der Gambio Administration auf den Menüpunkt `MailBeez` klicken, um das Grundsystem zu installieren

[/ui-accordion-item]
[ui-accordion-item title="<b class='label label-integrated'></b> Gambiocloud.de"]
Dank der Vorintegration von MailBeez in [Gambiocloud.de](https://gambiocloud.de) kann das kostenlose Grundsystem mit wenigen Klicks installiert werden. 

Hierzu bitte in der Gambio Administration auf den Menüpunkt `MailBeez` klicken, um das Grundsystem zu installieren

[/ui-accordion-item]
[ui-accordion-item title="Gambio 2.x"]
Bitte der Anleitung zur [Installation von MailBeez auf Gambio 2.x](/dokumentation/installation/basic-installation-gambio-gx-2) folgen.

[/ui-accordion-item]
[ui-accordion-item title="Gambio 1.x"]
Bitte der Anleitung zur [Installation von MailBeez auf Gambio 1.x](/dokumentation/installation/basic-installation-gambio) folgen.

[/ui-accordion-item]
[ui-accordion-item title="Modified-Shop 2.x"]
Bitte der Anleitung zur [Installation von MailBeez auf Modified-Shop 2.x](/dokumentation/installation/basic-installation-modified-shop-2) mittels des passenden updatesicheren Integrations-Pakets folgen.

[/ui-accordion-item]
[ui-accordion-item title="Modified-Shop 1.x"]
Bitte der Anleitung zur [Installation von MailBeez auf Modified-Shop 1.x](/dokumentation/installation/basic-installation-modified-shop) folgen.

[/ui-accordion-item]
[ui-accordion-item title="<b class='label label-integrated'></b> Zen-Cart-pro.at"]
Dank der Vorintegration von MailBeez in Zen-Cart-pro.at kann das kostenlose Grundsystem unter `Admin > Tools > MailBeez` per Button-Klick installiert werden.

[/ui-accordion-item]
[ui-accordion-item title="ZenCart"]
Bitte der Anleitung zur [Installation von MailBeez auf ZenCart](/dokumentation/installation/basic-installation-zen-cart-1-5-x) folgen.

[/ui-accordion-item]
[ui-accordion-item title="osCommerce 2.3.x"]
Bitte der Anleitung zur [Installation von MailBeez auf osCommerce 2.3+](/dokumentation/installation/oscommerce-2-3-x) folgen.

[/ui-accordion-item]
[ui-accordion-item title="osCommerce 2.2"]
Bitte der Anleitung zur [Installation von MailBeez auf osCommerce 2.2](/dokumentation/installation/basic-installation-oscommerce) folgen.

[/ui-accordion-item]
[/ui-accordion]

### 2. Verbindung herstellen
Im MailBeez System unter `MailBeez > Konfiguration > Email System` den Button zur Verbindung mit Newsletter2Go anklicken.

Falls Sie bereits ein Konto bei Newsletter2Go haben, bitte einloggen und den Zugriff zulassen.

Falls Sie noch nicht Newsletter2Go nutzen, bitte in dem Dialog die Registrierung vornehmen.

>>>>> Stand April 2017: Falls Sie den Fehler `Bad Request (field entrypoint must not be empty)` erhalten, bitte das Fenster schliessen und nochmals im MailBeez-System den Button zur Verbindung mit Newsletter2Go anklicken

### 3. Fertig

Herzlichen Glückwunsch, die Integration von Newsletter2Go und MailBeez ist abgeschlossen!

Das Newsletter2Go System zeigt Ihnen jetzt den Status der Integration an. Wechseln Sie zurück ins MailBeez System, um dort nach erneutem Laden der Seite ebenfalls den Status der Integration zu prüfen.

Falls wider Erwarten Fehler aufgetreten sind, wenden Sie sich bitte an den Support von Newsletter2Go.
