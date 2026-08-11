# LabTV — Catalogo cinematografico Angular

Single Page Application dedicata alla scoperta di film. Integra la TMDB API per mostrare catalogo, ricerca, dettagli, cast, regista e titoli simili.

[Demo online](https://lab-tv.vercel.app/)

## Stato del progetto

**Sospeso temporaneamente.** Lo sviluppo riprenderà dopo il completamento del [Gestionale Spese](https://github.com/fabiozagaria/expense-tracker-angular). La demo resta disponibile, ma LabTV non è ancora considerato concluso.

## Competenze dimostrate

- integrazione di una REST API esterna;
- gestione asincrona dei dati con HttpClient e RxJS;
- modelli TypeScript per risposte API tipizzate;
- gestione degli stati di caricamento ed errore;
- routing con parametri dinamici;
- componenti riutilizzabili;
- stato locale con Angular Signals.

## Funzionalità

- catalogo di film recuperato dalla TMDB API;
- ricerca locale per titolo;
- pagina di dettaglio del film;
- visualizzazione di cast e regista;
- suggerimenti di film simili;
- messaggi dedicati per caricamento ed errore;
- navigazione tra home, catalogo, ricerca, contatti e dettaglio.

## Tecnologie

- Angular 21
- TypeScript 5.9
- RxJS
- Angular Signals
- Angular Router
- Angular HttpClient
- Bootstrap 5 e Bootstrap Icons
- TMDB API
- Vitest come test runner configurato

## Architettura

`MovieService` centralizza le chiamate HTTP e restituisce `Observable` tipizzati. I componenti separano catalogo, ricerca, card e dettaglio; Signals mantiene lo stato locale dell'interfaccia.

Le rotte principali sono definite in `app.routes.ts`, mentre i modelli condivisi descrivono film, crediti e risposte della API.

## Avvio in locale

### Requisiti

- Node.js in versione LTS
- npm

```bash
git clone https://github.com/fabiozagaria/labtv-angular.git
cd labtv-angular
npm install
npm start
```

L'applicazione sarà disponibile su `http://localhost:4200`.

## Nota architetturale sulle credenziali

In una SPA, ogni configurazione inclusa nel bundle è accessibile dal browser. In un'applicazione production-ready, le chiamate che richiedono credenziali riservate dovrebbero essere mediate da un backend controllato.

## Limiti attuali

- il progetto è esclusivamente frontend;
- la pagina di login è dimostrativa e non implementa autenticazione reale;
- non è presente persistenza utente.

## Attribuzione

I dati cinematografici sono forniti da [The Movie Database](https://www.themoviedb.org/). LabTV è un progetto educativo e non è affiliato a TMDB.

## Autore

Fabio Zagaria — progetto Angular realizzato durante il percorso LabForWeb.
