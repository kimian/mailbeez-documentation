---
# http://learn.getgrav.org/content/headers
title: Anpassung der Hauptvorlage
slug: anpassung-der-hauptvorlage
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
    tag: [pro]
---

[TOC]

## Aufbau der Vorlagen

Alle von MailBeez generierten Emails werden aus der gemeinsamen Haupt-Vorlage und Modul-Vorlagen zusammengesetzt. In diesem Tutorial wird beschrieben, wie die gemeinsame Haupt-Vorlage ("Briefpapier") bearbeitet werden kann.

<div style="padding: 30px; border: 1px solid #c0c0c0; background-color: #E7F2FA; width: 100%; max-width: 600px; margin:auto" markdown="1">
Gemeinsame Hauptvorlage
<div style="padding: 30px; border: 1px solid #c0c0c0; background-color: #FFFFFF;" markdown="1">[Modul-spezifische Inhalts-Vorlage](/dokumentation/tutorials/anpassung-der-modul-vorlagen)
Platzhalter `{$body}`
<div style="padding: 30px; border: 1px solid #c0c0c0;" markdown="1">Produktlisten-Vorlage<br>
Platzhalter z.B. `{$list_engine.productlist}`
</div>
</div>
</div>

## Gemeinsame Hauptvorlage zum Bearbeiten öffnen
Alle Profi-Module enthalten den visuellen Editor, mit dem die gemeinsame Hauptvorlage (also das "Briefpapier" in welches die Module ihre Email-Texte einfügen) komfortabel und visuelle bearbeitet werden können.

Die Hauptvorlage kann unter 

`MailBeez > Konfiguration > Template Verwaltung > Gemeinsame Hauptvorlage bearbeiten` 

im visuellen Editor zur Bearbeitung geöffnet werden.


## Laden einer Vorlage

Auf der rechten Seite kann mit Hilfe des Buttons `Layout-Vorlage wählen` eine Vorlage geladen werden. Wählen Sie dort "**responsive Email**" aus, um die aktuellste Version der mobilfreundlichen Hauptvorlage zu laden.

## Anpassung der Kopf-Bilder

Der Button `Styling bearbeiten` öffnet die Konfiguration der Layout-Einstellungen. Da [responsive (Mobil-freundliche) Emails](/dokumentation/responsive-emails) zwei verschiedene Bilder für die Desktop-Version und die Mobil-Version nutzen, können in den Layout-Einstellungen auch zwei Bilder konfiguriert werden. Alle Angaben mit `@480` kennzeichnen hier die Einträge für die Mobil-Version unter 480px Schirmbreite.


## Anpassung der Firmen-Angaben im Fussbereich

Die Firmen-Angaben im Fussbereich können frei bearbeitet werden, einfach auf das entsprechende Element klicken und dort die gewünschten Änderungen vornehmen.

## Anpassung der Menü-Einträge

Die oberen Menü-Einträge können frei bearbeitet werden, einfach auf das entsprechende Element klicken und dort die gewünschten Änderungen vornehmen.


## Testen der Vorlage

Im visuellen Editor finden Sie oben links Buttons wie "320px", "480px" - hiermit können Sie jederzeit beim bearbeiten testen, wie die Vorlage auf mobilen Endgeräten umgebrochen wird. Sollte sich die Vorlage nach einigen Anpassungen nicht sauber auf z.B. 320px umbrechen, dann gibt es ein Element (z.B. ein Bild) welches eine feste Breiten-Angabe hat und somit nicht angepasst werden kann. In diesem Fall als Breite "100%" angeben. Auch lange URLs können Probleme machen, ggf. den Text etwas kürzen.

Sobald die Vorlage im Editor gut aussieht, können Sie die "Mobil" Vorschau nutzen - oben rechts finden Sie den Button "Mobil", welche Ihnen dann die Möglichkeit gibt, eine Inhaltsvorlage (z.B. das Geburtstags-Modul) für die Vorschau auszuwählen. Auch können Sie mit der Funktion "Sende Test-Email" schnell eine Email mit Test-Inhalten zur Layout-Kontrolle an eine beliebige Email-Adresse senden.


## Text-Version

Um das Risiko eines Spam-Ratings zu reduzieren und auch alte Email-Programm zu unterstützen empfiehlt es sich, auch die Text-Version der Vorlage zu bearbeiten. Mit Klick auf den Button "**TXTMODE**" öffnet sich der Editor der Text-Version - mit dem entsprechenden Button unten rechts kann dann automatisch eine Text-Version der Haupt-Vorlage angelegt und danach bearbeitet werden.


## Speichern einer Vorlage

Sind Sie mit den Anpassungen zufrieden? Dann ist es eine gute Idee, den aktuellen Stand als Vorlage zu speichern. Hierzu rechts den Button `als Layout-Vorlage speichern` anklicken und nach Angabe eines Namens die Vorlage abspeichern. Diese Version kann dann jederzeit unter  `Layout-Vorlage wählen > User` wieder geladen werden.
 
 
## Aufpasst: Nerd-Mode

Der "**Nerd-Mode**" erlaubt die Bearbeitung der Haupt-Vorlage in Code-Ansicht. Hier haben Sie vollen Zugriff auf den Code der Vorlage und Experten können dort komplexere Anpassungen vornehmen - Achtung: man kann auch schnell eine Vorlage "Kaputt"-verbessern, so dass die Darstellung auf den verschiedenen Email-Programmen (z.B. Outlook ist sehr undankbar) ungewünschte Ergebnisse bring.