# GarbAIge: linee guida di design

Nota: da rivedere in fase di sviluppo.

## stile

App desktop pulita. Riferimento: Opal, l'app di screen time
([opal.so](https://opal.so)). Riferimento di stile, non di funzioni.

- Scuro.
- Tanta aria.
- Pochi elementi per schermata.
- Numeri grandi.

## tema

Solo dark. Non esiste un tema chiaro.

## font

Da Google Fonts.

| Uso | Font |
| --- | --- |
| Testi | Outfit |
| Numeri | [Xmind](https://fonts.google.com/specimen/Xmind) |

## icone

Solo Tabler Icons. Mai altre librerie, mai emoji.

## colori

Base: VS Code Dark.

| Ruolo | Valore |
| --- | --- |
| Sfondo | `#1e1e1e` |
| Pannelli | `#252526` |
| Superfici | `#2d2d30` |
| Bordi | `#3c3c3c` |
| Testo | `#d4d4d4` |
| Testo secondario | `#9d9d9d` |
| Accento | `#569cd6` |

### fasce

| Fascia | Valore |
| --- | --- |
| Sicure | `#4ec9b0` |
| Probabili | `#dcdcaa` |
| Dubbie | `#ce9178` |
| Elimina | `#f48771` |

Sempre con etichetta o icona. Mai solo colore.

## spaziatura

Griglia a 4px. Valori ammessi: 4, 8, 12, 16, 24, 32, 48.

## raggi

| Elemento | Raggio |
| --- | --- |
| Controlli | 8 |
| Card | 12 |
| Finestre e modali | 16 |
| Tag | pillola |

## movimento

- Transizioni tra 150 e 200 ms.
- Nessuna animazione decorativa.

## regole d'uso

- Il rosso solo sull'azione di cancellare.
- Una sola azione principale per schermata.
