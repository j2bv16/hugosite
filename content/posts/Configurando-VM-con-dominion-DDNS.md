---
title: "Configurar servidor web con dominio personalizado para que sea accesible desde internet"
date: "2021-09-06T21:20:43-04:00"
# weight: 1
# aliases: ["/first"]
tags: ["IPV6, RD"]
author: "Jose@blanco.com.do"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Configurando maquina virtual para accesar desde internet"
#canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
cover:
    image: "https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/images/virtualbox-main-empty.png" # image path/url
    alt: "<alt text>" # alt text
    caption: "Oracle Virtualbox" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/j2bv16/hugosite/tree/main/content"
    Text: "Sugerir Cambios" # edit text
    appendFilePath: true # to append file path to Edit link
---


## Lo que utilice para montar mi servidor personal
* Virtual box corriendo Ubuntu 21.04
* Apache2 + PHP 7.4
* ddclient para servicios Dynamic DNS
* Dominio namecheap con soporte Dyndns
* Certbot para SSl de letsEncrypt gratis

## Comandos de instalacion
    sudo apt install apache2
    sudo apt install php libapache2-mod-php
    sudo apt install ddclient
    sudo snap install --classic certbot

## Documentacion consultada
-   [Configurar DynDns Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/583/11/how-do-i-configure-ddclient/)
-   [Tutorial como configurar DDclient](https://serdima.wordpress.com/2018/04/23/tutorial-updating-dynamic-dns-with-ddclient/)
-   [Configurar apache2 con mas de un dominio](https://www.digitalocean.com/community/tutorials/how-to-set-up-apache-virtual-hosts-on-ubuntu-18-04-es)
-   [Obtener certificado con Certbot](https://certbot.eff.org/lets-encrypt/ubuntufocal-apache)

## Otros detalles

Puerto 80,443 abiertos en modem. Esta configuracion se obtiene mediante "NAT" y "Port Forwarding". Se deben apuntar estos puertos al ip asignado a tu servidor/maquina virtual.

#### Nota final
Es posible que para la configuracion especifica de cada caso se necesite investigar bastante. Google normalmente tiene la mayoria de las respuestas