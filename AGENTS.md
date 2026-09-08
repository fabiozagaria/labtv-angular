# Istruzioni per assistenti AI

## Scopo
LabTV è una SPA Angular per la scoperta di film tramite TMDB API. La release frontend 1.0.0 è considerata stabile rispetto allo scope attuale.

## Regole operative
- Non trattare il progetto come in sviluppo attivo salvo richiesta esplicita.
- Preservare lo scope frontend della 1.x; backend, account e persistenza appartengono a un'eventuale evoluzione 2.x.
- Leggere `README.md` e `docs/CONTEXT.md` prima di modifiche strutturali.
- Non inserire segreti TMDB o altre credenziali nel bundle/repository.
- Per correzioni, privilegiare compatibilità con la release stabile e regressioni minime.

## Fonti di verità
- Il codice è la verità tecnica.
- `README.md` descrive la release pubblica.
- `docs/CONTEXT.md` chiarisce stato e limiti.
- Roadmap didattica e valutazioni restano in Notion.

## Sicurezza
Le credenziali riservate non devono essere esposte in una SPA pubblica.