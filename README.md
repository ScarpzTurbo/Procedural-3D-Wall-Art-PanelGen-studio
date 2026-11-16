# PanelGen-studio
A procedural Blender add-on for creating customizable 3D wall art, with full control over shapes, details, and dimensions, featuring seamless 3D model export for 3D printing.
PANELGEN STUDIO 1.0 — PLUGIN AUTONOMO

Compatibilita: Blender 5.1 o successivo; prove eseguite su Blender 5.1.2. Non e certificato per versioni precedenti.

INSTALLAZIONE
Preferenze > Componenti aggiuntivi > Installa da disco: selezionare PanelGen_Studio_1.0.zip e attivare PanelGen Studio.
Il pannello N > PanelGen e i pulsanti nella scheda Modificatori sono registrati dal plugin e restano disponibili alla riapertura. Non serve eseguire Text datablock o abilitare l'esecuzione automatica degli script contenuti nei .blend.
In una scena nuova usare Crea PanelGen (unita mm). Gli oggetti gia presenti non vengono eliminati. E supportato un generatore canonico PANEL_GEN per file.

CONTROLLI
1 BU = 1 mm. Conteggi X/Y, dimensioni automatiche/manuali, gap reale e margini. HEIGHT_CTRL si muove e scala; sono disponibili immagine B/N e noise. Tip Orbit applica un campo rotazionale comune lasciando ferme le basi.
Anteprima libera consente 0–360 gradi ma NON certifica la stampabilita. Il controllo stampa puo quindi segnalare difetti senza che il programma sia guasto.

BASI E ASSEMBLAGGIO
Crea/aggiorna base attiva la base rettangolare lunga quanto il pannello; spessore regolabile.
Gap=0 con layer continuo attivo riempie tutto il rettangolo, anche fra basi pentagonali. Il layer e parte del rilievo; la base aggiuntiva puo essere applicata sotto, con spessore indipendente. La preview rimane istanziata: l'unione solida e effettuata solo sulle copie di esportazione.

ESPORTAZIONI
- Singoli senza base aggiuntiva: un file per rilievo. Se Gap=0, include il rispettivo tassello del layer uniforme, senza la base aggiuntiva.
- Singoli con base: un solido chiuso per pezzo, con base affiancabile.
- Pannello intero con base: un unico solido.
- Settori con base: rettangoli di celle complete, senza tagliare i rilievi, entro Max X/Y/Z.
Mantieni coordinate del pannello evita il riposizionamento: i file contengono le coordinate originali. Nel slicer disattivare l'auto-disposizione o importare come parti dello stesso modello. Il manifest identifica righe/colonne e offset.
Esporta viewport STL conserva esattamente la geometria visibile, senza certificazione di stampa.

GARANZIE E LIMITI
Le unioni con base sono controllate per volume positivo, un solo componente, bordi manifold e facce non degeneri. Vengono verificati ingombro, file STL binario e reimportazione. Sbalzi, supporti e dimensioni delle punte in anteprima libera richiedono comunque una verifica di stampa. Non sono aggiunti incastri meccanici: le basi sono affiancabili per assemblaggio/incollaggio.
Le vecchie opzioni avanzate Custom Collection, certificazione di mesh arbitrarie e image blur non sono dichiarate implementate. Non sono necessarie ai pulsanti principali verificati.

Il plugin funziona localmente, senza il connettore Higgsfield. In file non ancora salvati, gli export vanno nella cartella PanelGen_Exports della home utente.
