# Changelog

Tutte le modifiche rilevanti al progetto sono documentate in questo file.

Il formato segue [Keep a Changelog](https://keepachangelog.com/it/1.0.0/),
e il progetto aderisce a [Semantic Versioning](https://semver.org/lang/it/).

## [Unreleased]

### Aggiunto
- **Finitura superficiale** - Supporto per finiture Gold (ENIG) e Silver
  - Pulsanti di selezione rapida nel pannello Vista
  - Dropdown nel pannello Layer
  - Finitura visibile anche in modalita "Solo Rame"
  - Default impostato su Gold
- **Supporto Gerber X2** - Parsing degli attributi TF.FileFunction per riconoscimento automatico layer
- **Layer interni** - Supporto per PCB multilayer (G1-G6, inner layers)
- **Misurazione distanze** - Tool per misurare distanze punto-punto in mm
- **DRC base** - Design Rule Check per verifica regole di progettazione
- **Netlist** - Estrazione e visualizzazione delle net dal PCB
- **Rotazione nella toolbar** - Pulsanti 0/90/180/270 gradi
- **Modalita Solo Rame** - Visualizza solo i layer di rame

### Modificato
- **Rendering migliorato** - Sistema di rendering 2D riscritto per maggiore accuratezza
- **Via pad ottimizzati** - Ridotto lo spessore del bordo da 0.15mm a 0.05mm
- **Interfaccia layer** - Pannello layer riorganizzato con toggle e controlli integrati
- **Ordine rendering** - Finitura superficiale ora renderizzata sopra la solder mask

### Rimosso
- **Vista 3D** - Rimossa in favore del rendering 2D ottimizzato
- **Dual side view** - Rimossa la vista affiancata top/bottom
- **Esportazione SVG** - Rimossa, mantenuta solo esportazione PNG
- **Finitura HASL** - Rimossa, mantenute solo Gold e Silver

## [1.0.0] - 2025-01-17

### Aggiunto
- Visualizzatore Gerber RS-274X completo
- Supporto Excellon drill con slot (G85)
- Rendering solder mask semi-trasparente
- Gestione layer con toggle visibilita
- Viste predefinite Top/Bottom/All
- Colori PCB: verde, blu, rosso, nero, bianco, viola
- Zoom, pan e navigazione
- Caricamento drag & drop
- Supporto archivi ZIP
- Esportazione PNG
- Statistiche PCB (dimensioni, fori, tool)
- Interfaccia dark theme
- 100% client-side, nessun server richiesto

---

## Tipi di Modifiche

- `Aggiunto` per nuove funzionalita
- `Modificato` per modifiche a funzionalita esistenti
- `Deprecato` per funzionalita che saranno rimosse
- `Rimosso` per funzionalita rimosse
- `Corretto` per bug fix
- `Sicurezza` per vulnerabilita
