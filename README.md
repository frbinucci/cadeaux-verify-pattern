###PROGETTO CADEAUX

###GRUPPO 4: VERIFICA PATTERN

###INFORMAZIONI GENERALI SULLO SCRIPT
***
Lo script consente di verificare quanti schemi (pattern) sono presenti nel file di output confrontando gli output prodotti dal codice da correggere con quelli previsti.
Siccome gli output possono variare di molto a seconda di chi ha prodotto il codice, questo script consente di verificare che sul file di output siano presenti solamente gli elementi necessari per giudicare la correttezza dello script.

###REQUISITI E FUNZIONAMENTO
***
Lo script necessita dei seguenti dati in input:  

* Percorso della cartella generale degli utenti.
* Percorso della cartella del singolo utente.
* Percorso della cartella del progetto.
* Nome del file da compilare.

Tali dati dovranno essere passati ad uno degli script creati dai gruppi 1 e 2. In particolare, nel caso in cui il file da compilare abbia un'estensione .java, 
lo script richiamerà quello creato dal gruppo 1, nel caso in cui l'estensione sia .c richiamerà invece quello creato dal gruppo numero 2.

Nel caso in cui l'estensione non sia riconosciuta verrà generato un messaggio di errore e il programma genererà l'exit code 3.

Gli script creati dai primi due gruppi restiuiranno il percorso del file eseguibile, il quale verrà salvato su un'apposita variabile. A questo punto 
lo script necessiterà di ulteriori input, in particolare:

* Il file contenente gli input esemplari.
* L'eseguibile "soluzione".

Gli input contenenti nel file verranno redirezionati all'eseguibile "soluzione" e all'eseguibile da correggere i quali, a loro volta, redirezioneranno 
i propri output in due file differenti.

Il codice soluzione, creato dal docente, deve contenere solo ed esclusivamente gli output essenziali, i quali verranno salvati all'interno del file in cui
verrà redirezionato l'output. Il contenuto di quest'ultimo file verrà redirezionato all'interno di un'apposita variabile (tramite il comando cat) e verrà quindi
impostato un ciclo che controllerà se ogni pattern contenuto all'interno della variabile sarà presente all'interno del file contenente l'output prodotto dal 
programma creato dallo studente (tramite il comando grep). Una variabile conterà il numero di cili, mentre un altra il numero delle corrispondenze trovate.

*Problematica da risolvere: la redirezione dell'output dei programmi genera un file con caratteri di fine linea in formato Windows*

Al termine del ciclo vi sarà un controllo:

* Se il numero di pattern trovati sarà uguale al numero di cicli eseguiti tutti i pattern sono stati trovati, lo script restiuirà exit code 0.
* Se il numero di pattern trovati sarà minore del numero di cicli eseguiti non tutti i pattern saranno stati trovati, lo script restiuirà exit code 1.
* Se il numero di pattern trovati sarà 0 il codice creato dallo studente sarà completamente errato, lo script restiuirà exit code 2.

###RIEPILOGO DEI REQUISITI NECESSARI

***

####ARGOMENTI DA FORNIRE AGLI SCRIPT 1 O 2

* Cartella contenente gli utenti
* Cartella del singolo utente
* Cartella del progetto
* Nome del file da compilare

####DATI PROVENIENTI DAGLI SCRIPT 1 O 2

* Percorso del file eseguibile

####DATI SPECIFICATI DALL'UTENTE

* Percorso dell'eseguibile di esempio
* Percorso del file contente gli input

####OPERAZIONI NECESSARIE AL CORRETTO FUNZIONAMENTO DELLO SCRIPT

* Il codice utilizzato come esempio dovrà fornire solo gli output indispensabili
* Il carattere di fine linea dei file di output deve essere in formato UNIX







