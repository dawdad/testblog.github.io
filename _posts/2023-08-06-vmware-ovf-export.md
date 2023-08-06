---
title: Export VM´s (VMWare) auf ein externes Laufwerk exportieren
subtitle: VMWare 7.x Export, OVF
gh-repo: dawdad/testblog.github.io
tags: [Tarek,VMWare]
comments: true
full-width: false
last-updated: true
---

# Inhaltsverzeichnis

1. [Einleitung](#Into)
2. [Durchführung](#durchführung)


## Intro

Beim Export von VMWare über die Console im Browser wird ein Download über HTTP/HTTPS auf den Client durchgeführt, mit dem man verbunden ist, was zu diversen Problemen führt, die man umgehen möchte. Der Export in ein Share oder Datastore ist leider nicht direkt aus der Webkonsole möglich. Hierfür bietet VMWare das [OVF Tool] (https://developer.vmware.com/web/tool/4.4.0/ovf) an, welches auf einen Client geladen werden muss. 

In diesem Beispiel wird ein Windows Jump Server im Netzwerk der ESXi Server verwendet, am Jump Server ist ein externes NFS Share angeschlossen, auf dem wir die OVF Dateien der Bestehenden VMs sammeln möchten.

> Alle Angaben erfolgen nach bestem Wissen, ohne Gewähr für die Richtigkeit, wir freuen uns über Anregungen und Rückmeldungen.

## Durchführung

Download der OVF Tools auf den Client. 

Über die Powershell in das Softwareverzeichnis wechseln

```
C:\VMware-ovftool-4.4.3-18663434-win.x86_64\ovftool
```

Zusammenstellung des Codes für den Export:

```
ovftool.exe "vi://<ESXI-BENUTZER>:<PASSWORT>@<IP-HOSTNAME-ESXI/<VM-NAME>" <ZIELVERZEICHNIS>
```

> Im Exportverzeichnis wird ein Unterverzeichnis mit dem Namen der virtuellen Maschine angelegt.

* ESXI-BENUTZER: root
* PASSWORT: xxxx
* IP-HOSTNAME-ESXI: esxiserver01
* VM-NAME: WindowsServer01
* ZIELVERZEICHNIS: Z:\export\vmware\

> Die virtuelle Maschine muss heruntergefahren sein.

Die Namen der virtuellen Maschinen können über SSH im folgenden Pfad (Datastore) überprüft werden.

```
/vmfs/volumes/<DATASTORE>
```


> Export der Virtuellen Maschine

![]({{ '/assets/img/2023-08-06-vmware-ovf-01.png' | relative_url }})


