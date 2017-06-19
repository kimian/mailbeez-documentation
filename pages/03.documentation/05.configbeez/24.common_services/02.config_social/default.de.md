---
title: Social Sharing
slug: config_social
routes:
    default: /dokumentation/configbeez/config_social
    aliases:
        - /dokumentation/configbeez/social-sharing

date: 31-08-2011
published: true
publish_date: 31-08-2011
template: docs
visible: true
summary:
    enabled: true
    format: short
    size: 128
taxonomy:
    migration_status: done
    category:
        - docs
    tag: [pro]
module:
    code: 'pro'
    category: [pro]
    compatiblity: [comp_osc,comp_cre,comp_digi,comp_zencart,comp_xtc,comp_xtcm2,comp_gambio]   
    pro: 'pro'          
author:
    name: admin
metadata:
    author: admin
---

## Social Sharing in Emails


Als gemeines Dienst-Modul erlaubt dieses Unter-Modul das Einfügen von Social Sharing Elementen in die Produkt Listen. Sie können wählen, für welche der Sozialen Seiten Facebook, Twitter, oder Google+ Sie Share Buttons einfügen wollen.

![](Screen_social_email.de.jpg?resize=582)

>>>>> Standardmässig sind die Share Link nicht in den responsive Email Vorlagen enthalten, um diese so schlank wie möglich zu halten.


Nachfolgendes Beispiel zeigt, wie die Social Sharing Link - in diesem Fall die Vorlage "tiny" - in die Produkt-Listen Vorlagen unter Verwendung von `{$products[product].social_tiny}` eingfügt werden kann: 

```text
{section name=product loop=$products max=$max_products}
(...)
   {$products[product].social_tiny}
(...)
{/section}
```

**Wichtig**: Das Tag `{$products[product].social_tiny}` kann nur innerhalb der `products` Schleife, da Produkt-Daten verwendet werden. 
