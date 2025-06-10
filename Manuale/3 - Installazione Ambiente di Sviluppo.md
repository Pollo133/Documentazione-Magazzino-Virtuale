## Installazione di SimLab Composer
SimLab Composer è un software professionale per la creazione di scene 3D, rendering, VR e animazioni. È disponibile in versione gratuita con funzionalità limitate e in versioni a pagamento con funzionalità complete.

>**NOTA BENE**
>Per la modifica del Magazzino VR è richiesta la versione **11.1.22** di **SimLab Composer**.
>Tutte le modifiche dovranno essere fatte con la versione **con licenza** (a pagamento) del software, in quanto **ogni file aperto con la versione gratuita non potrà più essere utilizzato e modificato nella versione a pagamento.**

Per installare SimLab Composer seguire i seguenti passaggi:
- Visitare il [sito ufficiale di SimLab Composer](https://www.simlab-soft.com/3d-products/simlab-composer-old-download.aspx).
- Selezionare la versione corretta di SimLab Composer: la 11.1.22.
![[SimLabComposer11Download.png]]
- Scaricare ed eseguire il file.
- Seguire il processo d'installazione (non sono richiesti particolari impostazioni).

Una volta completata l'installazione, potrai avviare SimLab Composer e iniziare a utilizzarlo.

> **NOTA BENE**
> La versione gratuita (abilitata di default) offre funzionalità di base ed è ideale per la valutazione iniziale. Alcune funzionalità avanzate (come il rendering in alta qualità o l'esportazione in determinati formati) richiedono una licenza a pagamento.
> La versione di prova ha una durata limitata (generalmente 21 o 30 giorni).
### Requisiti di sistema
#### Windows
- **Processore:** Quad-core Intel o AMD 2.5 GHz o superiore
- **RAM:** Minimo 4 GB
- **Scheda grafica:** Qualsiasi scheda con almeno 1 GB di memoria (dedicata o condivisa)
- **Spazio su disco:** 4 GB liberi
- **Risoluzione monitor:** 1440 × 900 o superiore    
- **Sistema operativo:** Windows 10 o 11 (64-bit)
#### macOS
- **Processore:** Intel-based o Apple Silicon (con Rosetta 2)
- **RAM**: Minimo 4 GB
- **Spazio su disco:** 4 GB liberi
- **Risoluzione monitor:** 1440 × 900 o superiore
- **Sistema operativo:** macOS 12.0 o superiore (per Composer 12)

---
## Installazione di SimLab Viewer
SimLab Viewer consente di visualizzare i progetti creati con SimLab Composer, inclusi modelli 3D e scene VR.

> **NOTA BENE**
> Con i seguenti passaggi verrà installata l'**ultima versione** di SimLab Viewer.
> Nonostante la **versione** del visualizzatore **non corrisponda** con quella del composer sarà **comunque possibile visualizzare** tramite il PC il magazzino.
> Si potrebbero però riscontrare problemi nel caso si volesse far funzionare il visore tramite Steam VR e questa versione del Viewer, in quanto **potrebbe non corrispondere a quella installata sul visore**.
> Purtroppo SimLab **non mette a disposizione** i download delle **versioni passate** del Viewer.

Per installare SimLab Viewer sul proprio dispositivo (PC/Mobile/VR Headset) seguire i seguenti passaggi:
- Visita la [sezione Showroom](https://www.simlab-soft.com/technologies/simlab-showroom.aspx) del sito ufficiale di SimLab per scaricare l'installer del Viewer per il sistema desiderato.
  ![[SimLabViewerDownload.png]]
	1. Nel caso si voglia installare la **versione per PC** sarà sufficiente cliccare il pulsante per il sistema operativo del proprio PC e il download verrà eseguito in automatico.
	   Una volta eseguito il file basterà seguire la **procedura di installazione** senza particolari modifiche alle impostazioni di default e SimLab Viewer sarà utilizzabile.
	2. Nel caso si voglia installare la **versione per il visore PICO** bisognerà cliccare il pulsante `Pico VR` e successivamente `Get it Now`, una volta inseriti i dati nel form il file verrà scaricato.
	   > **NOTA BENE**
	   > La versione per Pico dovrà poi essere **caricata sul visore**, i visori in dotazione alla scuola avevano già il software installato quindi non **abbiamo dovuto eseguire il processo di installazione.**

SimLab Viewer è disponibile anche come app per:
- Android e iOS
- Dispositivi VR come Meta Quest

---
## Installazione di Blender
Blender è un software libero, open source e multipiattaforma per la modellazione, animazione, rigging, compositing, rendering, editing video e molto altro.

Per installar Blender seguire i seguenti passaggi:

1. Visita il sito ufficiale di [Blender](https://www.blender.org/download/).
2. Il sito rileverà automaticamente il tuo sistema operativo. Se non lo fa, clicca sul menù a tendina per selezionarlo manualmente.
### Installazione su Windows
1. Clicca su `Download Blender` per Windows.
2. Scarica il file `.msi`.
3. Al termine del download, esegui il file.
4. Segui il processo guidato d’installazione. Puoi lasciare le **impostazioni predefinite**.
Al termine, Blender sarà installato e potrai avviarlo dal menu Start o dalla scorciatoia sul desktop.
### Installazione su macOS
1. Clicca su Download Blender per macOS (formato `.dmg`).
2. Una volta scaricato il file `.dmg`, aprilo.
3. Trascina l'icona di Blender nella cartella Applicazioni.
4. Avvia Blender dalla cartella Applicazioni (potrebbe comparire un messaggio di sicurezza: clicca su `Apri` tenendo premuto il tasto `Control` la prima volta).
### Installazione su Linux
1. Blender è disponibile in formato `.tar.xz`, scarica il file.
2. Estrai il contenuto dell’archivio in una cartella a tua scelta.
3. Apri un terminale, spostati nella cartella estratta e lancia Blender con il comando:
```Bash
./blender
```
(oppure crea un collegamento per facilitarne l’avvio). 

In alternativa, puoi installare Blender tramite gestori di pacchetti come:
**Ubuntu/Debian:**
```bash
sudo apt install blender
```
**Fedora:**
```bash
sudo dnf install blender
```
**Snap (disponibile su molte distro):**
```bash
sudo snap install blender --classic 
```
### Requisiti di sistema
#### Windows
- **Sistema operativo:** Windows 8.1 (64-bit), Windows 10 o 11
- **CPU:** 4 core con supporto SSE4.2 (8 core consigliati)
- **RAM:** 8 GB (32 GB consigliati)
- **GPU:** 2 GB VRAM compatibile con OpenGL 4.3 (8 GB VRAM consigliati)
#### macOS
- **Sistema operativo:** macOS 11.2 (Big Sur) o superiore
- **CPU:** Apple Silicon o Intel
- **RAM:** 8 GB (32 GB consigliati)
- **GPU:** Compatibile con Metal 2.2
#### Linux
- **Sistema operativo:** Distribuzione con glibc 2.28 o più recente (64-bit)
- **CPU:** 4 core con supporto SSE4.2 (8 core consigliati)
- **RAM:** 8 GB (32 GB consigliati)
- **GPU:** 2 GB VRAM compatibile con OpenGL 4.3 (8 GB VRAM consigliati)
