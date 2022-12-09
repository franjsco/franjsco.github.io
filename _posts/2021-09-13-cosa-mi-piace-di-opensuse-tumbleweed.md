---
layout: single
title:  "Cosa mi piace di openSUSE Tumbleweed"
date:   2021-09-01 00:00:00 +0000
categories: 
---

Nel post [GNU/Linux e l'opensource mi hanno cambiato la vita](https://franjsco.github.io/2021/09/01/gnulinux-opensource-mi-hanno-cambiato-la-vita.html) mi ero ripromesso di scrivere un post per argomentare perché mi piace **openSUSE Tumbleweed**.


## Cos'è openSUSE? 📜

<div align="center">
    <img src="https://i.giphy.com/media/wZQBoc6V821fSJMrRO/giphy.webp"  width="250px">
</div>

Per introdurre cos'è openSUSE, riporto quanto presente nella wiki ufficiale del progetto:

>Il progetto openSUSE è l'espressione dell'impegno di una comunità diffusa in tutto il mondo per promuovere l'utilizzo di Linux ovunque. openSUSE crea una delle migliori distribuzioni Linux, e una varietà di strumenti utili (come OBS, OpenQA, KIWI, YaST, OSEM e molti altri), lavorando insieme in modo aperto, trasparente e in un clima di amichevole condivisione come parte della comunità mondiale del Software Libero e Open Source. 

Sembra più o meno chiaro, ma aggiungerei un ulteriore dettaglio:

È sponsorizzata da [SUSE](https://www.suse.com/it-it/) e la sua mascotte è un camaleonte simpatico.


## Cosa mi piace di Tumbleweed 🔥

<div align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/4/49/OpenSUSE_Tumbleweed_green_logo.svg" width="220px">
</div>

<div align="center">
    <img src="https://i.giphy.com/media/gPBKtKGk00TfD3D6mY/giphy.webp" width="250px">
</div>


[openSUSE Tumbleweed](https://en.opensuse.org/Portal:Tumbleweed) mi piace per alcune cosette come:

### Rolling release 🔄

Ha un modello di rilascio rolling, ovvero a rilascio continuo. 
Sono sempre alla ricerca dell'ultima versione software. E quindi, come potevo vivere senza una distribuzione rolling?? Non penso ci sia da aggiungere altro. Anzi si, consiglio una lettura di [Regular Release Distributions Are Wrong](https://rootco.de/2020-02-10-regular-releases-are-wrong/).


### Rollback per esseri umani ⏳

Le cose possono rompersi, e per sicurezza è meglio prepararsi. **openSUSE** ha uno strumento chiamato [snapper](https://en.opensuse.org/Portal:Snapper) (configurato out-of-box), che permette di creare e gestire snapshot del filesystem. Lo strumento rende molto semplice effettuare rollback di sistema direttamente dal boot loader (ho iniziato a dormire meglio la notte).


### Stabile e testata (con test automatici) 🧪

I rilasci/aggiornamenti di **openSUSE** sono testati mediante [openQA](https://openqa.opensuse.org/), un tool di testing automatico sviluppato in casa **openSUSE**. La vita è troppo breve per i test manuali!!

PS: nel tempo libero ho sviluppato [osqu](https://github.com/franjsco/osqu), un tool utilizzabile da CLI per consultare i test presenti su **openQA**.



### Agnostico sul desktop environment 😇

Ha un approccio agnostico sul desktop environment. Non avendone uno di default, lascia all'utente la possibilità di scegliere il suo preferito.

L'installer fornisce il supporto ufficiale ai seguenti DE: **KDE**, **GNOME**, **Xfce**.


Maggiori dettagli: 
[Desktop FAQ | How to choose a desktop environment](https://en.opensuse.org/openSUSE:Desktop_FAQ#How_to_choose_a_desktop_environment.3F).



###  Package manager 🧰

Ha [Zypper](https://en.opensuse.org/SDB:Zypper_usage), un package manager **rpm** più performante di **dnf** (spero che nessuno mi faccia fuori per questa affermazione). Mi trovo davvero bene e fino ad oggi non ho avuto rogne.


### openSUSE Build Service 📦

Ha [openSUSE Build Service](https://en.opensuse.org/Portal:Build_Service), un sistema automatizzato di build e distribuzione pacchetti da sorgenti. Su OBS è possibile trovare software aggiuntivo fornito da repository di terzi (o crearsi il proprio).

Maggiori dettagli: [Public Projects - openSUSE Build Service](https://build.opensuse.org/project#)

### Configura ogni aspetto con YaST 🔨

[YaST](https://yast.opensuse.org/) è un tool di installazione e configurazione per **openSUSE** e **SUSE Linux Enterprise**. Permette di controllare la maggior parte delle impostazioni di sistema e viene fornito con due interfacce: Qt e ncurses.

Ovviamente per me esiste solo l'interfaccia **ncurses**. 🤓

E per gli amanti dell'automazione, esiste [AutoYaST](https://doc.opensuse.org/projects/autoyast/). Uno strumento che permette di automatizzare installazioni e configurazioni di sistema mediante dei file di configurazione.


## Oltre Tumbleweed ✨

Per quanto preferisca **openSUSE Tumbleweed**, esistono altre versioni di **openSUSE** che vale la pena menzionare:


### openSUSE Leap

<div align="center">
    <img src="https://upload.wikimedia.org/wikipedia/commons/7/72/OpenSUSE_Leap_green_logo.svg" width="200px">
</div>

[openSUSE Leap](https://en.opensuse.org/Portal:Leap) è la versione di openSUSE a rilascio regolare. Ha il seguente ciclo di rilascio stimato:

-  Un rilascio minore è previsto circa ogni 12 mesi, allineato con SUSE Linux Enterprise Service Pack

-  Una release importante è prevista dopo circa 36-48 mesi, allineati con SUSE Linux Enterprise Release


### openSUSE MicroOS

<div align="center">
    <img src="https://microos.opensuse.org/assets/images/microos-logo.svg" width="200px">
</div>
[openSUSE MicroOS](https://microos.opensuse.org/) è una versione pensata principalmente per essere utilizzata nei container e negli edge devices. Essa è basata su openSUSE Tumbleweed.


### openSUSE KubicOS

<div align="center">
    <img src="https://kubic.opensuse.org/assets/images/logo.svg" width="200px">
</div>
[openSUSE KubicOS](https://kubic.opensuse.org/) è una distribuzione certificata Kubernetes ed è focalizzata su tecnologie correlate ai container.


## Conclusioni
Da quasi 2 anni a questa parte utilizzo **openSUSE Tumbleweed**. Oltre a trovarla un'ottima distribuzione l'ho trovata anche un buon compromesso: unisce alcune caratteristiche delle due distribuzioni che preferisco ([Fedora](https://getfedora.org/) e [ArchLinux](https://archlinux.org/)).

Alcuni link utili:

- [Sito Ufficiale](https://www.opensuse.org/)
- [Wiki](https://en.opensuse.org/Main_Page)
- [openSUSE News](https://news.opensuse.org/)
- [Software openSUSE](https://software.opensuse.org/)
- [openSUSE Build Service](https://build.opensuse.org/)
- [openQA](https://openqa.opensuse.org/)
- [PackMan repository](http://packman.links2linux.org/)


Bene, come con il precedente post, non potevo non lasciare una video-parodia prodotta da **SUSE**.

{% include video id="b0tsZB_LEQk" provider="youtube" %}