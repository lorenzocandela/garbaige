# agents.md

Istruzioni per gli agenti di coding che lavorano in questa repo.

## 1. contesto

GarbAIge è un'app desktop che ripulisce lo storico delle chat AI da un posto solo.
Riunisce per account le chat sparse tra CLI e web, indica la spazzatura e la cancella alla fonte dopo una copia locale.
Il progetto è in stato "Alpha in definizione": esiste solo la documentazione.

- Definizione dell'Alpha: [docs/alpha.md](docs/alpha.md)
- Linee guida di interfaccia: [docs/design.md](docs/design.md)

Leggi entrambi prima di toccare qualsiasi cosa.

## 2. perimetro

- Lavora solo sull'Alpha, così come è definita in `docs/alpha.md`.
- Solo Claude: Claude Code su disco e claude.ai.
- Solo modalità Pulizia.
- Non anticipare nulla di ciò che sta nella sezione "Dopo l'Alpha". Niente
  predisposizioni, niente astrazioni pensate per il futuro.

## 3. vincoli fissi

- Tutto in locale. Nessun dato esce dalla macchina dell'utente.
- Nessuna cancellazione senza conferma esplicita dell'utente.
- Nessuna cancellazione senza copia locale fatta prima.
- Icone: solo Tabler Icons.
- Font: Outfit per i testi, [Xmind](https://fonts.google.com/specimen/Xmind) per i numeri.
- Stack: Tauri 2 + Rust.

## 4. regole di lavoro

codice
- Indentazione: sempre 4 spazi. Mai tab, mai 2 spazi.
- Mai commenti nel codice.
- Codice pulito e ottimizzato: niente codice morto, niente duplicazioni,
  niente log di debug lasciati in giro.
- Mai emoji, da nessuna parte: codice, interfaccia, testi, commit,
  documentazione.
- Icone: sempre e solo Tabler Icons.
- Titoli e intestazioni sempre in minuscolo, e solo nei file md.
  Nel codice mai titoli, banner o separatori di sezione.
- Solo caratteri normali da tastiera. Vietati i caratteri tipografici
  tipici dei testi generati: punto mediano (·) al posto del trattino,
  trattino lungo (— e –), puntini di sospensione come carattere unico (…),
  virgolette curve (“ ” ‘ ’), frecce e simboli decorativi (→ ✓ •).
  Usa - ... " ' e basta. Vale per codice, interfaccia, commit e documenti.

git
- Messaggi di commit sempre tutti in minuscolo: git commit -m "..."
- Puoi arrivare fino al commit. Il push lo fa sempre e solo Lorenzo.
  Mai git push, per nessun motivo e con nessun metodo.
- Nessuna firma nei commit: niente Co-Authored-By, niente trailer,
  niente riferimenti ad agenti o sessioni. I commit devono sembrare
  scritti da un dev che lavora da solo.

verifiche
- I controlli grafici e i bug visivi del frontend li fa Lorenzo, non tu.
  Non aprire browser, non fare screenshot, non dichiarare che
  l'interfaccia funziona.
- Quando tocchi l'interfaccia, chiudi il lavoro con un elenco breve di
  cosa deve controllare lui e dove, e aspetta la sua risposta.
