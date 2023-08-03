---
title: Part-1 - Aufbau und Planung
subtitle: Netzwerke, Cluster, HA?, Storage
gh-repo: dawdad/testblog.github.io
tags: [Tarek,Proxmox,VMWare,HPServer,Linux]
comments: true
full-width: false
last-updated: true
---

# Inhaltsverzeichnis

1. [Einleitung](#Into)
2. [Systeme und ihr Aufbau](#systeme-und-ihr-aufbau)


## Intro

In diesem Teil des Blogs gehe auf die Planung für den Aufbau von Promox auf einem HP Proliant Gen9 Server für den PoC ein. Hierzu gibt es diverse Themen welche zu beachten sind.

Proxmox benötigt für den Cluster Betrieb (nicht zu verwechseln mit HA (High Avaliablity)) immer eine ungrade anzahl von Server, die alternative wäre ein Q-Device auf einem anderen Gerät z.B. Raspberry welcher die dritte Stimme des Clusters spielt. 

# Systeme und ihr Aufbau

Für die Planung des Setups sind zwei HP Server geplant, beide Server verfügugen über 4x 1GE Netzwerk Anschlüsse und 2x 10GE Anschlüsse, die vorteile einer Clusterlösung von Promox und der damit bestehenden Migrations Option von Containern und Virtuellen Maschinen werde ich eine Cluster Lösung ohne HA (High Avaliablity) planen. Hierdurch hat man direkt ein paar vorraussetungen z.B. Cluster Netzwerk für den CoroSync, ein Netzwerk für das Management (eigenes Subnetz ggf. eigener Anschluss) ein Netzwerk für die Frontend Kommunikation (Trunk Port für VLANs), Ein Migrations Netzwerk damit die Last beim verschieben von Virtuellen Maschinen nicht über das Management oder Frontend abgewickelt wird. 

> Unter berücksichtung von nur drei Netzwerken ergibt sich folgendes layout mit drei Hosts:

![]({{ '/assets/img/promox_netzwerk_setup_1.png' | relative_url }})

