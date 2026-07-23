# Un Mare

Brano elettroacustico per **viola**, **tamburo a cornice** e **due attuatori elettromeccanici (exciter)**, composto da **Pietro Barale** nel 2026 in collaborazione con l'esecutore Giulio Romano De Mattia, per l'esame di Composizione Elettroacustica I — Corsi Accademici di Musica Elettronica, Conservatorio "A. Casella" dell'Aquila.

Il brano non prevede altoparlanti tradizionali: il suono, elaborato in tempo reale con Pure Data, viene trasmesso direttamente agli strumenti tramite gli attuatori, che li trasformano simultaneamente in risonatori acustici e diffusori. Due microfoni omnidirezionali generano cicli di feedback elettroacustico controllato, in un principio che dialoga con precedenti storici come *Rainforest* di David Tudor e *I am sitting in a room* di Alvin Lucier.

**Durata:** circa 10–12 minuti, in tre sezioni con configurazioni diverse di routing del segnale e trattamento DSP.

## Ascolto

Registrazioni audio (.wav) del brano disponibili su Mega:
 **[Ascolta le versioni audio di Un Mare](https://mega.nz/folder/trl1DJQD#IUzRp37Xvp70Xevib5CkLQ)**

## Struttura del repository

```
Un_Mare/
├── pure_data/        # Patch Pure Data (Pd-Vanilla)
│   ├── Main.pd         # Patch principale (routing sezioni, timer, uscite)
│   ├── sezione1.pd      # Sezione 1 — routing diretto
│   ├── sezione2.pd      # Sezione 2 — routing incrociato
│   └── sezione3.pd      # Sezione 3 — routing incrociato + diretto combinato
├── docs/             # Tesina d'esame e note di progetto
│   └── Pietro_Barale_UnMare_tesina.pdf
├── img/              # Partitura e materiale visivo
│   └── Pietro_Barale_UnMare_partitura.pdf
└── audio/            # Note sull'ascolto (le tracce audio sono ospitate su Mega, vedi sopra)
```

Ogni cartella (`audio/`, `docs/`, `img/`) contiene un proprio `README.md` con indicazioni sul contenuto.

## Setup tecnico

- 1 viola con attuatore **Visaton EX 30S** (fisso, in prossimità delle "f")
- 1 tamburo a cornice con attuatore **Visaton EX 60R** (mobile sulla membrana)
- 1 mini amplificatore stereo (es. Nobsound NS-01G)
- 2 microfoni omnidirezionali (uno per strumento)
- 1 interfaccia audio: 2 ingressi / 2 uscite, 48 kHz / 24 bit
- 1 laptop con Pure Data e la patch del brano

Il brano è pensato per spazi medio-piccoli e non richiede amplificazione aggiuntiva per il pubblico (salvo diversamente richiesto dallo spazio).

## Struttura del brano

| Sezione | Routing | Durata |
|---|---|---|
| 1 | diretto (ogni strumento in feedback con sé stesso) | 3'00"–4'30" |
| 2 | incrociato (ogni strumento diffonde l'altro) | max 3'30" |
| 3 | incrociato + diretto combinato (buffer lungo verso lo strumento opposto, buffer corto verso lo strumento di provenienza) | max 3'00" |

Il passaggio tra le sezioni è gestito da tastiera del computer con un crossfade audio di 10 secondi. Dettagli completi su DSP, routing e indicazioni per gli esecutori nella tesina in `docs/`.

## Requisiti software

- [Pure Data](https://puredata.info/) (Pd-Vanilla)

## Utilizzo

Aprire `pure_data/Main.pd` con Pure Data per avviare la patch principale. Il passaggio tra le sezioni avviene tramite barra spaziatrice (o un eventuale pedale esterno collegato).

## Documentazione

- **Tesina d'esame** (`docs/Pietro_Barale_UnMare_tesina.pdf`): descrizione generale, setup, analisi sezione per sezione, funzionamento della patch, bibliografia e discografia.
- **Partitura** (`img/Pietro_Barale_UnMare_partitura.pdf`): indicazioni per gli esecutori, schemi di routing per ciascuna sezione.

## Discografia

- Tudor, David. 1968. *Rainforest*.
- Lucier, Alvin. 1969–1970. *I am sitting in a room*.

## Autore

Pietro Barale — in collaborazione con Giulio Romano De Mattia (esecutore)

## Licenza

Questo lavoro è distribuito con licenza [Creative Commons Attribuzione - Non Commerciale - Non Opere Derivate 4.0 Internazionale (CC BY-NC-ND 4.0)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.it). Vedi il file [LICENSE](./LICENSE) per i dettagli.
