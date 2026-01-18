# Gerber Viewer Pro

Un visualizzatore di file Gerber e Excellon moderno, leggero e completamente client-side. Nessun server richiesto, funziona direttamente nel browser.

![Gerber Viewer Screenshot](screenshot.png)

## Caratteristiche

### Rendering PCB
- **100% Client-Side** - Nessun upload su server, i tuoi file rimangono sul tuo computer
- **Supporto formati multipli** - Gerber RS-274X, Gerber X2, Excellon drill, file ZIP
- **Rendering accurato** - Supporto completo per aperture C, R, O, P e macro
- **Solder mask realistica** - Rendering semi-trasparente con aperture pad
- **Fori e slot** - Supporto completo per drill e fori ovali (G85)
- **Layer interni** - Supporto PCB multilayer (fino a 6+ layer)

### Finitura Superficiale
- **Gold (ENIG)** - Finitura oro per pad esposti
- **Silver** - Finitura argento immersion
- **Selezione rapida** - Pulsanti Oro/Argento nel pannello Vista
- **Layer dedicato** - Visibile anche in modalita "Solo Rame"

### Strumenti di Analisi
- **Misurazione distanze** - Click per punti, visualizza distanza in mm
- **DRC (Design Rule Check)** - Verifica regole di progettazione base
- **Netlist** - Estrazione e visualizzazione delle net
- **Statistiche** - Dimensioni scheda, conteggio fori, tabella tool

### Visualizzazione
- **Viste predefinite** - Top, Bottom, Tutti i layer
- **Gestione layer** - Mostra/nascondi singoli layer
- **Colori PCB** - Verde, blu, rosso, nero, bianco, viola
- **Rotazione** - 0°, 90°, 180°, 270°
- **Solo Rame** - Visualizza solo i layer di rame
- **Zoom e Pan** - Navigazione fluida con mouse

### Esportazione
- **PNG** - Esporta l'anteprima come immagine ad alta risoluzione

## Demo

Apri `index.html` nel tuo browser oppure visita: [GitHub Pages Demo](https://quakef4.github.io/Visualizzatore-Gerber-web/)

## Formati Supportati

### Gerber RS-274X / X2
| Estensione | Descrizione |
|------------|-------------|
| `.gtl` | Top Copper |
| `.gbl` | Bottom Copper |
| `.g1` - `.g6` | Inner Layers |
| `.gts` | Top Solder Mask |
| `.gbs` | Bottom Solder Mask |
| `.gto` | Top Silkscreen |
| `.gbo` | Bottom Silkscreen |
| `.gtp` | Top Paste |
| `.gbp` | Bottom Paste |
| `.gko` / `.gm1` | Board Outline |
| `.gbr` / `.ger` | Generic Gerber |

### Excellon Drill
| Estensione | Descrizione |
|------------|-------------|
| `.drl` | Drill file |
| `.xln` | Drill file (alternativo) |
| `.txt` | Drill file (se formato Excellon) |

### Archivi
| Estensione | Descrizione |
|------------|-------------|
| `.zip` | Archivio contenente file Gerber/Drill |

## Utilizzo

### Caricamento File
1. **Drag & Drop** - Trascina i file Gerber/Excellon nell'area di drop
2. **Click** - Clicca sull'area per aprire il file browser
3. **ZIP** - Carica un archivio ZIP contenente tutti i file

### Navigazione
- **Zoom** - Rotella del mouse o pulsanti +/-
- **Pan** - Trascina con il mouse
- **Fit** - Pulsante per adattare alla finestra
- **Rotazione** - Pulsanti 0°/90°/180°/270° nella toolbar

### Misurazione
1. Clicca sul pulsante "Misura" nella toolbar
2. Clicca sul primo punto
3. Clicca sul secondo punto
4. La distanza viene mostrata in mm
5. ESC o click destro per annullare

### Finitura Superficiale
- Seleziona **Oro** o **Argento** dai pulsanti nel pannello Vista
- Oppure usa il dropdown nel pannello Layer
- La finitura viene applicata ai pad esposti dalla solder mask

### DRC (Design Rule Check)
1. Clicca su "DRC" nella toolbar
2. Vengono verificate le regole base di progettazione
3. I risultati mostrano eventuali violazioni

## Installazione

### Opzione 1: Uso diretto
Scarica `index.html` e aprilo nel browser. Fine!

### Opzione 2: GitHub Pages
1. Fai fork di questo repository
2. Vai su Settings > Pages
3. Seleziona branch `main` e cartella `/ (root)`
4. Il viewer sara disponibile su `https://tuousername.github.io/Visualizzatore-Gerber-web/`

### Opzione 3: Server locale
```bash
# Con Python
python -m http.server 8000

# Con Node.js
npx serve .

# Con PHP
php -S localhost:8000
```

## Tecnologie

- **HTML5 Canvas** - Rendering 2D ad alte prestazioni
- **JavaScript ES6+** - Logica applicativa moderna
- **JSZip** - Estrazione archivi ZIP (via CDN)
- **CSS3** - Interfaccia dark theme responsive

## Struttura del Progetto

```
Visualizzatore-Gerber-web/
├── index.html      # Applicazione completa (single-file)
├── README.md       # Documentazione
├── CHANGELOG.md    # Storico delle modifiche
├── CONTRIBUTING.md # Guida per i contributori
├── LICENSE         # Licenza MIT
├── screenshot.png  # Screenshot demo
└── examples/       # File di esempio
    └── README.md
```

## Browser Supportati

| Browser | Versione Minima |
|---------|-----------------|
| Chrome | 80+ |
| Firefox | 75+ |
| Safari | 13+ |
| Edge | 80+ |

## Problemi Noti

- Alcune aperture macro molto complesse potrebbero non renderizzare correttamente
- File Gerber con formati non standard potrebbero richiedere aggiustamenti manuali
- La performance puo degradare con PCB molto complessi (>100k elementi)

## Contribuire

Le pull request sono benvenute! Consulta [CONTRIBUTING.md](CONTRIBUTING.md) per le linee guida.

## Licenza

[MIT](LICENSE) - Sentiti libero di usare questo progetto come preferisci.

## Crediti

Sviluppato con passione per la community dei maker e progettisti PCB.

---

**Nota**: Questo viewer e pensato per anteprime rapide e verifica visiva. Per la produzione, usa sempre i file Gerber originali e verifica con il tuo produttore PCB.
