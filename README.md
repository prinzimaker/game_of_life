# 🧬 Conway's Game of Life - Infinite Canvas

Un'implementazione moderna, interattiva e performante del famoso **Gioco della Vita di John Conway**, scritta interamente in **JavaScript puro (Vanilla JS)** senza alcuna dipendenza esterna.

Questo progetto utilizza HTML5 Canvas per renderizzare una griglia virtuale ampia, offrendo controlli di navigazione fluidi simili a quelli di una mappa interattiva (Pan & Zoom).

[https://via.placeholder.com/800x400?text=Screenshot+Game+of+Life+Preview](https://github.com/prinzimaker/game_of_life/blob/main/screenshot.png)


## ✨ Caratteristiche Principali

* **Zero Dipendenze:** Funziona su qualsiasi browser moderno semplicemente aprendo il file HTML.
* **Rendering Performante:** Utilizza `requestAnimationFrame` e HTML5 Canvas API.
* **Navigazione Avanzata:**
    * **Zoom Intelligente:** Zoom in/out centrato sulla posizione del cursore del mouse.
    * **Limiti Dinamici:** Lo zoom si adatta per mostrare sempre l'intera area di gioco o un dettaglio minimo di 50 celle.
    * **Panoramica (Pan):** Spostamento fluido della visuale con il tasto destro.
* **Disegno Libero:** Clicca e trascina per "dare vita" alle cellule manualmente.
* **Funzione Memoria:** * 💾 **Salva:** Memorizza lo stato attuale della griglia in una variabile temporanea.
    * 📂 **Carica:** Ripristina istantaneamente l'ultimo stato salvato.
* **UI Minimalista:** Barra di controllo flottante (Dock) con icone intuitive e help visivo integrato.

## 🚀 Come usare

Non è necessaria alcuna installazione, build system o server locale.

1.  Scarica o clona questo repository.
2.  Apri il file `index.html` nel tuo browser preferito (Chrome, Firefox, Edge, Safari).
3.  Inizia a giocare!

## 🎮 Controlli

### Mouse
| Azione | Input |
| :--- | :--- |
| **Disegna / Cancella** | Clic e trascinamento **Tasto Sinistro** |
| **Sposta Visuale** | Clic e trascinamento **Tasto Destro** (o Centrale) |
| **Zoom In / Out** | **Rotella del Mouse** |

### Interfaccia (Dock)
La barra di controllo si trova in basso al centro dello schermo:

* ▶ **Play:** Avvia la simulazione.
* ■ **Stop:** Mette in pausa la simulazione per modificare la griglia.
* 🔀 **Random:** Genera una distribuzione casuale di cellule vive.
* 🗑️ **Clear:** Pulisce l'intera griglia (uccide tutte le cellule).
* 💾 **Save:** Salva la configurazione attuale in memoria.
* 📂 **Load:** Carica la configurazione salvata dalla memoria.

## 🛠️ Dettagli Tecnici

### Griglia Virtuale & Camera
Il gioco simula una griglia virtuale di dimensioni fisse (es. 300x300 celle) che è molto più grande della viewport del browser.
La "telecamera" gestisce la visualizzazione attraverso trasformazioni matriciali 2D:
```javascript
ctx.translate(camera.x, camera.y);
ctx.scale(camera.zoom, camera.zoom);
