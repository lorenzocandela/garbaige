# AGENTS.md

Istruzioni per gli agenti di coding che lavorano in questa repo.

## 1. Contesto

GarbAIge è un'app desktop che ripulisce lo storico delle chat AI da un posto solo.
Riunisce per account le chat sparse tra CLI e web, indica la spazzatura e la cancella alla fonte dopo una copia locale.
Il progetto è in stato "Alpha in definizione": esiste solo la documentazione.

- Definizione dell'Alpha: [docs/alpha.md](docs/alpha.md)
- Linee guida di interfaccia: [docs/design.md](docs/design.md)

Leggi entrambi prima di toccare qualsiasi cosa.

## 2. Perimetro

- Lavora solo sull'Alpha, così come è definita in `docs/alpha.md`.
- Solo Claude: Claude Code su disco e claude.ai.
- Solo modalità Pulizia.
- Non anticipare nulla di ciò che sta nella sezione "Dopo l'Alpha". Niente
  predisposizioni, niente astrazioni pensate per il futuro.

## 3. Vincoli fissi

- Tutto in locale. Nessun dato esce dalla macchina dell'utente.
- Nessuna cancellazione senza conferma esplicita dell'utente.
- Nessuna cancellazione senza copia locale fatta prima.
- Icone: solo Tabler Icons.
- Font: Outfit per i testi, Xmind per i numeri.
- Stack: Tauri 2 + Rust.

## 4. Regole di lavoro

Da definire.
