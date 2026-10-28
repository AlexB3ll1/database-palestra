# Progettazione database — gestione palestra

**Tipologia:** progetto personale di modellazione dati  
**Tecnologie e strumenti documentati:** modello entità-relazione (ER), schema logico relazionale, diagrammi di attività/UML, Dia

## Obiettivo

Progettare la struttura informativa di un sistema dedicato alla gestione di una palestra/centro sportivo, considerando utenti, allenatori, lezioni, prenotazioni, abbonamenti e certificati medici.

## Materiale disponibile

| File | Contenuto |
| --- | --- |
| `schema ER.png` / `schema ER.dia` | Diagramma concettuale entità-relazione |
| `schema logico.png` / `schema logico.dia` | Tabelle, attributi e relazioni dello schema relazionale |
| `UML_progetto_boxe.png` / `UML_progetto_boxe.dia` | Flusso operativo e decisionale legato a prenotazioni e gestione utenti |

Le versioni `.png` consentono di consultare i diagrammi senza software aggiuntivi; le versioni `.dia` possono essere aperte/modificate con [Dia](https://wiki.gnome.org/Apps/Dia) o strumenti compatibili.

## Tabelle presenti nello schema logico

- **Utente allenatore:** dati identificativi e di accesso dell'allenatore.
- **Lezioni:** allenatore associato, orario di inizio, posti disponibili e verifica delle presenze.
- **Prenotazione:** associa una lezione a un atleta e ne registra stato e mancata partecipazione.
- **Abbonamento:** associazione all'atleta con date di inizio e fine, stato e corso.
- **Atleta:** informazioni anagrafiche e credenziali.
- **Certificato medico:** atleta, stato, file, scadenza e tipologia di certificato.

Nello schema sono rappresentate le chiavi identificative e alcune relazioni tramite chiavi esterne, per esempio dalle prenotazioni verso atleti e lezioni.

## Flussi modellati

Il diagramma UML descrive passaggi e decisioni relativi all'accesso degli utenti, alla richiesta e cancellazione di prenotazioni, alla verifica dei posti e alle attività amministrative relative a fasce e presenze. La documentazione riguarda il **disegno del sistema**, non un'interfaccia software già funzionante.

## Come consultare il progetto

1. Aprire `schema ER.png` per osservare le entità e le relazioni concettuali.
2. Aprire `schema logico.png` per analizzare le tabelle e i riferimenti tra i record.
3. Aprire `UML_progetto_boxe.png` per seguire i flussi di gestione e prenotazione.
4. Usare le copie `.dia` per modificare i diagrammi.

## Stato e limiti

**Nell'archivio esaminato non sono presenti script `.sql`, database esportati, applicazioni o query eseguibili.** Non è quindi corretto descrivere il progetto pubblicato come un database SQL implementato e testato: la parte verificabile è la **progettazione**.

Sviluppi successivi possibili: DDL SQL (`CREATE TABLE` e vincoli), dati di prova non personali, query d'esempio, normalizzazione motivata, indici e politiche di gestione sicura delle credenziali e dei dati medici.

## Competenze illustrate

Analisi dei requisiti, rappresentazione concettuale dei dati, modellazione relazionale e rappresentazione dei processi mediante diagrammi UML.
