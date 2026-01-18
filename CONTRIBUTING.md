# Contribuire a Gerber Viewer Pro

Grazie per il tuo interesse nel contribuire a questo progetto! Ogni contributo e benvenuto.

## Come Contribuire

### Segnalare Bug

Se trovi un bug, apri una [Issue](https://github.com/quakef4/Visualizzatore-Gerber-web/issues) includendo:

1. **Descrizione** - Cosa e successo e cosa ti aspettavi
2. **Riproduzione** - Passi per riprodurre il problema
3. **File di esempio** - Se possibile, allega il file Gerber che causa il problema
4. **Browser** - Nome e versione del browser usato
5. **Screenshot** - Se utile a capire il problema

### Proporre Nuove Funzionalita

Prima di implementare una nuova funzionalita:

1. Apri una Issue per discuterne
2. Descrivi il caso d'uso e i benefici
3. Attendi feedback prima di iniziare lo sviluppo

### Inviare Pull Request

1. **Fork** il repository
2. **Crea un branch** per la tua modifica:
   ```bash
   git checkout -b feature/nome-feature
   # oppure
   git checkout -b fix/nome-bug
   ```
3. **Fai le modifiche** seguendo le linee guida sotto
4. **Testa** le modifiche in diversi browser
5. **Commit** con messaggi descrittivi:
   ```bash
   git commit -m "Add: descrizione della nuova feature"
   git commit -m "Fix: descrizione del bug risolto"
   ```
6. **Push** e apri una Pull Request

## Linee Guida per il Codice

### Struttura

Il progetto usa un'architettura single-file (`index.html`) per semplicita di distribuzione. Mantieni questa struttura.

### Stile JavaScript

- **ES6+** - Usa sintassi moderna (const, let, arrow functions, template literals)
- **Naming** - camelCase per variabili e funzioni, PascalCase per classi
- **Commenti** - Commenta solo logica complessa, il codice dovrebbe essere auto-esplicativo
- **Funzioni** - Mantieni le funzioni brevi e con singola responsabilita

```javascript
// Buono
const calculateDistance = (p1, p2) => {
    const dx = p2.x - p1.x;
    const dy = p2.y - p1.y;
    return Math.sqrt(dx * dx + dy * dy);
};

// Evita
function calc(a, b) {
    return Math.sqrt((b.x-a.x)*(b.x-a.x)+(b.y-a.y)*(b.y-a.y));
}
```

### Stile CSS

- **Variabili CSS** - Usa le variabili definite (--bg, --surface, --accent, etc.)
- **BEM-like** - Nomi descrittivi (.panel-header, .layer-toggle, .btn-primary)
- **Mobile-first** - Considera la responsivita

### Performance

- **Canvas** - Minimizza le operazioni di draw, usa batch quando possibile
- **Memory** - Evita memory leak, pulisci listener e riferimenti
- **Parsing** - Il parsing Gerber puo essere pesante, evita operazioni inutili

## Testing

Prima di inviare una PR, testa:

1. **Caricamento file** - Prova con diversi file Gerber/Excellon
2. **Browser** - Chrome, Firefox, Safari, Edge
3. **Funzionalita** - Zoom, pan, layer toggle, esportazione
4. **Edge cases** - File vuoti, file malformati, file molto grandi

### File di Test

Puoi usare i file nella cartella `examples/` o generare file di test con software come KiCad, Eagle, o Altium.

## Struttura del Codice

```
GerberViewer class
├── Constructor
│   ├── Canvas setup
│   ├── State initialization
│   └── Event binding
├── File handling
│   ├── loadFiles()
│   ├── extractZip()
│   └── parseFile()
├── Parsing
│   ├── parseGerber()
│   ├── parseDrill()
│   └── detectLayerType()
├── Rendering
│   ├── render()
│   ├── renderLayer()
│   ├── renderSolderMask()
│   ├── renderSurfaceFinish()
│   └── renderDrillLayer()
├── Tools
│   ├── Measurement
│   ├── DRC
│   └── Netlist
└── UI
    ├── updateUI()
    ├── updateLayerList()
    └── Export functions
```

## Domande?

Se hai domande, apri una Issue con il tag `question`.

Grazie per contribuire!
