# Liquid Saffire 56 su Mac Apple Silicon (M5) — IN PAUSA

**In pausa dal 6 novembre 2026.** Si riprende quando arriva il Mac nuovo.

## Situazione
- Il "Saffire Pro 56" è il **Focusrite Liquid Saffire 56**: un'interfaccia FireWire con chip DICE, model ID `0x000006`.
- I Mac M5 non hanno la porta FireWire. macOS 26 Tahoe ha tolto del tutto il supporto FireWire, e Focusrite non sviluppa più i Saffire.
- Esiste già un driver open source: **ASFireWire** (https://github.com/mrmidi/ASFireWire, licenza Apache-2.0, versione 0.6.0 al momento del controllo).
  - Il Liquid Saffire 56 è nel catalogo e usa il profilo DICE generico, ma **nessuno l'ha mai provato sull'hardware**.
  - Il profilo dedicato al Liquid 56 non esiste ancora: c'è solo un segnaposto in `ASFWDriver/DeviceProfiles/Audio/Definitions/Focusrite.hpp`.
  - Modelli Focusrite simili che funzionano: Saffire Pro 24, Pro 24 DSP e Pro 40 con chip TCD2220. Il Pro 40 con chip TCD3070 non suona ancora (issue #185).

## Da comprare
Adattatore Apple da Thunderbolt 3 (USB-C) a Thunderbolt 2, adattatore Apple da Thunderbolt a FireWire 800, cavo da FireWire 800 a FireWire 400.

## Quando arriva il Mac
1. Installa la build firmata di ASFireWire (istruzioni su asfw.net/install).
2. Collega il Saffire con il volume basso e prova riproduzione e registrazione.
3. Se non funziona, esporta i log dall'app di ASFireWire (sezione System Logs).
4. Con i log si scrive il profilo dedicato al Liquid Saffire 56 in un fork, e poi lo si propone al progetto principale.
