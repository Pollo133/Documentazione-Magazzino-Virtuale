## Business Streaming 
### Introduzione
**PICO Enterprise Streaming** è un set di software di supporto ai visori della PICO che consente agli utenti di utilizzare i contenuti dalla piattaforma Steam sul visore Pico VR tramite una funzione di streaming. Questa tecnologia è alla base di una vasta gamma di visori per la realtà virtuale, tra cui il **Pico 4 Enterprise**.

Lo streaming è composto da due applicazioni: 
- **Lato PC:** è compatibile con sistemi Windows VR-Ready e richiede l'installazione di SteamVR
- **Lato visore:** preinstallato nel visore PICO VR. 

Per il corretto funzionamento dello streaming è inoltre necessario che il router sia di tipo Gigabit con banda WiFi 5G. 

Il software **Business Streaming** ha tre modalità differenti:
1. Streaming tramite **Wi-Fi**.
2. Streaming tramite cavo **USB**.
3. Streaming tramite **DisplayPort**.
##### Streaming tramite Wi-Fi :
Il computer deve essere collegato al router con un **cavo di rete di categoria 6**. È necessario che il router wireless del computer sia compatibile con la **banda a 5 GHz**.
*E' supportato su tutti i dispositivi PICO Enterprise [[2 - I Visori VR#Glossario|6DoF]]*

**Vantaggi:**
- Nessun cavo di connessione al computer
**Svantaggi:**
- Segnali di rete facilmente disturbati.

![Immagine Streaming con WIFI](Immagini/StreamingWIFI.jpg)
#### Streaming tramite cavo USB
Lo streaming tramite cavo USB si ottiene collegando un **connettore USB-A** a un'estremità e un connettore **USB-C** all'altra. La velocità di trasmissione deve essere in linea con quella dello standard **USB 3.0 o superiore**. Il cavo deve essere lungo circa **4-5 metri**, una **lunghezza eccessiva causerà attenuazione del segnale** e interferenze, mentre una lunghezza troppo corta potrebbe non essere sufficiente.
*E' supportato su tutti i dispositivi PICO Enterprise 6DoF*

**Vantaggi:**
- Trasmissione delle immagini veloce e stabile.

![Immagine Streaming con USB](/Immagini/StreamingUSB.jpg).
#### Streaming tramite DisplayPort
Lo streaming tramite DisplayPort si ottiene collegando un'estremità alla porta DP del visore e l'altra estremità alla porta DP del computer. Si usi l'**USB 3.0** o superiore. Si prega di utilizzare il **cavo DP ufficiale** acquistato da PICO.
*E' supportato su PICO Neo3 Pro / Pro Eye*

**Vantaggi:**
- Trasmissione delle immagini veloce e stabile.

![Immagine Streaming con display port](/Immagini/StreamingDisplayPort.jpg).
### Installazione 
Configurazione del computer richiesta per poter utilizzare Business Streaming:
1. **Sistema operativo:** Windows 10 o Windows 11
2. **Processore:** Intel Core i5-4590/ AMD FX 8350 o superiore
3. **Memoria:** 8 GB  RAM o superiore 
4. **Scheda grafica:** NVIDIA GeForce GTX 970, AMD Radeon RX 480 o superiore (la scheda grafica consigliata è NVIDIA GeForce GTX 1060, AMD Radeon RX 480)
5. **Sistema Operativo:** Windows 10+
6. **Software:** SteamVR

Una volta verificati i requisiti per l'installazione è sufficiente visitare il [Sito Ufficiale di Business Streaming](https://business.picoxr.com/us/doc/BusinessStreaming) e scaricare la versione che coincide con la versione installata sul visore.
A questo punto l'installer guiderà tutto il processo di installazione una volta eseguito.

---
## SimLab Viewer
### Introduzione
SimLab VR Viewer è un'applicazione gratuita, autonoma e multipiattaforma, che esegue le esperienze VR di SimLab ( `.vrpackage`) create con i prodotti SimLab Soft .

Le sue **funzionalità principali** che possono essere utilizzate accedendo al menù presente all'interno del mondo virtuale sono:
1. Controllo ambientale
2. Catalogo VR
3. Materiali di modifica
4. Misure
5. Note
6. Modalità di navigazione
7. Condivisione SimLab
#### Controllo ambientale
Permette di controllare l'**illuminazione della scena**, il sole e il cielo, la nebbia e le luci HDR in tempo reale mentre si è nell'ambiente virtuale.
#### Catalogo VR
Mette a disposizione dei **modelli 3D** (in locale o online) che possono essere importati e piazzati direttamente nella scena virtuale per rendere più immersiva l'esperienza dell'utente. Questi oggetti **non verranno aggiunti definitivamente** al progetto.
#### Materiali di modifica
Direttamente dal VR si possono cambiare i **materiali** dei vari oggetti modificandone i tipi e applicando diversi tipi di strumenti a disposizione dell'utente. Anche in questo caso le modifiche **non andranno a influenzare il progetto**.
#### Misure
Puoi **misurare** in modo semplice e veloce le dimensioni di un oggetto tracciando delle linee con il cursore presente al centro dello schermo.
#### Note
Lo strumento delle note è la funzionalità più usata. Viene utilizzata per scambiarsi idee e commenti tra il cliente e l'operatore. E permette la **cattura di immagini** direttamente dall'ambiente virtuale.
#### Modalità di navigazione
Nel mondo virtuale è possibile navigare in tre diverse modalità di navigazione: **camminata** (l'utente è quindi relegato al terreno e alla fisica del progetto), **volo** (l'utente può muoversi nello spazio tridimensionale in tutte le direzioni possibili) e **meccanica** (l'utente disporrà di una vista fissa dall'alto)
#### Condivisione SimLab
Si possono vedere e condividere facilmente esperienze virtuali e modelli 3D tra dispositivi e team utilizzando la [piattaforma cloud SimLab](https://youtu.be/-0FJTQ0DoJU) messa a disposizione da SimLab Viewer.
Tramite la **dashboard di SimLab** è infatti possibile **creare un account** e utilizzare una serie di **modelli e tutorial** già messi a disposizione per l'utente. Inoltre un utente che avrà eseguito l'accesso potrà **caricare sul cloud** i suoi modelli che saranno disponibili al **download** e all'utilizzo su tutti i dispositivi connessi con il suo account.
### Installazione
Per l'Installazione fare riferimento alla [[3 - Installazione Ambiente di Sviluppo#Installazione di SimLab Viewer|pagina di documentazione dedicata]].

---
## Steam e Steam VR
### Introduzione
Steam è una piattaforma che si occupa di distribuzione digitale di **videogiochi**, gestione dei diritti digitali, modalità di gioco multigiocatore e comunicazione.

SteamVR è un'applicazione inclusa nel client di Steam che consente di **usufruire della realtà virtuale**. SteamVR viene installato automaticamente quando Steam rileva la connessione di un visore al PC dell'utente, ma può essere installato anche manualmente.

SteamVR consente la gestione da parte dell'utente di diversi aspetti della loro esperienza VR (realtà virtuale), tra cui:
1. **Configurazione della stanza**, con cui definire la propria area di gioco.
2. Stato e **gestione del dispositivo**, con cui aggiornare il firmware, associare nuovi dispositivi, cambiare le impostazioni audio, impostare la duplicazione e personalizzare funzionalità.

**SteamVR Home** è il punto d'inizio per gli utenti di SteamVR. I giocatori possono avviare app, connettersi con gli amici ed esplorare ambienti diversi in lobby private o pubbliche, completare missioni, creare e personalizzare avatar ed ambienti e sfogliare il Negozio e la Comunità di Steam.
### Installazione
L'installazione di Steam è semplice e veloce:
1. Visitare la [pagina ufficiale di steam](https://store.steampowered.com/about/) e cliccare `INSTALLA STEAM`.
   ![[SteamDownloadPage.png]]
2. Scaricare il **setup** ed eseguirlo (non sono necessarie impostazioni particolari).
   ![Immagine run](/Immagini/run.jpg)
3. Avviare il software.
4. Creare un nuovo **Account Steam** o **accedere** a uno già esistente.
![Immagine login](/Immagini/login.jpg)
5. Completare l'autenticazione cliccando sull'opzione dove affermi di aver ricevuto un codice da Steam Support.
   ![Immagine messaggio](/Immagini/message.jpg)
6. Compilare l'accesso con il codice ricevuto e clicca 'Finito'.
   ![Immagine codice](/Immagini/code.jpg).
7. Cercare nella barra di ricerca dei giochi "**Steam VR**"
   ![[SteamSearch.png]]
8. Nella pagina dell'applicazione, in basso, premere su `Avvia Gioco`, se Steam VR non è ancora installato inizierà il download.
   ![[SteamVRAVVIA.png]]
   ![Immagine spazio](/Immagini/spazio.jpg)
   
>**NOTA BENE**
>Puoi verificare che Steam VR sia in fase di download visitando la scheda Libreria. L'app sarà visibile lì, in coda o in fase di download.

Una volta seguite queste operazioni l'ambiente si Steam sarà correttamente installato e pronto ad essere utilizzato per un visore.

>**NOTA BENE**
>Se hai precedentemente installato Steam e stai reinstallando per risolvere un problema con la tua installazione precedente, puoi semplicemente eseguire nuovamente il programma di installazione di Steam e Steam verrà reinstallato automaticamente