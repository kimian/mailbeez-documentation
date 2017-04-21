---
# http://learn.getgrav.org/content/headers
title: Erstellen eines Newsletter Anmeldeformulars
slug: erstellen-eines-newsletter-anmeldeformulars
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

>>>>>**Voraussetzung**  
 Technisches Wissen im Umgang mit HTML, CSS und Javascript  
 Die Code-Beispiele müssen "gelesen", verstanden und angepasst werden.



MailBeez unterstützt mit dem Modul [MailBeez Newsletter Profi ab Version 3.72](/dokumentation/mailbeez/newsletter) vollständig den Prozess der Erfassung von Interessenten-Emails in konfigurierbaren Themen-Gruppen. Aber auch bestehende Kunden können sich für den Newsletter und auch Themenbereich registrieren. Die API erkennt selbständig, ob eine Email-Adresse zu einem bestehenden Kunden gehört oder ob diese einen neuen Interessenten darstellt.
In diesem Tutorial lernen Sie, wie Sie selbst ein Anmelde-Formular erstellen können. Dieses Formlar kann sowohl im Shop aber auch auf jeder anderen Webseite eingefügt werden.


>>>>>**Vorbemerkung**  
 In absehbarer Zeit (Stand Oktober 2016) wird das MailBeez System um `SiteBeez` erweitert. Mit Hilfe von SiteBeez können intelligent Email-Adressen von Besuchern und Kunden erfasst werden.


## Vorab-Überlegungen

Mit jedem zusätzlichen Eingabe-Feld fällt die Conversion-Rate von Formularen, daher begrenzen wir uns in diesem Beispiel auf das Feld `prospect_email`. Dank der intelligenten progressiven  Datenerfassung bekommen Interessenten nach Klick auf den Double-Opt-In Link auf der dann erscheinenden Bestätigungs-Seite die Möglichkeit, die Angaben Vorname und Nachname zu ergänzen. Bei Kunden liegen diese Informationen bereits vor und es werden keine weiteren Möglichkeiten zur Dateneingabe angeboten.


## Erstellen eines Anmeldeformulares

Zunächst benötigen wir den HTML-Code für das Anmeldeformular. Nachfolgend ein einfaches Grundgerüst, welches ein Eingabefeld für die Email-Adresse sowie verschiedene Meldungen enthält. Die Meldungen sind mit Hilfe von `style="display: none;"` ausgeblendet und werden mit Hilfe von JavaScript angezeigt. Bei der Entwicklung kann es hilfreich sein, die Meldungen anzuzeigen - dafür dann die Style-Angabe entsprechend z.B. in `style="display: block;"` ändern.


Im Hidden-Field `topic_ids` sind die IDs der Themenbereiche 1 und 3 hinterlegt. Zunächst diese Themenbereich im Newsletter Modul anlegen. Bei Registrierung über dieses Formular wird die zu registrierende Email-Adresse automatisch den Themenbereich 1 und 3 zugeordnet.

```html
<div id="capture_prospect">
  <form method="post" action="" id="capture_prospect">
    <!-- in diesem Beispiel soll die Email den Themenbereichen 1 und 3 zugeordnet werden -->

    <input type="hidden" name="topic_ids" id="prospect_topics" value="1,3">
    <!-- bitte nach eigenen Wünschen anpassen -->
    <dl>
      <dt>
        <strong>Wollen Sie auf dem laufenden bleiben?</strong>
        Dann registrieren Sie sich hier für unseren Newsletter
      </dt>
      <dd id="mailing_list" class="">
        <input type="text" name="email_address" id="prospect_email" class="text">
        <!-- Button - please customize to your needs -->
        <button id="capture_prospect_submit_button" class="capture_prospect_submit_button">Submit</button>

        <div id="capture_prospect_submit_button_loader"></div>

        <!-- Message - please customize to your needs -->
        <div id="subscribe_success" style="display: none;">Bitte bestätigen Sie Ihre Registrierungen - wir haben Ihnen hierzu eine Email geschickt</div>
        <div id="error_invalid" style="display: none;">Ungültige Email</div>
        <div id="error_duplicate" style="display: none;">Email ist bereits vorhanden</div>
      </dd>
    </dl>
  </form>
</div>
```

Sie können das Anmelde-Formular mit Hilfe von CSS nach Ihren Wünschen gestalten.


## JavaScript Code zur AJAX-Anbindung an die MailBeez Newsletter API

Um das Formular zum Leben zu erwecken, ist noch etwa JavaScript /jQuery Code erforderlich, dieser Code muss auf der Seite des obigen HTML-Codes eingefügt werden. In unserem Bespiel ist MailBeez auf `www.shop.de/mailhive` installiert. Diese Url muss natürlich auf die URL des "echten" Shops angepasst werden. Am besten sollte `https` zum Einsatz kommen.

Der API-Aufruf ist dokumentiert auf der Seite [MailBeez Newsletter API](/dokumentation/configbeez/config_api/mb_newsletter_api).


```javascript
// in diesem Beispiel ist MailBeez auf www.shop.de/mailhive installiert, bitte anpassen
// Prüfe ob jQuery vorhanden ist, sonst aus dem MailBeez System laden
<script>window.jQuery || document.write('<script src="http://www.shop.de/mailhive/common/js/jquery-1.8.2.min.js">\x3C/script>')</script>

<script type="text/javascript">
  $(document).ready(function () {

    $("#prospect_email").focus(function () {
      $('#mailing_list dd').removeClass("error").addClass('focus');
    });
    $("#prospect_email").blur(function () {
      if ($("#prospect_email").attr("value") == "") $('#mailing_list dd').removeClass("focus", "error");
    });
    var loader = jQuery('<img src="http://www.shop.de/mailbeez/mb_newsletter/includes/templates/loading.gif" alt="loading..."  style="margin-top: 10px;" />')
        .appendTo("#capture_prospect_submit_button_loader")
        .hide();
    $('#capture_prospect_submit_button').click(function () {
      loader.show();
      $('#capture_prospect_submit_button').hide();
      $('#error_invalid').hide();
      $('#error_duplicate').hide();
      $.ajax({
        type: 'POST',
        url: 'http://www.shop.de/mailhive.php/api/public/v1.0/newsletter/add/',
        dataType: 'json',
        data: {
          email: $('#prospect_email').val(),
          firstname: $('#prospect_firstname').val(),
          lastname: $('#prospect_lastname').val(),
          gender: $('#prospect_gender').val(),
          topic_ids: $('#prospect_topics').val(),
          lng_id: '2'
        },
        success: function (data) {
          if (data.error === false) {
            loader.hide();
            $('#subscribe_success').show();
            $('#capture_prospect_submit_button').hide();
            $('.subscribe_success_hide').hide();
            $('#capture_prospect dd').removeClass().addClass('success');
          } else if (data.error === "invalid_email") {
            loader.hide();
            $('#capture_prospect_submit_button').show();
            $('#capture_prospect dd').removeClass().addClass('error');
            $('#error_invalid').show();
          } else if (data.error === "duplicate") {
            loader.hide();
            $('#capture_prospect_submit_button').show();
            $('#capture_prospect dd').removeClass().addClass('error');
            $('#error_duplicate').show();
          } else if (data.error === true) {
            loader.hide();
            $('#capture_prospect_submit_button').show();
            $('#capture_prospect dd').removeClass().addClass('error');
          }
        }
      });
      return false;
    });
  });

</script>
```


## Problembehebung

Bei der Entwicklung empfiehlt sich FireFox mit der Erweiterung FireBug oder natürlich jeder anderer Browser mit Entwickler-Unterstützung. Mit Hilfe dieser Tools können JavaScript Fehler erkannt und die AJAX-Requests beobachtet werden. 
