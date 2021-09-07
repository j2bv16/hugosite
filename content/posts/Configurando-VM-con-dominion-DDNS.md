+++
title = "Configurando VM Con Dominio DDNS"
date = "2021-09-06T21:20:43-04:00"
author = "Jose Blanco"
authorTwitter = "J2bv16" #do not include @
cover = "https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/images/virtualbox-main-empty.png"
tags = ["VM", "DDNS"]
keywords = ["", ""]
description = "Configurando maquina virtual para accesar desde internet"
showFullContent = true
+++

## Contenidos de este servidor
* Virtual box corriendo Ubuntu 21.04
* Apache2 + PHP 7.4
* ddclient para servicios Dynamic DNS
* Dominio namecheap con soporte Dyndns
*  Certbot para SSl de letsEncrypt

## Comandos de instalacion
    sudo apt install apache2
    sudo apt install php libapache2-mod-php
    sudo apt install ddclient
    sudo snap install --classic certbot

## Documentacion consultada
* Configurar DynDns Namecheap
* Tutorial como configurar DDclient
* Configurar apache2 con mas de un dominio
* Obtener certificado con Certbot
## Otros detalles

Puerto 80,443 abiertos en modem. Esta configuracion se obtiene mediante "NAT" y "Port Forwarding". Se deben apuntar estos puertos al ip asignado a tu servidor/maquina virtual.

##### Es posible que para la configuracion especifica de cada caso se necesite investigar bastante. Google normalmente tiene la mayoria de las respuestas