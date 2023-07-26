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
2. [](#)


## Intro

In diesem Teil des Blogs gehe auf die Planung für den Aufbau von Promox auf einem HP Proliant Gen9 Server für den PoC ein. Hierzu gibt es diverse Themen welche zu beachten sind.

Proxmox benötigt für den Cluster Betrieb (nicht zu verwechseln mit HA (High Avaliablity)) immer eine ungrade anzahl von Server, die alternative wäre ein Q-Device auf einem anderen Gerät z.B. Raspberry welcher die dritte Stimme des Clusters spielt. 

# Systeme und ihr Aufbau

Für die Planung des Setups sind zwei HP Server geplant, beide Server verfügugen über 4x 1GE Netzwerk Anschlüsse und 2x 10GE Anschlüsse

> Quote

Link [https://xxx.xxx](https://xxx.xxx)


![]({{ '/assets/img/xxxxx.png' | relative_url }})
