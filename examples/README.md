# File di Esempio

Questa cartella può contenere file Gerber di esempio per testare il viewer.

## Dove trovare file Gerber di esempio

- **KiCad** - I progetti KiCad includono spesso file Gerber di esempio
- **PCBWay** - [Sample Gerber Files](https://www.pcbway.com/blog/help_center/Generate_Gerber_file_from_Kicad.html)
- **OSH Park** - Repository di progetti open source
- **GitHub** - Cerca "gerber files example" o "open source pcb"

## Struttura tipica di un pacchetto Gerber

```
progetto-gerber/
├── progetto.GTL          # Top Copper
├── progetto.GBL          # Bottom Copper  
├── progetto.GTS          # Top Solder Mask
├── progetto.GBS          # Bottom Solder Mask
├── progetto.GTO          # Top Silkscreen
├── progetto.GBO          # Bottom Silkscreen
├── progetto.GKO          # Board Outline
└── progetto.DRL          # Drill File
```

## Test rapido

Per testare il viewer, puoi creare un semplice file Gerber manualmente:

```
G04 Simple test file*
%FSLAX24Y24*%
%MOMM*%
%ADD10C,1.0*%
D10*
X0Y0D03*
X10000000Y0D03*
X10000000Y10000000D03*
X0Y10000000D03*
M02*
```

Salva come `test.gbr` e caricalo nel viewer.
