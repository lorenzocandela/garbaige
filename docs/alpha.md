# GarbAIge: definizione dell'Alpha

Stato: Alpha in definizione. Questo documento descrive cosa si vuole
costruire. Niente di quanto segue è ancora implementato.

## Goal

Un'app desktop che ripulisce lo storico delle chat AI da un posto solo.

- Riunisce per account le conversazioni sparse tra terminale, web e app.
- Indica cosa è spazzatura.
- La cancella alla fonte, dopo averne salvato una copia in locale.

Gira tutto sulla macchina dell'utente. Niente server, niente registrazione.

## Pain

Lo stesso account viene usato da più canali. Lo sporco si accumula sparso
tra disco e server. Oggi si pulisce a pezzi, con strumenti diversi.

Sporco significa:

- chat vecchie
- chat brevissime
- chat senza correlazione con nessun'altra
- chat lontane dagli argomenti che coprono la maggior parte dello storico

## Target

Il dev che usa l'AI come assistente di lavoro e alterna CLI e web sullo
stesso account.

## Architettura

- App desktop Tauri 2. Logica in Rust, interfaccia web.
- Struttura dei dati: provider -> account -> canali.
- Tutti i dati restano in locale.

### Collegamento

1. Clic sull'icona del provider.
2. Login in una finestra dell'app.
3. Il canale web è collegato.
4. Il canale CLI viene trovato sul disco e agganciato allo stesso account.

### Piano B per il web

Se il login in finestra viene bloccato, il canale web passa da
un'estensione browser compagna.

## Analisi

### Cosa si tiene di ogni chat

- Il titolo.
- I messaggi dell'utente.

### Come si confrontano le chat

- Modello di embedding locale e multilingua. Le chat sono miste, italiano
  e inglese.
- Le chat vengono raggruppate in argomenti. Ogni argomento ha un nome.

### Le quattro misure

| Misura | Cosa misura |
| --- | --- |
| Età | Tempo dall'ultimo messaggio. Soglia di default: 1 mese, regolabile nelle impostazioni. |
| Lunghezza | Quanto è corta la chat. |
| Isolamento | Distanza dalla chat più simile. |
| Peso dell'argomento | Quanto pesa il suo argomento sul totale dello storico. |

### Segnali extra

- Sessioni CLI: la cartella di progetto.
- Web: progetti e chat fissate non vanno mai nella fascia "sicure".

### Risultato: tre fasce

- **Sicure.** Più criteri d'accordo. Preselezionate, si approvano con un clic.
- **Probabili.** Raggruppate per motivo o per argomento. Si approva il gruppo.
- **Dubbie.** Segnali in conflitto. Mostrate una per una.

Regola: l'isolamento da solo non porta mai una chat tra le sicure.

## Flusso utente

1. Collega.
2. Scansione e analisi.
3. Riepilogo a fasce.
4. Conferma.
5. Copia locale.
6. Cancellazione alla fonte.

La copia locale viene sempre prima della cancellazione. Senza conferma non
si cancella nulla.

## Perimetro dell'Alpha

- Solo Claude: Claude Code su disco e claude.ai.
- Solo modalità Pulizia.

### Prima incognita tecnica

Da provare prima di tutto il resto, su claude.ai e da dentro l'app:

- login
- lettura dell'elenco chat
- cancellazione

Se non regge, si passa al piano B: l'estensione browser compagna.

## Dopo l'Alpha

Fuori perimetro. Solo elencati.

- Regole di sicurezza complete.
- Licenza e piano a pagamento.
- Modalità Compattazione: distillare lo storico utile, cancellare tutto,
  ricreare poche chat tematiche.
- OpenAI, poi Google.
