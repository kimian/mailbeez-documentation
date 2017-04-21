---
# http://learn.getgrav.org/content/headers
title: Anpassung der Modul-Vorlagen
slug: anpassung-der-modul-vorlagen
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
Alle von MailBeez generierten Emails werden aus der gemeinsamen Haupt-Vorlage und Modul-Vorlagen zusammengesetzt. In diesem Tutorial wird beschrieben, wie die Vorlagen der Module bearbeitet werden können.

<div style="padding: 30px; border: 1px solid #c0c0c0; background-color: #FFFFFF; width: 100%; max-width: 600px; margin:auto" markdown="1">
[Gemeinsame Hauptvorlage](/dokumentation/tutorials/anpassung-der-hauptvorlage)
<div style="padding: 30px; border: 1px solid #c0c0c0; background-color: #E7F2FA;" markdown="1">Modul-spezifische Inhalts-Vorlage<br>
Platzhalter `{$body}`
<div style="padding: 30px; border: 1px solid #c0c0c0;" markdown="1">Produktlisten-Vorlage<br>
Platzhalter z.B. `{$list_engine.productlist}`
</div>
</div>
</div>


## Modul-Vorlage zum Bearbeiten öffnen

Alle Profi-Module enthalten den visuellen Editor, mit dem die modul-spezifischen Vorlagen (also der Inhalt welches die Module in das gemeinsame "Briefpapier" einfügen) komfortabel und visuelle bearbeitet werden können.

Die Modul-Vorlagen können jeweils im Modul, also z.b. für das Modul "[Gutschein: Geburtstags Glückwünsche](/dokumentation/mailbeez/coupon_birthday)" unter 

`MailBeez > MailBeez Module > Gutschein: Geburtstags Glückwünsche  > Template Verwaltung Button "bearbeiten"` 

im visuellen Editor zur Bearbeitung geöffnet werden.


## Laden einer Vorlage

Auf der rechten Seite kann mit Hilfe des Buttons `Layout-Vorlage wählen` eine Vorlage geladen werden. Wählen Sie dort die für das aktuelle Modul passende "**responsive**" Vorlage aus, um die aktuellste Version der mobilfreundlichen Modul-Vorlage zu laden.


## Anpassung des Inhaltes

Jede Vorlage ist aus einer Reihe von Inhalts-Elementen zusammengestellt, welche einzeln bearbeitet, verschoben oder auch entfernt werden können. Sobald Sie den Mouse-Zeiger über die Bereiche bewegen, werden Sie die Inhalts-Elemente erkennen. 

### Inhalt bearbeiten

Zeigt sich links ein Bleistift-Symbol? Einfach anklicken und es öffnet sich die jeweilige Bearbeitungs-Ansicht.

### Element verschieben

In dem Kontext-Menü rechts sehen Sie Pfeile (oben/unten) - mit klick auf den gewünschten Pfeil verschieben Sie das aktuelle Element entweder nach oben oder unten


### Element löschen

Die Mülltonne-Schaltfläche im  Kontext-Menü macht genau dies - es entfernt das aktuelle Element

### Element einfügen

Mit Klick auf das +-Symbol Kontext-Menü öffnet sich eine Auswahl der einfügbare Inhalts-Elemente. Mit Klick wird das gewünschte Element nach dem aktuellen Element eingefügt.

## Testen der Vorlage

Im visuellen Editor finden Sie oben links Buttons wie "320px", "480px" - hiermit können Sie jederzeit beim bearbeiten testen, wie die Vorlage auf mobilen Endgeräten umgebrochen wird. Sollte sich die Vorlage nach einigen Anpassungen nicht sauber auf z.B. 320px umbrechen, dann gibt es ein Element (z.B. ein Bild) welches eine feste Breiten-Angabe hat und somit nicht angepasst werden kann. In diesem Fall als Breite "100%" angeben. Auch lange URLs können Probleme machen, ggf. den Text etwas kürzen.

Sobald die Vorlage im Editor gut aussieht, können Sie die "Mobil" Vorschau nutzen - oben rechts finden Sie den Button "Mobil", welche Ihnen dann die aktuelle Vorlage interaktiv in verschiedenen mobilen Endgeräten anzeigt. Auch können Sie mit der Funktion "Sende Test-Email" schnell eine Email mit Test-Inhalten zur Layout-Kontrolle an eine beliebige Email-Adresse senden.


## Text-Version

Um das Risiko eines Spam-Ratings zu reduzieren und auch alte Email-Programm zu unterstützen empfiehlt es sich, auch die Text-Version der Vorlage zu bearbeiten. Mit Klick auf den Button "**TXTMODE**" öffnet sich der Editor der Text-Version - mit dem entsprechenden Button unten rechts kann dann automatisch eine Text-Version der Modul-Vorlage angelegt und danach bearbeitet werden.


## Speichern einer Vorlage

Sind Sie mit den Anpassungen zufrieden? Dann ist es eine gute Idee, den aktuellen Stand als Vorlage zu speichern. Hierzu rechts den Button `als Layout-Vorlage speichern` anklicken und nach Angabe eines Namens die Vorlage abspeichern. Diese Version kann dann jederzeit unter  `Layout-Vorlage wählen > User` wieder geladen werden.
 
 
## Aufpasst: Nerd-Mode

Der "**Nerd-Mode**" erlaubt die Bearbeitung der Modul-Vorlagen in Code-Ansicht. Hier haben Sie vollen Zugriff auf den Code der Vorlage und Experten können dort komplexere Anpassungen vornehmen - Achtung: man kann auch schnell eine Vorlage "Kaputt"-verbessern, so dass die Darstellung auf den verschiedenen Email-Programmen (z.B. Outlook ist sehr undankbar) ungewünschte Ergebnisse bring.