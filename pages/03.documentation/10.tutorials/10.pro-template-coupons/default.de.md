---
# http://learn.getgrav.org/content/headers
title: Erstellen von Vorlagen-Gutscheinen
slug: erstellen-von-vorlagen-gutscheinen
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

>>>>>> Lassen Sie sich den Ablauf direkt in Ihrem Shop-System von dem Lehrgang zum Anlegen von Vorlagen-Gutscheinen zeigen

In diesem Tutorial lernen Sie, wie Sie Vorlagen-Gutscheine anlegen und in den entsprechenden Module konfigurieren.


## Personalisierte Gutscheine

Der MailBeez [Gutschein-Generator](/dokumentation/configbeez/config_coupon_engine) wird als Untermodul von allen MailBeez Modulen verwendet, welche personalisierte Gutscheine generieren und versenden.

Am Beispiel des Modules [Gutschein: Geburtstags Glückwünsche ](/dokumentation/mailbeez/coupon_birthday) gehen wir die Schritte zur Konfiguration durch - dieser Ablauf lässt sich auf alle anderen MailBeez-Module mit Gutschein-Funktion übertragen.

## Funktionsweise

Der MailBeez Gutschein-Generator generiert basierend auf einem konfigurierten Vorlagen-Gutscheine neue Gutscheine. Die generierten Gutscheine sind eine Kopie des Vorlagen-Gutscheines, allerdings wurde das **Ablaufdatum** und der **Gutschein-Code** individuell generiert. So wird sichergestellt, dass jeder Kunde einen individuellen Gutschein-Code erhält, welcher nur solange gültig ist, wie im jeweilige Modul (z.B. "Gutschein: Geburtstags Glückwünsche") konfiguriert worden ist

## Anlegen eines Vorlagen-Gutscheines

>>>>> Bitte sicherstellen, dass das Gutschein-System aktiviert ist (osCommerce: ein [kompatibles Gutschein-Addon](/dokumentation/configbeez/config_coupon_engine) muss installiert sein)

Navigieren Sie in der Shop-Administration zum Abschnitt "Gutscheine".

Klicken Sie dort auf "Neuer Gutschein".

Geben Sie im Feld **Gutschein-Code** (nicht Name) folgendes ein: `template_birthday`.

Wichtig ist, dass der **Gutschein-Code** mit `template_` anfängt, da dies Vorlagen-Gutscheine kennzeichnet. Anderfalls kann der Vorlagen-Gutschein nicht im folgenden Abschnitt zugeordnet werden.

Konfigurieren Sie den Vorlagen-Gutschein nach Ihren Wünschen, z.B. "10%" Rabatt. Alle Angaben - ausser das Gültigkeitsdatum - werden auf die generierten Gutscheine übertragen.

Speichern Sie den Gutschein ab. (Wichtig: nach dem 1. Klick wird eine Seite zur Prüfung der Angaben gezeigt, dort dann nochmals speichner klicken)

## Zuordnen des Vorlagen-Gutscheines

Vergewissern Sie sich, dass der neu angelegte Vorlagen-Gutschein im Gutschein-System Ihres Shops zu sehen ist.

Wechseln Sie dann nach `MailBeez > MailBeez Module > Gutschein: Geburtstag` und klicken Sie dort im rechten Bereich oben auf den Button **Bearbeiten**, um die Konfigurations-Ansicht dieses Modules zu öffnen. Weiter unten im rechten Bereich finden Sie eine Auswahl-Liste, in der Sie den angelegten Vorlagen-Gutschein wählen können.

Speichern Sie die Konfiguration des Modules.

In der Ansicht rechts sehen Sie im unteren Bereich, dass der Vorlagen-Gutschein zugeordnet worden ist.


## Wissenswertes

### Testen des Gutschein-Generators

Sie können mit Hilfe der Betriebsart "Simulation" die Generierung von Gutscheinen testen. Stellen Sie dazu sicher, dass MailBeez sich in der Betriebsart "Simulation" befindet (Anzeige oben rechts) und führen Sie das Modul "Gutschein: Geburtstags Glückwünsche" aus - es werden "echte" Emails generiert, diese werden aber alle an die konfiguration Simulations-Email-Adresse versendet und sind mit **[SIM]** im Betreff gekennzeichnet.

Im Gutschein-System werden Sie zu jeder Email einen generierten Gutschein finden. Die Simulations-Gutscheine sind mit **[SIM]** im Gutschein-Code gekennzeichnet. Diese Gutscheine sind voll funktionsfähig, d.h. Sie können hiermit Test-Bestellungen vornehmen.

### Löschen von Simulations-Gutscheinen

Die im Simulations-Modus angelegten Gutscheine können im jeweilige Modul mit dem dafür erscheinenden Button gelöscht werden. Alternativ können Sie auch die Lösch-Funktion unter `MailBeez > Konfiguration > Gutschein Generator` nutzen.

### Löschen alter Gutscheine
Mit der Zeit werden tausende von Gutscheinen generiert werden. Unter `MailBeez > Konfiguration > Gutschein Generator` finden Sie eine praktische "Aufräum"-Funktion, um verfallene Gutscheine zu löschen.


### Finden von Gutscheinen

Auf dem MailBeez Dashboard finden Sie eine Suchfunktion (ggf. unter `MailBeez > Konfiguration > Dashboard Konfiguration` nachinstallieren), mit der Sie schnell Gutscheine - oder auch Vorlagen-Gutscheine finden und dann zur Bearbeitung öffnen können.

>>>>>> Suchen Sie nach **template_**, um alle Vorlagen-Gutscheine zu finden und direkt zur Bearbeitung öffnen zu können