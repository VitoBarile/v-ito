Processi

Un intero sistema o un insieme di processi che possono essere eseguiti in parallelo sui processori alternando nell’esecuzione.  
Ogni processo è costituito da due parti: 
● codice (composto dalle istruzioni); 
● dati del programma, a loro volta suddivisi in:
	 – ==variabili globali==, allocate nella RAM nell’area dati globali
	 – ==variabili locali e non locali== memorizzate in uno stack 
	 – ==variabili temporane==e introdotte dal compilatore (tra cui PC o IP) caricate nei registri del processore
	 – ==variabili allocate dinamicamente== durante l’esecuzione, memorizzate in un heap*.

E’ possibile avere in esecuzione contemporaneamente più istanze di un programma, ossia più processi originati dallo stesso codice. I processi possono essere:
● Indipendenti: un processo può evolvere autonomamente senza necessità di scambiare dati con altri processi 
● Cooperanti: due o più processi per evolvere necessitano di scambiarsi informazioni 
● Competitori: due processi possono ostacolarsi a vicenda, per usare la medesima risorsa, compromettendo la terminazione delle loro elaborazioni

Un programma può generare più processi, ma ogni processo è associato ad un solo programma.
	-**processo utente**: processo generato da un programma scritto dall’utente
	-**processo supervisore**: processo generato da un programma del SO( es. gestore dell attività)

I processi supervisori in esecuzione sulla cpu (in background) hanno un’importanza maggiore rispetto ai processi utente.
Quando un programma va in esecuzione viene creato il processo(memorizzato in memoria centrale)
**PCB**: strutture che contengono le informazioni relative allo stato del processore ovvero:
	-*PID(process identifier)*
	-*indirizzo del descrittore di processo che lo ha generato(puntatore)*
	-*la priorità*
	*-lo stato di avanzamento*
	*-immagine nella memoria*
	*-informazioni relative alle altre risorse assegnate nel processo*

Un processo può avviarne altri(copie). questo processo viene chiamato”processo padre”, mentre i processi “copie” vengono chiamati “processi figli”. 

Descrittore di processo
Il SO per ogni processo deve mantenere delle informazioni, che istante per istante tengano traccia di cosa sta “facendo il processo”. L’insieme di queste informazioni è detto descrittore di processo