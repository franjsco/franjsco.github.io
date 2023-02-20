---
layout: single
title:  "Una gentile introduzione a Git"
date:   2023-01-20 00:00:00 +0000
categories: 
---

In questo post proverò ad introdurre in modo molto gentile **Git**, lo strumento indispensabile per qualunque sviluppatore.


## ❓ Cosa è Git?

<img style="float: right; max-height: 180px" src="/assets/images/post/logo-git.png">
Git è un software di controllo di versione distribuito sviluppato da **Linus Torvalds** (si, il papà del kernel Linux). 

Il suo scopo è quello di tenere traccia di tutte le modifiche apportate al codice e  permettere la collaborazione decentralizzata tra sviluppatori.


## 📜 Concetti fondamentali

Elenchiamo alcuni concetti fondamentali riguardo a Git:

- **Repository:** 
    è il luogo dove è presente il codice e la relativa storia. Il repository può essere sia locale che remoto. Git permette di lavorare al proprio progetto localmente per poi sincronizzare modifiche con repository remoti (e viceversa). Questo permette la collaborazione tra gli svillupatori in modo davvero efficace. I repository remoti sono solitamente hostati su piattaforme dedicate come [GitHub](), [GitLab]() o soluzioni on-premise. I file che permettono a Git di funzionare, risiedono nella cartella nascosta `.git`.

- **Commit:**
    un'istantanea del progetto in un determinato momento. Git permette di tenere traccia delle modifiche effettuando dei commit. In ogni commit è possibile visionare le modifiche apportate, la data e il relativo autore di tali modifiche. 

- **Branch:**
    utilizzato per ramificare il codice. È possibile iniziare ad apportare modifiche da un commit su un determinato branch per poi ramificare le successive modifiche in diversi branch. Questo permette sia di organizzare meglio gli sviluppi ma anche di lavorare contemporanemente in modo parallelo. 

- **Merge:**
    processo per fondere/unire un branch con un altro. In parole semplici, il concetto di merge è: permette di unire modifiche di diversi branch in un singolo branch. Git provvederà ad individuare le varie differenze per permettere un'integrazione corretta. Non sempre fila tutto liscio e delle volte è necessario l'intervento manuale.


- **Working directory:**
    l'area contenente il nostro codice. Git monitora costantemente i file al suo interno.

- **Staging area:**
    area virtuale predisposta a prepare i commit. I file vengono aggiunti alla staging area per poi permettere il commit.

- **Gli stati dei file:**
    Git è un osservatore che controlla costantemente i file.
    I file presenti nella directory che git monitora, possono avere i seguenti stati:

    - **<u>untracked</u>**: il file non sarà versionato, quindi non preso in considerazione da Git.
    - **<u>modified</u>**: il file è cambiato rispetto al suo ultimo commit/salvataggio.
    - **<u>staged</u>**: il file è stato segnalato per essere salvato nel prossimo commit.
    - **<u>committed</u>**: il file sono stati congelati (in un commit) in un preciso istante.

## 🔄 Flusso di lavoro

Git ha un suo flusso di lavoro, come ben rappresentato nell'immagine sottostante:

<figure>
    <img src="/assets/images/post/git.png" alt="flusso di lavoro git">
    <figcaption>Flusso di lavoro Git</figcaption>
</figure>

Vediamolo nel dettaglio:

- **Inizializzazione di un repository**<br>
    Prima di tutto, per poter lavorare con Git, occorre inizializzare il repository.
    Per farlo, occorre creare la directory dove abbiamo intenzione di lavorare, entrarci e lanciare il comando:

    ```sh
    git init
    ```
    
    Se invece il progetto è gia presente su un remote, occorrerà clonarlo, lanciando il comando:

    ```sh
    git clone <url-repo-remoto>
    ```
    

- **Aggiungere un file alla staging area** <br>
    Per aggiungere un file alla staging area, ovvero l'area temporanea predisposta a preparare il commit, occorrerà lanciare il comando:

    ```sh
    git add <nome-del-file>
    # oppure si possono aggiungere tutti i file con:
    git add .
    ```
    

- **Effettuare il commit** <br>
    Dopo che sono stati aggiunti i file alla staging area, è possibile effettuare il commit con il seguente comando:
    ```sh
    git commit -m "<messaggio-del-commit>"
    ```


- **Sincronizzarsi con il remote** <br>
    Dopo aver effettuato i commit, è necessario sincronizzare le modifiche dal locale al remote, mediante il comando:
    ```sh
    git push -u origin <nome-branch>
    ```
    <br>
    Per sincronizzare le modifiche presenti sul remote nel repo locale, è possibile utilizzare:
    ```sh
    # per scaricare le sole modifiche dal remote:
    git fetch

    # per scaricarele e integrarle nella working directory:
    git pull
    ```

## 🍃 Ramificazioni

Git utilizza i branch per ramificare le modifiche. Questo permette di organizzare le modifiche e sviluppare in modo completamente parallelo.

<figure>
    <img src="/assets/images/post/git-branch.png" alt="Branch di git">
    <figcaption>Branch di git</figcaption>
</figure>




Prendiamo come esempio l'immagine precedente. In essa sono presenti due branch, `master` e `new_feature`.


- **Creazione di un branch** <br>
    Supponiamo che nel branch `master` ci sia codice attualmente in produzione e abbiamo la necessità di sviluppare nuove feature mantenedo intatta la codebase. In questo caso si procederà alla creazione di un branch partendo dal branch `master` mediante il seguente comando:

    ```sh
    git checkout -b new_feature 
    ```
    Con questo comando, git procederà a creare un nuovo branch `new_feature` e si sposterà al suo interno. Tutti i commit successivi seguiranno una diramazione diversa mantendo intatto il codice presente su `master`. Possiamo rivedere l'immagine precedente dove sul branch `new_feature` sono rappresentati due commit. <br>



- **Merge dei branch** <br>
    Riprendedo sempre l'immagine precedente, dopo due commit viene effettuato il merge su `master`. 
    Il merge non è nient'altro che una fusione tra due branch.

    Per effettuare il merge è necessario prima di tutto passare sul branch `master` con:
    ```sh
    git checkout master
    ```
    e successivamente lanciare il comando di merge indicando il branch da fondere in `master`:
    ```sh
    git merge new_feature
    ```

## 🔚 Conclusioni
**Git** è uno strumento meraviglioso e super utile e merita di essere approfondito. Nel prossimo capitolo è possibile trovare diverse risorse utili per l'apprendimento e ulteriori approfondimento.


## ℹ️ Risorse utili


- [Pro Git](https://git-scm.com/book/en/v2). Un ottimo libro molto completo consultabile online gratuitamente.

- [Oh My Git!](https://ohmygit.org/). Un gioco opensource che permette di imparare Git divertendosi.

- [Learn Git Branching](https://learngitbranching.js.org). Web app che permette di imparare il branching mediante delle sfide.


- [Git cheat sheet by Atlassian](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).