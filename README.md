# MultiModo-boh

Plugin **VST3 gratuito per macOS 11 o successivo su Apple Silicon**.
Chorus, delay multitap e diffusione modulata, con nove modalità e 35 parametri automatizzabili.

![Interfaccia di MultiModo-boh](assets/MultiModo-boh-interface.png)

## Download

[Scarica l'ultima release](https://github.com/vallaproductionsoriginal-byte/MultiModo-boh/releases/latest).

Apri la release e scarica **MultiModo-boh-mac-arm64.zip** dalla sezione **Assets**.
Il pacchetto contiene il plugin compilato, le istruzioni e gli avvisi di licenza.
Questo repository distribuisce il VST3 in forma binaria; il codice sorgente non è pubblicato.

## Installazione

1. Estrai l'archivio ZIP.
2. Copia l'intera cartella `MultiModo-boh.vst3` in `~/Library/Audio/Plug-Ins/VST3/`.
   Crea la cartella `VST3` se non esiste.
3. Riavvia la DAW oppure esegui una nuova scansione dei plugin VST3.

La release richiede una DAW con supporto VST3 eseguita nativamente su Apple Silicon.
Il bundle ha firma ad hoc locale ed è privo di notarizzazione Apple. Se macOS lo blocca
dopo il download da questa release ufficiale, puoi rimuovere l'attributo di quarantena
dal solo bundle installato, poi ripetere la scansione:

```sh
xattr -dr com.apple.quarantine "$HOME/Library/Audio/Plug-Ins/VST3/MultiModo-boh.vst3"
```

## Controlli

Mix, Depth, Width, Delay e Feedback sono sempre disponibili. Le sei pagine raggruppano
i controlli TAPS, MOD, DIFF, TONE, DRIVE e WARP.

- **Mode:** DimD, VP330, SuperSix, 6TapRandom, DualEnsemble, 8Tap, 16Phase, 16Tap e 32Tap.
- **Diffusione e tono:** diffusione modulata, filtri nel feedback, larghezza stereo e drive.
- **Tempo:** delay libero oppure sincronizzato alla DAW, con suddivisioni regolari, puntate e terzine.
- **Dark e Half Speed:** variazioni del colore, dei tempi di delay e della modulazione.
- **Preset:** dieci impostazioni integrate; Save e Load gestiscono file `.multimodo`.
- **Lock mix:** mantiene il valore Mix durante il richiamo dei preset.
- **Automazione:** 35 parametri; supporto mono e stereo.

Un doppio clic su un knob ripristina il valore predefinito. È possibile digitare
i valori nei campi sotto i knob. Lo stato viene salvato nel progetto della DAW.

## Licenza

Le parti originali di MultiModo-boh e la documentazione sono offerte sotto
[licenza MIT](LICENSE). Il download è gratuito.

JUCE 9.0.3 è utilizzato secondo i termini della licenza commerciale **JUCE Starter**.
JUCE e gli altri componenti di terzi mantengono i propri copyright e le rispettive
licenze, descritti in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
La licenza MIT del progetto non modifica le licenze dei componenti di terzi.

## Segnalazioni

Per segnalare un problema, [apri una issue](https://github.com/vallaproductionsoriginal-byte/MultiModo-boh/issues)
indicando versione di macOS, DAW, versione del plugin e passi per riprodurlo.
