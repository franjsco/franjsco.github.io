---
title: "trackmyd-bot"
excerpt: "Bot telegram che permette di tracciare dispositi GPS."
header:
  # image: https://picsum.photos/200
  teaser: /assets/images/portfolio/trackmydbot.png
sidebar:
  - title: "Informazioni"
    image: /assets/images/portfolio/trackmydbot.png
    image_alt: "logo"
    text: |
        **Tipologia**: Telgram Bot \\
        **Sorgente**: [GitHub](https://github.com/franjsco/trackmyd-bot)
gallery:
  - url: /assets/images/portfolio/trackmydbot.png
    image_path: /assets/images/portfolio/trackmydbot.png
    alt: "-"
---

Bot telgram che permette di tracciare dispositivi GPS.

{% include gallery caption="Screenshot" %}

## Architettura 
(*) **trackmyd-bot** usa [**trackmyd-api**](https://github.com/franjsco/trackmyd-api) per recuperare la posizione dei dispositivi

In aggiunta a **trackmyd-api** è necessario configurare [**GPSLogger**](https://github.com/mendhak/gpslogger) per l'invio della posizione del dispositivo al server.


<img align="center" src="/assets/images/portfolio/trackmydbot-architecture.jpg" height="200px">