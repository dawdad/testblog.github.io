---
title: Intro Promox version 8.0
subtitle: VMWare Migration / Produktiv Einsatz
gh-repo: dawdad/testblog.github.io
tags: [Tarek,Proxmox,VMWare,HPServer,Linux]
comments: true
full-width: false
last-updated: true
---


## Einleitung 

Diese Blog reihe wird einen PoC (Proof of Concept) mit Proxmox begleiten und ob Promox VMWare ESXi ersetzen kann, und ob dies ggf. eine Lösung für den produktiven Einsatz ist. 

Bei mir steht Proxmox schon länger auf der ToDo Liste, dies hat diverse Gründe, den Preis für Support welcher im Vergleich zu VMWare (Essentials Paket) geringer ausfällt. Auch der Funktionsumfang Out of the Box bestärkt mich dieses Produkt zu evaluieren. 

Mit dem Erscheinen von Proxmox Version 8.x am 22. Juni 2023 habe ich mir die ISO Datei geladen und zunächst einen kleinen VMWare nesseted Promox PoC durchgeführt. Dabei sind mir einige Themen aufgefallen, die ich im PoC auf Hardware näher erläutern möchte. 

> Alle Angaben erfolgten nach besten Wissen und Gewissen, ohne das eine Gewähr für die Richtigkeit, wir freuen uns auf anregungen und Feedback. 


###Part-1 Konfigurationsdesign

Ich beginne mit einem Router der für mich als DHCP/DNS Server fungiert, ich habe einen ProLiant DL380 Gen9 mit 4x 1GE Ports und einer LOM Karte mit 2x 10GE die später noch zum Einsatz kommt. 

Wir starten mit einer einfachen Netzwerkkonfiguration und verbinden den Server mit einem Port (Access) auf dem Switch auf dem ein Netzwerk (192.168.100.0/24) liegt.

Die Installation von Proxmox sieht wie folgt aus: 

Download der aktuellen ISO-Dateien für Proxmox VE (Virtual Environment): [https://enterprise.proxmox.com/iso/](https://enterprise.proxmox.com/iso/)

Die Installations Screenshots sind von der VMWare installation unterscheiden Sich aber zu der Hardware installation kaum. 

## Installations Screenshots:
<br/>
> Alle Einstellung können im System nach der Installation noch angepasst werden!

<pre>test-1</pre>
![]({{ '/assets/img/2023-07-22-promox-intro-1.png' | relative_url }})

<pre>test-1</pre>
![]({{ '/assets/img/2023-07-22-promox-intro-2.png' | relative_url }})

<pre>test-1</pre>
![]({{ '/assets/img/2023-07-22-promox-intro-3.png' | relative_url }})

<pre>test-1</pre>
![]({{ '/assets/img/2023-07-22-promox-intro-4.png' | relative_url }})

<pre>test-1</pre>
![]({{ '/assets/img/2023-07-22-promox-intro-5.png' | relative_url }})

<pre>test-1</pre>
![]({{ '/assets/img/2023-07-22-promox-intro-6.png' | relative_url }})
<br/>
<br/>