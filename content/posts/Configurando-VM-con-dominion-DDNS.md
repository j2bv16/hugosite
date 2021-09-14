+++
title = "Configurar servidor web con dominio personalizado para que sea accesible desde internet"
date = "2021-09-06T21:20:43-04:00"
author = "Jose Blanco"
authorTwitter = "J2bv16" #do not include @
cover = "https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/images/virtualbox-main-empty.png"
tags = ["VM", "DDNS"]
keywords = ["", ""]
description = "Configurando maquina virtual para accesar desde internet"
showFullContent = false
+++

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

##### Es posible que para la configuracion especifica de cada caso se necesite investigar bastante. Google normalmente tiene la mayoria de las respuestas