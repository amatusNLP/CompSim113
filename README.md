# CompSim113
Un dataset per testare modelli composizionali di Distributional Semantics in Italiano. 


Lo scopo di questo lavoro è quello di creare un dataset di correlazioni basato sul giudizio dei parlanti per testare
le metodologie di SD composizionali in lingua italiana. 
Pertanto, il dataset consisterà di una serie di parole composte associate a più parole semplici.

Alla parola target, un composto polirematico, sono state associate quattro parole semplici ordinate in scala di plausibilità: 
delle quattro alternative, infatti, una corrisponderà ad un sinonimo della parola target, due rappresenteranno delle ipotesi
plausibili o con significati simili, mentre l'ultima sarà una parola di controllo dal significato completamente arbitrario. 
Un esempio di gruppo di parole associate è il seguente:

    mal di testa: emicrania, cefalea, dolore, diarrea

Nella scelta delle parole target sono state prese in considerazione principalemente parole composte polirematiche con un grado
di idiomaticità basso, cioè dal significato composizionale. 
Parole come "mal di testa" o "macchina fotografica" infatti, presentano un significato che è deducibile dall'unione dei
significati delle parole semplici che le compongono. Parole come "lavaggio del cervello" o "settimo cielo", al contrario,
hanno significati prettamente idiomatici o metaforici che, per definizione, non sono composizionali. 
Il Dataset include, per la maggior parte, composti polirematici composizionali (93), ma si è deciso di includere anche una
percentuale di composti idiomatici, che potranno avere una funzione di controllo o potranno essere esclusi dai possibili test
futuri. 

Le parole target, inoltre, sono state selezionate all'interno di quattro classi grammaticali principali, corrispondenti con
le classi aperte (Aggettivi, Avverbi, Nomi e Verbi), in modo da permettere un'analisi differenziata dei risultati del test.

Il risultato finale è un dataset contenente 113 gruppi di parole, di cui 25 aggettivi, 27 avverbi, 31 nomi e 30 verbi.

Dopo aver selezionato le parole e le espressioni oggetto della nostra analisi, abbiamo realizzato un questionario accessibile
a tutti tramite Survey Monkey. Successivamente i dati sono stati aggregati, generando una media dei punteggi per ciascuna
parola semplice, assegnando così un indice di correlazione che va dall'1 al 4 a ciascuna coppia di parole.

Al dataset finale è stata assegnato un formato tabellare di tipo TSV, 
Ogni riga conterrà, pertanto le seguenti informazioni:

     1. Parola target
     2. Parola semplice
     3. Valore di correlazione (da 1 a 4)
     4. Categoria grammaticale (aggettivo, avverbio, nome, verbo)
     5. Categoria di composto (composizionale, idiomatico)

Nel seguente esempio viene riportata l'associazione tra la parola mal di testa e le quattro alternative, 
suddivisa in quattro righe:

    mal di testa  cefalea  2.893617021  nome  c
    mal di testa  emicrania  3.617021277  nome  c
    mal di testa  dolore  2.404255319  nome  c
    mal di testa  diarrea  1.085106383  nome  c

Il dataset finale consta di 452 coppie di parole.
