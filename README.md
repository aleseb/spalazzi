# spalazzi
progetto di advanced cybersecurity

spiegazione del progetto: ho scaricato tanti file di log dal garr, ogni file conteneva 10 campi come indirizzo ip, porta di ingresso, datetime. A noi quello che interessa è campo dominio (individuabile visto che è il sesto campo di ogni file di testo e ogni campo è delimitato da un punto e virgola, gli erroi delle righe visto che sono poche e visto che ho preso 2 milioni di domini, non sono state gestiste). esempio di file di testo ---> 2022-10-05 08:05:03.541577;178b3011f59349a0b246ec31c955cfec44db5f42;193.206.141.38;udp;IN;uniurb.it.;MX;ASPMX.L.GOOGLE.COM.;600;1

con questi nomi dei domini devo estrarre monogrammi (es univpm è u n i v p m), bigrammi (es univpm è un ni iv vp pm) e trigrammi (es univpm è uni niv ivp vpm) e con questi file non so che cazzo ci devo fare, credo addestrare il modello per capire quali sono benevoli e quali malevoli (?)

quello che ho fatto io è prendere i file di log, filtrarli per il dominio, concatenarli ed estrarre mono bi e trigrammi tramite algoritmo che ho creato e infine salvarli su un file csv per ogni tipologia mono bi tri. 

ora i passi da fare sono questi: 

- Prendere il classificatore di tipo ensemble denominato stack.

  
- Addestrare lo strato di embedding con mono,bi,tri-grammi e aggiungerlo al classificatore.

  
- Prendere il dataset etichettato UMUDGA (https://data.mendeley.com/datasets/y8ph45msv8/1) In particolare i csv da 10.000 campioni per classe.

  
- creare tre taglie diverse per ogni classe: 1/50, 1/25, 1/10.

  
- Fare la k-fold cross evaluation (se possibile k=10) per ognuna delle tre taglie .

  



