<h1 align="center">GarbAIge</h1>

<p align="center">
  <em>Le tue chat AI, senza la spazzatura.</em>
</p>

<p align="center">
  <strong>Stato: Alpha in definizione.</strong> Non c'è ancora codice.
</p>

---

## cos'è

Un'app desktop che ripulisce lo storico delle chat AI da un posto solo.

Riunisce per account le conversazioni sparse tra terminale, web e app.
Indica cosa è spazzatura. La cancella alla fonte, dopo averne salvato una
copia in locale.

Gira tutto sulla tua macchina. Niente server, niente registrazione.

## il problema

Usi lo stesso account da più canali. Lo sporco si accumula in due posti:
sul disco e sui server del provider. Oggi si pulisce a pezzi, con strumenti
diversi.

Per sporco si intende:

- chat vecchie
- chat brevissime
- chat senza correlazione con nessun'altra
- chat lontane dagli argomenti che coprono la maggior parte dello storico

## come funziona

1. **Collega.** Clic sull'icona del provider, login in una finestra dell'app.
   Il canale CLI viene trovato sul disco e agganciato allo stesso account.
2. **Scansione e analisi.** L'app legge lo storico e lo misura in locale.
3. **Riepilogo.** Le chat arrivano divise in tre fasce: sicure, probabili,
   dubbie.
4. **Conferma.** Decidi tu cosa va via. Niente viene cancellato senza una
   conferma esplicita.
5. **Copia e cancella.** Prima la copia in locale, poi la cancellazione alla
   fonte.

## per chi

Per il dev che usa l'AI come assistente di lavoro e alterna CLI e web sullo
stesso account.

## stato del progetto

Alpha in definizione.

Esiste solo la documentazione. Nessuna funzione è implementata, nessuna
versione è scaricabile.

L'Alpha copre solo Claude: Claude Code su disco e claude.ai. Una sola
modalità: Pulizia.

La prima incognita tecnica è ancora da provare: login, lettura dell'elenco
chat e cancellazione su claude.ai da dentro l'app.

## documenti

- [docs/alpha.md](docs/alpha.md): definizione completa dell'Alpha.
- [docs/design.md](docs/design.md): linee guida di interfaccia.
- [AGENTS.md](AGENTS.md): istruzioni per gli agenti di coding.
