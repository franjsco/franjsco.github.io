---
layout: single
title:  "AMQP, RabbitMQ e le code"
date:   2023-04-24 00:00:00 +0000
categories: 
---

Nell'ultimo periodo ho avuto modo di guardare un po più da vicino **AMQP** e **RabbitMQ**, il binomio perfetto per quanto riguarda comunicazioni asincrone e architettura a microservizi.


## 📜 Il protocollo AMQP
Il protocollo **AMQP** (*Advanced Message Queuing Protocol*) è uno standard aperto definito per garantire funzionalità di messaggistica, routing, accodamento e affidabilità. 

Uno dei principali usi di questo protocollo è la possibilità di implementare comunicazioni asincrone mediante code, particolarmente utilizzate nell'implementazione di architetture a microservizi.

### Concetti fondamenti
I principali concetti del protocollo sono:

- **`Messaggio`**: il dato, l'informazione che produce un `Producer`.
- **`Producer`**: si occupa di genera il messaggio e di inviarlo ad un `Broker`.
- **`Broker`**: si occupa di ricevere il messaggio ed effettuare il dispatch (_in base a delle regole definite dal tipo di `Exchange`_) verso diverse code (`Queue`).
- **`Queue`**: la coda dove il `Producer` mediante `Exchange` produce ed il `Consumer` consuma.
- **`Consumer`**: estrae il messaggio dalla `coda` per cui si è sottoscritto e lo consuma/elabora.
- **`Exchange`**: il componente che permette di definire le regole di binding e dispatch sulle code.

<img src="/assets/images/post/amqp-message-flow.png">


---

### Tipologie di Exchange
Il protocollo prevede diverse tipologie di exchange:

- **`DIRECT`**: effettua il dispatch dei messaggi a delle code in base ad una routing key.
- **`FANOUT`**: effettua il dispatch dei messaggi a tutte le code ignorando qualunque routing key.
- **`TOPIC`**: effettua il dispatch dei messaggi in base a dei pattern match specificati.
- **`HEADERS`**: effettua il dispatch dei messaggi usando l'header dei messaggi per il routing.

<img src="/assets/images/post/exchanges-example.png">


### Versioni del protcollo
Sono attualmente disponibili due versioni del protcollo: la 1.0 e la 0-9-1.



## ✉️ RabbitMQ, il message broker
**RabbitMQ** è uno dei _Message Broker_ opensource più importanti nel panorama odierno. Scritto in *Erlang*, implementa il protocollo AMQP v 0-9-1 e permette di essere esteso mediante dei plugin.

Esso dispone di un interfaccia di gestione e monitoring via web molto intuitiva:

<img src="/assets/images/post/rabbitmq-manager.jpg">

Dispone anche di diversi strumenti utilizzabili da CLI come: [rabbitmqctl](https://www.rabbitmq.com/rabbitmqctl.8.html), [rabbitmqadmin](https://www.rabbitmq.com/management-cli.html) e altri ancora.


Inoltre dispone di tutta una serie di funzionalità come: il clustering, Virtual hosting e auth.

## 🔗 Link utili

Qui di seguito potete trovare alcuni link utili che potete consultare:

- [Sito ufficiale - RabbitMQ](https://www.rabbitmq.com/)
- [Documentazione - RabbitMQ](https://www.rabbitmq.com/documentation.html)
- [Introduzione a Rabbit (Video) - DevDay Salerno](https://www.youtube.com/watch?v=pNlwdmE33CY)


## 🔚 Conclusioni
**AMQP** e **RabbitMQ** sono senza ombra di dubbio tecnologie interessanti e utilizzate tantissimo, partendo dalle piccole start-up fino ad arrivare ai grandi colossi enterprise. 

Sono inoltre delle tecnologie fondamentali per quanto riguarda architetture a microservizi e siuramente merita di essere approfondito come si deve, cosa che mi auguro di riuscire a fare nei prossimi mesi.
