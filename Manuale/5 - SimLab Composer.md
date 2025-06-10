**SimLab Composer** è l'ambiente di sviluppo che è stato utilizzato per la creazione e la modifica del magazzino virtuale. Il software permette l'importazione di modelli 3D da diversi [formati](/SimLab-Composer/Formati-di-Importazione) e la manipolazione di questo materiale all'interno delle **scene** grazie ad [**animazioni**](/SimLab-Composer/Animazioni) e [**scripting**](/SimLab-Composer/Training-Builder). Con tali strumenti è possibile costruire un ambiente interattivo e visualizzabile sia tramite apposito dispositivo VR sia su PC con SimLab Viewer.
## Apertura del progetto
Una volta scaricata e installata la versione gratuita di SimLab Composer dal [sito web ufficiale](https://www.simlab-soft.com/3d-products/simlab-composer-trial.aspx?composer_main_page) sarà necessario accedere al proprio account SimLab (o registrarsi se non se ne possiede uno) ed eseguire l'**`Edizione Gratuita`**.
Per aprire un progetto già esistente bisognerà selezionare l'icona con l'immagine dei file del menù in alto e poi cliccare il tasto **`Aperto`** che aprirà la schermata di esplora risorse da cui si dovrà cercare il file relativo al progetto.
Il file in questione sarà di tipo **`.sim`**.

---
## Formati di Importazione
In Blender è possibile esportare i modelli 3D in tre diversi formati di file compatibili a SimLab Composer.
### Wavefront (OBJ) [1]
Il formato OBJ è un file di testo in cui ogni riga descrive un elemento della geometria.
*   È facilmente leggibile e modificabile manualmente, rendendolo un formato trasparente per lo scambio di dati 3D.
*   Si concentra esclusivamente sulla geometria, senza includere informazioni su animazioni o strutture gerarchiche complesse.
*   Utilizza un file di supporto esterno chiamato **MTL** (Material Template Library), che definisce colori, texture e altre proprietà dei materiali.

> **NOTA BENE**  
> Anche se l'OBJ è un formato testuale, non si basa su XML, ma segue una sintassi propria che lo rende comunque relativamente semplice da leggere e modificare.
### Collada (DAE) [2]

COLLADA (_Collaborative Design Activity_) è stato sviluppato per facilitare lo scambio di asset 3D tra diversi software.
*   Supporta non solo la geometria statica, ma anche animazioni, trasformazioni, scheletri e altri dati dinamici.
*   È progettato per essere un formato versatile, adatto all'interscambio di modelli con materiali, texture e strutture complesse.

> **NOTA BENE**  
> In Blender, COLLADA è considerato un formato "legacy", il che significa che potrebbe non essere aggiornato rispetto alle tecnologie più recenti o alle attuali esigenze di interoperabilità.
### Stereolithography (STL)

STL descrive la superficie di un modello 3D tramite una rete di triangoli.
*   È un formato essenziale, focalizzato esclusivamente sulla geometria.
*   Non supporta materiali, texture, colori o animazioni.

> **NOTA BENE**  
> L'assenza di informazioni su materiali, texture e animazioni rappresenta una limitazione del formato STL, rendendolo meno adatto per l'interscambio di modelli complessi.

---
## Animazioni
In SimLab Composer l'unico modo per gestire lo spostamento degli oggetti sono le **animazioni**, uno strumento che permette tramite una timeline di **registrare** le diverse **posizioni** che un oggetto deve assumere e come questo si **muove nello spazio** per raggiungerle.

Per aggiungere e modificare le animazioni si deve utilizzare l'apposita schermata posizionata di default nella zona bassa dello schermo, selezionando la tab `Animazione`.

![[TabAnimazioneSimLab.png]]

La schermata che appare si può dividere in 3 zone principali:
- **Albero di selezione**.
- **Timeline dei keyframe.**
- **Barra Opzioni**.
#### Albero di Selezione
Nella zona in basso a sinistra è presente una piccola finestra grigia chiamata "Albero di selezione". In questa zona verranno mostrati **tutti gli oggetti selezionati** nella scena.

![[AlberoDiSelezione.png]]

Ad ogni oggetto mostrato nella schermata sarà associata una **timeline** nell'apposito riquadro a fianco, ogni elemento potrà avere **solo una animazione** in contemporanea negli stessi keyframe, quindi, per aggiungerne un'altra in parallelo, sarà necessario creare un **ulteriore oggetto** che dovrà essere posto in relazione con quello originale **come oggetto padre**.
#### Timeline dei keyframe
La Timeline presenta invece la serie di **keyframe catturati** su un oggetto durante la creazione dell'animazione. 

![[TimelineAnimazione.png]]

La Timeline è a sua volta suddivisa in diverse parti:
- **Cursore** (nell'immagine impostato su 0)
  Indica il frame nel quale si trovano al momento gli oggetti nella visualizzazione.
- **Cursore di fine** (nell'immagine impostato su 100)
  Indica il frame nel quale l'animazione si interromperà. Lo spostamento del cursore aumenterà quindi la durata dell'animazione aggiungendo più frame.
- **Riquadro dei keyframe**
  Riquadro nel quale è possibile trovare in arancione i keyframe registrati.
#### Funzionalità (Barra Opzioni)
Per creare, manipolare, organizzare ed eliminare i keyframe è necessario utilizzare i tasti presenti nella barra delle opzioni.

![[ToolbarAnimazione.png]]
Di seguito sono illustrate le **principali funzionalità:**
1. **Cattura** un keyframe per ogni **oggetto selezionato**.
2. Rende **visibile un oggetto** a partire dal **keyframe selezionato** con il cursore.
3. Rende **invisibile un oggetto** a partire **keyframe selezionato** con il cursore.
4. **Riproduce** l'intera animazione.
5. Selezionato un elemento dall'albero di selezione **salta al keyframe salvato più vicino** in **avanti** o **indietro** rispetto al cursore d'inizio.
6. Seleziona **tutti i keyframe** degli **oggetti selezionati** (presenti nell'albero di selezione)
7. Selezionati più keyframe salvati li **raggruppa** in modo reversibile.
8. Selezionato un gruppo di keyframe li **divide** nei keyframe originali (è l'operazione inversa della funzionalità 7).
9. Apre una finestra di dialogo dalla quale è possibile indicare di quanti frame **spostare** un certo keyframe salvato.
10. Apre una finestra di dialogo dalla quale è possibile indicare di quanti frame **spostare la copia** di un certo frame.
11. **Elimina** i keyframe **selezionati**.
12. **Elimina** **tutte le animazioni** presenti nella scena.
13. **Salva tutti i keyframe selezionati in una sequenza** che sarà possibile utilizzare dalla sezione `Sequenze`. Per riutilizzarla sarà sufficiente cliccare due volte la sequenza e confermare le impostazioni già selezionate.
14. Apre l'**elenco delle sequenze** dal quale sarà possibile selezionarle per **inserirle** all'interno della timeline.
15. Permette di creare delle **animazioni** che richiedono un **movimento particolare**, come quello di una ruota.
    Per permettere ad un oggetto di ruotare, ad esempio, sarà necessario prima indicare il **fotogramma di inizio e fine**, poi il **numero di giri** che si vogliono far fare all'oggetto in quel tempo e infine la **direzione**. 
    Sarà infine necessario selezionare un punto dell'oggetto che serva da **baricentro** per la rotazione all'oggetto.

---
## Introduzione a Visual Scripting 
Visual Scripting è un metodo di creare programmi usando degli **elementi grafici** al posto di scrivere manualmente codice. Permette agli utenti di costruire delle funzionalità tramite dei "blocchi visivi" o "nodi" i quali rappresentano differenti funzioni e o azioni.
Tra i suoi **benefici** troviamo:
- la facilità d'uso
- la velocità nello sviluppo
- semplice apprensione
### Suddivisione nodi SimLab
I nodi vengono suddivisi in 4 categorie principali:
- **Inputs List**
- **Events List**
- **Responses List**
- **Booleans List**
### Input
Gli input sono entità utilizzate come innesco a determinate azioni. Il nodo input più importante è **SceneNode Query** il quale ci permette di riferirci ad uno o più oggetti in riferimento agli attributi. 
##### Events
Gli Events sono i nodi che utilizziamo per catturare le interazioni utenti-ambiente.
Qualsiasi azione vogliamo venga eseguita all'inizio dobbiamo far si che sia collegata a un **Scene Start**.
Quando un utente coglie un oggetto viene attivato il **Node Grab Started**, al contrario, quando viene posato si attiva il **Node Grab Ended**.
##### Responses
Le Responses sono inserite in successione agli Events, servono per attuare una modifica in un ambiente o ad un oggetto.
Le principali sono:
- Glow | Unglow Object 
- Change Node Grabbable State
- Fall to Surface
- Reset Rotation 
##### Booleans
Sono dei nodi che producono tramite degli input un booleano (vero o falso). Includono operatori logici come AND, OR, NOT e dei controlli sullo stato dell'oggetto.

---
## Visualizzazione Anteprima Magazzino
Per eseguire operazioni di testing sull'ambiente virtuale è necessario utilizzare il software SimLab Viewer che, se già installato correttamente sul pc, può essere direttamente avviato da Composer. In tal modo sarà possibile provare il mondo virtuale anche senza avere a disposizione il visore.
### Avvio
1. Dal menù di in alto selezionare l'icona con il visore.
![[VisualizzaAnteprima.png]]
2. Utilizza l'opzione `Mostra nel visualizzatore`.
3. Seleziona la modalità `Desktop` e attendi il caricamento del mondo.
![[ModalitàVisualizzatore.png]]
##### Tasti utili
`Q`, `E` --> Rotazione in senso Antiorario/Orario
 `W`, `A`, `S`, `D` --> Movimento
 `Spazio` --> Salto
 `H` --> Comparire/Scomparire la mano
 `M` --> Menù
##### Menù
SimLab Viewer presenta un menù con diverse funzionalità, nel capitolo sull'[[4 - Installazione Ambiente di Visualizzazione#SimLab Viewer|ambiente di visualizzazione]].

---
Riferimenti:
[1] *Wavefront OBJ.* Blender 4.4 Manual. https://docs.blender.org/manual/en/latest/files/import_export/obj.html
[2] *Collada (Legacy).* Blender 4.4 Manual. https://docs.blender.org/manual/en/latest/files/import_export/collada.html
[3] *STL.* Blender 4.4 Manual. https://docs.blender.org/manual/en/latest/files/import_export/stl.html