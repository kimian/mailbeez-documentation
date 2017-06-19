---
# http://learn.getgrav.org/content/headers
title: MailChimp Integration
slug: config_mailchimp
routes:
    default: /dokumentation/configbeez/config_mailchimp
    aliases:
        - /download/the-mailchimp-connector
        - /download/the-mailchimp-connector/oscommerce
        - /download/the-mailchimp-connector/zencart
# menu: MailChimp Integration
date: 02-03-2012
published: true
publish_date: 02-03-2012
# unpublish_date: 02-03-2012
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
    code: 'config_mailchimp'
    category: [configbeez]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]
    thumbnail: 'http://www.mailbeez.com/wp-content/uploads/downloads/thumbnails/2012/11/icon_64.png'
    pro: 'pro'
    cert: 'true'
    price: '300 EUR'
    title_en: 'MailChimp Integration'
    teaser_en: 'MailBeez unlocks, MailChimp delivers'
    title_de: 'MailChimp Integration'
    teaser_de: 'MailBeez verfasst, MailChimp liefert'
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


##Die MailBeez für MailChimp Integration
<div style="float:right;margin-top: -48px !important" markdown="1">
![](mc_connector_badge.png?resize=380,328)
</div>

Wollen Sie MailBeez nutzen, aber die intelligent personalisierten Emails über Ihren MailChimp account versenden?  
 Mit unserer offizielle MailChimp Integration ist dies möglich. (Die Integration wurde in enger Zusammenarbeit mit MailChimp entwickelt)


**Was genau macht MailBeez?**

Wenn Sie ein zu MailBeez kompatibles Shop-System nutzen, aber noch nicht wissen, was MailBeez ist - dann hier eine kurze Zusammenfassung: MailBeez läuft als integrierter Bestandteil Ihres Shopsystemes und ist modular aufgebaut. Von **automatisierten Einladungen zur Produktbewertung** bis hin zum Versand von **personalisierten Angebots-Gutscheinen**, kann MailBeez Ihnen helfen, **mehr Umsatz** aus Ihrer bestehenden Kundendatenbank zu generieren und den Kunden-Lebenszyklus intelligient auszunutzen.

**Hmm, klingt gut, und MailChimp?**

Falls Sie es noch nicht wissen: MailChimp ist ein hervorragendes Newsletter-System, mit dem Sie schnell und einfach gelungene Newsletter erstellen und versenden können. Die zertifizierten Server sorgen dafür, dass die Newsletter auch in die Inbox der Empfänger landen.  
 Aus diesem einfachen Grund verlassen sich tausende von Unternehmen weltweit auf das MailChimp System, um ihre Newsletter zu versenden.


**und jetzt beides kombinieren.**

Sie wollen die intelligente, integrierte Personalisierung von MailBeez nutzen, aber sich auf die Versende-Qualität von MailChip verlassen? Dann ist diese Integration genau die richtige Lösung: MailBeez generiert - MailChmip versendet.

>>>>>MailChimp ist toll, aber das System bereitet einige Kopfschmerzen z.B. aufgrund der begrenzten Anzahl von Personalisierungs-Feldern.  
 Wenn Sie nicht unbedingt über MailChimp versenden wollen, dann empfehlen wir, [Newsletter2Go als Email-System](/dokumentation/configbeez/config_email_engine) zu konfigurieren. Sie werden vergleichbare Zustellraten erreichen, aber ohne die Begrenzungen von MailChimp.

##Vorteile

**ZUSTELLRATEN!** optimieren Sie die Zustellraten durch den Versand über die Server von MailChimp  
 **DATEN-ABGLEICH!** durch eine echte 2-Wege Synkronisierung werden die Subscriber-Daten von MailChimp und vom Shop abgeglichen  
 **AUTOMATISCH!** volle Automatisierung sobald das System eingerichtet und auf Auto-Pilot gesetzt ist.
 
Enwickelt in enger Zusammenarbeit mit MailChimp: geprüft und abgenommen!  
 Neu: auch Listen mit über 15.000 Subscribern können Dank schneller Delta-Technik abgeglichen werden   
 Einfache Installation: Dank Assistent und Simulations-Unterstützung




##Mailchimp-fähige Module:
Die MailChimp-Integration kann mit allen MailChimp-fähigen Profi-Module eingesetzt werden:
<ul class="mc_read_list">
    {% for p in page.find('/dokumentation/mailbeez').children  if p.header.module.mc_ready %}
    <li>
    {# workaround #}
    {{ "[#{p.title}](#{p.url})"|markdown }}
    </li>
    {% endfor %}
</ul>