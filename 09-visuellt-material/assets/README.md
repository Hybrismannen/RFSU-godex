# Genererade visuella assets

Alla kärnvisualer i denna katalog byggs automatiskt från samma projektmodell.

- `projektdashboard.svg` — kanonisk publik dashboard
- `uppdraget-i-korthet.svg` — uppdragets komprimerade helhetsbild
- `urvalsprocess.svg` — register → grundkrav → relevans → palett → dialog → tre case
- `analysmodell.svg` — struktur → praktik → mekanism → hinder/möjliggörare → överförbarhet → rekommendation
- `arbetsprocess.svg` — WP- och leveranslogik

## Regel

Dessa filer ska **inte handredigeras**.

~~~text
källkontrollerad projektstatus
        ↓
automatisk validering
        ↓
RFSU-profilerad rendering
        ↓
publik whitelist
        ↓
SVG-assets
~~~

Varje SVG har titel/beskrivning för tillgänglighet och en textmotsvarighet i samarbetsytan.
