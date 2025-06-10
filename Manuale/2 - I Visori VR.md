## Introduzione alla VR

La **realtà virtuale (VR)** immerge l’utente in un ambiente digitale tridimensionale generato al computer, sfruttando un visore e sensori di movimento per ricreare la percezione dello spazio reale.  
La VR si distingue dalla realtà aumentata (AR), che sovrappone elementi digitali al mondo reale, e dalla realtà mista (MR), che integra dinamicamente oggetti virtuali con il contesto reale.  

---
## Tipologie di Visori VR [1]
### Visori Stand‑alone
I visori *stand‑alone* racchiudono **tutti i componenti fondamentali** ([[2 - I Visori VR#Glossario|SoC]], GPU, memoria, storage, batteria e sensori di tracciamento) direttamente nell’*head‑mounted display*, eliminando la necessità di un PC esterno o di stazioni base aggiuntive. Questo approccio "*all‑in‑one*" permette un setup ***plug‑and‑play***: basta accendere il visore, indossarlo e iniziare l’esperienza, senza cavi né configurazioni complesse. La **portabilità** è il punto di forza principale, poiché si può utilizzare il dispositivo ovunque serva, aule scolastiche, biblioteche o sale polivalenti, con uno spazio minimo di 2 × 2 m per garantire sicurezza nei movimenti a [[2 - I Visori VR#Glossario|6 DoF]]. In contesti didattici, questo si traduce in una flessibilità operativa ideale per lezioni itineranti o dimostrazioni pratiche in luoghi diversi, senza spostare PC o predisporre lunghe sessioni di installazione.

Dal lato delle prestazioni, i visori *stand‑alone* sono limitati dal **SoC mobile** integrato: pur essendo i chip più recenti in grado di offrire frame rate fino a 90 Hz in 2160 × 2160 pixel per occhio, non raggiungono mai la potenza bruta delle GPU desktop. Di conseguenza, per applicazioni con scene 3D complesse o rendering avanzato (*ray‑tracing*, fisica *real‑time*), le soluzioni *stand‑alone* possono richiedere ottimizzazioni di [[2 - I Visori VR#Glossario|LOD]], render scale ridotto o compressione degli asset. Inoltre, l’**autonomia della batteria** (tipicamente 2–3 ore) vincola la durata delle sessioni, rendendo necessario prevedere pause per la ricarica o l’uso di moduli sostituibili a caldo in contesti prolungati.

---
### Visori Tethered [2]
I visori tethered si basano su un **PC VR‑Ready** esterno che gestisce tutta l’elaborazione grafica e fisica, collegandosi tramite cavo USB‑C, DisplayPort o HDMI, oppure tramite soluzioni wireless ad alta banda che però possono introdurre compressione e latenza. Grazie a GPU desktop con *ray‑tracing* hardware e CPU multi‑core, supportano risoluzioni fino a 4 K e frame rate stabili a 90–120 FPS, garantendo **massima qualità visiva** e dettagli elevati anche in scene molto complesse. Questo li rende ideali per applicazioni che richiedono texture ad alta risoluzione, simulazioni industriali dettagliate o training con dinamiche fisiche avanzate.

Sul fronte pratico, l’installazione di un visore tethered richiede una **postazione fissa** con sensori esterni (per sistemi *outside‑in*) o router/cavi dedicati (per soluzioni wireless ad alte prestazioni), oltre a monitorare il routing dei cavi per evitare vincoli nei movimenti dell’utente. Il peso del visore è spesso inferiore rispetto ai modelli *stand‑alone* perché non incorpora batteria né SoC pesanti, migliorando il comfort nelle sessioni prolungate, ma la **portabilità risulta fortemente ridotta** e il setup più laborioso. In ambito scolastico, i tethered sono adatti a **laboratori dedicati** o sale VR fisse, dove si può contare su un’infrastruttura hardware stabile e su manutenzione centralizzata.

---
## Pico 4 Enterprise - Specifiche Hardware [3]  [4]  [5]
### System-on-a-Chip (SoC) e GPU
Il Pico 4 Enterprise monta un **Qualcomm Snapdragon XR2 Gen 1** a 7 nm con 8 core Kryo, garantendo consumi ottimizzati per VR.  
La GPU integrata è **Adreno 650**, sufficiente per gestire rendering 3D complessi e *[[2 - I Visori VR#Glossario|passthrough]]* avanzato.
### Memoria e Storage
La RAM è **8 GB LPDDR5**, capace di mantenere più applicazioni e texture ad alta risoluzione senza bisogno [[2 - I Visori VR#Glossario|swap]].  
Lo storage interno è **256 GBgood color passthrough**, permettendo l’installazione di decine di applicazioni VR di grandi dimensioni (target di ~1–2 GB per applicazione) e l’archiviazione di asset multimediali.
### Display e Ottiche
- **Dual Fast‑LCD** da 2,56 pollici: 2160 × 2160 pixel per occhio (4320 × 2160 totale), densità di 1200 PPI, refresh rate 72/90 Hz.
- **[[2 - I Visori VR#Glossario|Lenti pancake]]** che riducono lo spessore del visore, migliorano l’uniformità luminosa e abbassano artefatti da Fresnel, con un [[2 - I Visori VR#Glossario|FOV]] diagonale di 105°.
- **Regolazione [[2 - I Visori VR#Glossario|IPD]]** automatica da 62 mm a 72 mm mediante motore interno, o manuale tramite range continuo, per una visione nitida senza eye strain.
### Tracciamento e Sensori
Il tracciamento ***inside‑out* a 6 DoF** è affidato a quattro videocamere integrate, che mappano l’ambiente circostante e i controller con latenza <20 ms.  
Sono presenti ***eye‑tracking*** (due fotocamere [[2 - I Visori VR#Glossario|IR]]) e ***face‑tracking*** (due fotocamere IR), utili per avatar espressivi e metriche di attenzione .
### Batteria e Ricarica
La batteria è da **5300 mAh** (Li‑ion), garantendo 2–3 ore di autonomia in base al carico grafico e audio.  
Supporta **Qualcomm Quick Charge 3.0** a 20 W via porta USB‑C, ricaricandosi da 0 a 100% in circa 2 ore, o in 60 min per il 70%.  
La batteria è **sostituibile a caldo**: in contesti enterprise consente sessioni prolungate semplicemente scambiando moduli carichi.
### Dimensioni e Peso
- **Dimensioni**: 255–310 mm × 195 mm × 106 mm (testa + strap regolabile).
- **Peso**: 591 g (300 g senza cinturino), con distribuzione anteriore ([[2 - I Visori VR#Glossario|HMD]]) e posteriore (batteria) per bilanciamento comfort.
- **Custodia**: inclusa una valigetta rigida con scomparti sagomati per visore, controller e accessori.

---
## Privacy, Sicurezza e GDPR
Il tracciamento oculare e facciale genera dati biometrici sensibili è obbligatorio:
- raccogliere **consenso esplicito** via moduli digitali
- anonimizzare e criptare i log su server Https/TLS

---
## Glossario
- **SoC (System-on-a-chip):** è un chip con tutte le componenti base di un pc.
- **6DoF (6 Degrees of Freedom)**: sono i 6 gradi di libertà e si riferiscono ai movimenti lungo i tre assi (X, Y, Z) e le rotazioni yaw (asse verticale passante per il baricentro), pitch (asse trasversale passante per il baricentro), roll (asse longitudinale passante per il baricentro).
- **LOD (Level of Detail)**: complessità della rappresentazione di un modello 3D, che in alcuni casi può essere diminuita man mano che chi visualizza una certa scena si allontana da alcuni oggetti.
- **Passthrough**: modalità che mostra l’ambiente reale tramite le fotocamere del visore, utile per interazioni miste fra realtà e VR.
- **Swap:** lo swap è un'estensione della RAM presente su un altro dispositivo di memoria. 
- **FOV**: campo visivo, angolo di visione, indica quanto “avvolgente” è l’immagine.
- **Lenti pancake**: lenti sottili che piegano il percorso ottico, riducendo ingombro frontale.
- **IPD (Interpupillary Distance)**: distanza tra le pupille degli occhi, parametro critico per evitare distorsioni e affaticamento visivo.
- **IR (Infrared):** Infrarossi.
- **HMD (Head-Mounted Display):** display del Visore

---
Riferimenti:
[1] *Wireless VR vs tethered VR: which is best for you?* Android Authority. https://www.androidauthority.com/wireless-vr-vs-tethered-vr-677648
[2]  *Tethered Headsets: Exploring the Pros and Cons.* HOTVRSTUFF. https://www.hotvrstuff.com/vr-headset-types-tethered-headsets
[3] *PICO 4.* Pico. https://www.picoxr.com/global/products/pico4/specs
[4] *PICO 4.* Wikipedia. https://en.wikipedia.org/wiki/PICO_4
[5] *PICO 4.* pny. https://www.pny.com/file%20library/company/support/product%20brochures/pico/pico-4/english/pico4e-pny.pdf


