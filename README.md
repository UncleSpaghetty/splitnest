# SplitNest

**SplitNest** è un'app mobile per la gestione delle spese condivise tra coinquilini. Permette a gruppi di persone che vivono insieme di tracciare chi ha pagato cosa, calcolare i saldi reciproci e organizzare i rimborsi in modo semplice e trasparente.

## Repo del progetto

Questo repository è il **monorepo radice** che raccoglie tutti i sottomoduli del progetto SplitNest.

| Sottomodulo | Descrizione |
|---|---|
| [`splitnest-fe`](./splitnest-fe/) | App mobile React Native / Expo (iOS + Android) |
| [`splitnest-be`](./splitnest-be/) | Backend Django REST API |
| [`splitnest-infra`](./splitnest-infra/) | Configurazione infrastruttura (IaC, deploy, CI/CD) |
| [`splitnest-docs`](./splitnest-docs/) | Documentazione funzionale e tecnica del prodotto |

## Avvio rapido

```bash
# Clona il monorepo con tutti i sottomoduli
git clone --recurse-submodules git@github.com:UncleSpaghetty/splitnest.git

# Avvia il backend
cd splitnest-be
cp .env.example .env
docker compose up --build

# Avvia il frontend
cd ../splitnest-fe
npm install
npx expo start
```

## Funzionalità principali

- Creazione e gestione di case condivise
- Aggiunta e suddivisione di spese tra i membri
- Calcolo automatico dei saldi e suggerimenti di rimborso ottimizzati
- Invito dei coinquilini tramite token
- Pagamenti ricorrenti (affitto, bollette, ecc.)
- Piano gratuito con pubblicità e piano premium tramite paywall
