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

All'interno di un'apposita variabile verranno redirezionati i pattern presenti nel file di esempio e successivamente, tramite un ciclo for, si controllerà
la presenza di ogni pattern nel file generato dal codice dello studente. Un'apposita variabile conta quanti pattern sono stati trovati.

La ricerca dei pattern avviene tramite la ricerca di dati di tipo numerico nel file di output "esemplare".
*Quest'ultimo aspetto rimane da chiarire poichè possono esistere codici che restituiscono output non numerici.*

Al termine del ciclo vi sarà un controllo:

* Se il numero di pattern trovati sarà uguale al numero di cicli eseguiti tutti i pattern sono stati trovati, lo script restiuirà exit code 0.
* Se il numero di pattern trovati sarà minore del numero di cicli eseguiti non tutti i pattern saranno stati trovati, lo script restiuirà exit code 1.
* Se il numero di pattern trovati sarà 0 il codice creato dallo studente sarà completamente errato, lo script restiuirà exit code 2.


