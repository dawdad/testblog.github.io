---
layout: post
title: Intro Promox version 8.0
subtitle: VMWare Migration / Produktiv Einsatz
gh-repo: dawdad/testblog.github.io
tags: [Tarek,Proxmox,Linux]
comments: true
full-width: false
last-updated: true
---


### Einleitung 

PoC (Proof of Concept) ob Promox VMWare ESXi Server ersetzen kann und eine Lösung für evtl. produktiven Einsatz ist. 

Bei mir steht Proxmox schon länger auf der Liste um dieses Produkt zu evaluieren, dies hat diverse Gründe aber auch der Preis welcher im Vergleich zu VMWare selbst im Essentials Paket sehr gering ausfällt. Auch der Funktionsumfang Out of the Box von Proxmox bestärkt mich nun dieses Produkt zu evaluieren. 

Mit dem Erscheinen von Proxmox Version 8.x am 22. Juni 2023 habe ich mir direkt die ISO Datei geladen und zunächst einen kleinen VMWare nesseted Promox Test durchgeführt. Dabei sind mir einige Themen aufgefallen, die ich im PoC auf Hardware näher erläutern möchte. 

###Part-1 Konfigurationsdesign

Ich beginne mit einem Router der für mich als DHCP/DNS Server fungiert, ich habe einen ProLiant DL380 Gen9 mit 4x 1GE Ports und einer LOM Karte mit 2x 10GE die später noch zum Einsatz kommt. 

Wir starten mit einer einfachen Netzwerkkonfiguration und verbinden den Server mit einem Port (Access) auf dem Switch auf dem ein Netzwerk (192.168.100.0/24) liegt.

Die Installation von Proxmox sieht wie folgt aus: 

Download der aktuellen ISO-Dateien für Proxmox VE (Virtual Environment): https://enterprise.proxmox.com/iso/

#### Installations Screenshots:

1.

