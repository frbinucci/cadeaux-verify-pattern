###PROGETTO CADEAUX

####GRUPPO 4: VERIFICA PATTERN

###INFORMAZIONI GENERALI SULLO SCRIPT
***
Lo script consente di verificare quanti schemi (pattern) sono presenti nel file di output confrontando gli output prodotti dal codice da correggere con quelli previsti.
Siccome gli output possono variare di molto a seconda di chi ha prodotto il codice, questo script consente di verificare che sul file di output siano presenti solamente gli elementi necessari per giudicare la correttezza dello script.

###REQUISITI
***
Lo script necessita dei seguenti dati in input:

*Percorso della cartella generale degli utenti.
*Percorso della cartella del singolo utente.
*Percorso della cartella del progetto.
*Nome del file da compilare.

Tali dati dovranno essere passati ad uno degli script creati dai gruppi 1 e 2. In particolare, nel caso in cui il file da compilare abbia un'estensione .java, lo script richiamerà quello creato dal gruppo 1, nel caso in cui l'estensione sia .c richiamerà invece quello creato dal gruppo numero 2.

Gli script creati dai primi due gruppi restiuiranno il percorso del file eseguibile, il quale verrà salvato su un'apposita variabile. A questo punto lo script necessiterà di ulteriori input, in particolare:

*Il file contenente gli input esemplari.
*L'eseguibile di esempio.

Gli input contenenti nel file verranno redirezionati all'eseguibile di esempio e all'eseguibile da correggere i quali, a loro volta, redirezioneranno i propri output in due file differenti.



