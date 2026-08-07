# LabTV

Applicazione Angular dedicata alla scoperta di film. Integra la TMDB API per mostrare catalogo, ricerca, dettagli, cast, regista e titoli simili.

[Demo live](https://lab-tv.vercel.app/)

## Funzionalità

- catalogo di film recuperato tramite richieste HTTP;
- ricerca locale per titolo con aggiornamento reattivo dei risultati;
- pagina di dettaglio con informazioni del film, cast e regista;
- suggerimenti di film simili;
- gestione esplicita degli stati di caricamento e degli errori;
- navigazione tramite Angular Router;
- interfaccia responsive basata su Bootstrap.

## Tecnologie

- Angular 21
- TypeScript 5.9
- RxJS
- Angular Signals
- Angular Router e HttpClient
- Bootstrap 5 e Bootstrap Icons
- TMDB API
- Vitest

## Struttura applicativa

```text
src/app
├── components
│   ├── catalogo
│   ├── contatti
│   ├── login
│   ├── movie-card
│   ├── movie-detail
│   └── ricerca
├── layout
├── pages
├── services
│   └── movie-service.ts
└── app.routes.ts
```

`MovieService` centralizza l'accesso alla TMDB API attraverso `HttpClient` e restituisce `Observable` tipizzati. I componenti mantengono lo stato locale con Signals e separano catalogo, ricerca, scheda riutilizzabile e dettaglio.

## Avvio in locale

### Requisiti

- Node.js in versione LTS
- npm

```bash
git clone https://github.com/fabiozagaria/LabTV.git
cd LabTV
npm install
npm start
```

L'applicazione sarà disponibile su `http://localhost:4200`.

## TMDB e sicurezza

Le richieste partono da un'applicazione eseguita nel browser. Una credenziale inserita nel bundle frontend deve quindi essere considerata pubblica: spostarla soltanto in un file `environment` Angular non la rende segreta.

Per un utilizzo reale è opportuno:

1. non committare chiavi personali;
2. sostituire qualsiasi chiave già pubblicata;
3. inoltrare le richieste attraverso un backend controllato, se la credenziale deve rimanere riservata.

## Stato del progetto

Progetto didattico funzionante e in evoluzione. Login e autenticazione reale non sono ancora implementati.

## Attribuzione

I dati cinematografici provengono da [The Movie Database](https://www.themoviedb.org/). LabTV è un progetto educativo e non è affiliato a TMDB.

## Autore

Sviluppato da [Fabio Zagaria](https://github.com/fabiozagaria).
