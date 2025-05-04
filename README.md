# PreventHDDSpinOFF
Utility per mantenere attivi dischi usb serie WD_Black D10 Xbox Edition in windows 

Ciao a tutti, Posseggo un WD_Black D10 XBOX Edition USB che utilizzo per fare archivione del contenuto del mio pc! Ho riscontrato comunque un fastidiosissimo problema..  se il disco non è in uso per più di 70-80 secondi, va in standBy!

Naturalmente non è un problema del disco, da quanto ho capito è un comportamento standard! Comunque certo è che se stai navigando tra le cartelle o ti fermi per poco più di un minuto si inizia a risentire dei continui start & stop!

Ho visto che per altri Drive esterni della WD esistono programmini di supporto che permettono di modificare le impostazioni, ma per il WD_Black D10 XBOX Edition a quanto pare no.. o forse non sono riuscito a trovarli io! In ogni caso ho deciso di dedicare un attimo di tempo (e con l'aiuto di chat-gpt per qualche linea guida e qlk ricerchina su Google) dato non mettevo mani su vb.net da tanto ho scritto un piccolo programmino per sopperire a questa mancanza. 

Allego sia l'eseguibile che il Source usato in Visual Studio 2022 CE.

Spero possa essere utile anche a voi!

Il programma è molto semplice, Interfaccia semplicissima, chiede quale disco monitorare, per quanto tempo e ogni quanti secondi eseguire una funzione che mantenga il disco attivo.

![Screenshot 2025-05-04 070429](https://github.com/user-attachments/assets/3f993407-99c6-43b1-a889-dbfd51b966c4)

Per ottenerlo semplicemente scrive un file vuoto sulla root e periodicamente lo rinomina. Se il disco risulta in uso salta il processo fino a quando non rileva un utilizzo pari a zero. Io ho impostato di base 30 minuti ogni 60 secondi. In ogni caso se questi parametri sono modificati il tutto viene salvato automaticamente in un file .ini

Come detto il codice sorgente è li se volete migliorarlo.. magari invece di una selezione per singolo disco usare un elenco con selezioni multiple (nel mio caso non mi serve)

Una volta avviato il programma tramite il pulsante Spin ON viene iconizzato nella traybar. Doppio click per ripristinarlo.

Il file viene creato ed eliminato dal programma stesso.. premessa che il disco non venga rimosso manualmente prima di aver terminato l'applicazione.. Ciao a tutti!!

---------

Aggiornamento versione 2 : Inserito flag per il riavvio automatico dopo la scadenza del tempo massimo di prevenzione dello spegnimento. Se l'applicazione rileva un uso del disco da parte del sistema operativo riavvia il timer.


