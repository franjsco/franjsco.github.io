---
layout: single
title:  "Mantenere consistente il codice"
date:   2021-03-21 00:00:00 +0000
categories: 
---


In un progetto software, mantere consistente il codice seguendo gli stili e linee guida condivise è importante per l'evoluzione e la manutenzione della codebase.


Se ci sono più mani che lavorano alla stessa codebase, potrebbe capitare con molta facilità che la codebase del progetto diventi inconsistente.

Degli esempi di inconsistenza potrebbero essere:
- indentanzioni/spazi differenti
- codifica dei caratteri
- caratteri speciali di ritorno a capo 
- ecc...ecc...

## Cos'é EditorConfig?

> EditorConfig helps maintain consistent coding styles for multiple developers working on the same project across various editors and IDEs.

**EditorConfig** è uno strumento opensource che permette di uniformare lo stile di codifica di editor differenti. Il tutto predisponendo un file di configurazione chiamato `.editorconfig` con all'interno tutte le regole di cui necessitiamo.

La buona notizia è che molti editor usati nell'ambito della programmazione lo supportano nativamente. Qualora il vostro editor non lo suportasse nativamente, basterà semplicemente installarlo come plugin (sempre se il vostro editor ve lo permette).


## Installazione e configurazione
Potete verificare gli editor supportati nativamente o scaricare il plugin direttamente da [qui](https://editorconfig.org/#download).

Se necessitate dei dettagli su come configurare le regole, a [questo indirizzo](https://editorconfig.org/#file-format-details) potrete trovare tutte le informazione di cui necessitate.

Questo è tutto!  Passo e chiudo :)