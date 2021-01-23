Repository creato per il Final Projects di Intelligent Systems anno 2020/2021

Sviluppato tramite il software NetLogo da _Polticchia Mattia_ e _Matteo Baldassarrini_
# Covid_Distantiation 
Vi sono due tipi di agenti: le persone (numero parametrico), che si muovono in maniera random nello spazio, hanno un cono visivo (parametro) e vengono attratte convergendo in misura diversa (parametro) verso i vicini da cui mantengono una distanza minima (parametro). I distanziatori hanno un cono visivo in generale più lungo delle persone ed hanno il compito distanziare le persone che sono ad una distanza inferiore al minimo globale (parametro). Se una persona ha un minimo corrente inferiore a quello globale e vede un distanziatore nel suo cono visivo, aumenta il proprio minimo a quello globale e lo mantiene per un certo numero di tic, dopo di che ritorno alla distanza minima delle persone. Ad ogni passo vengono mostrate il numero di persone a distanza inferiore al minimo globale. Definire una strategia distribuita opportuna di comportamento dei distanziatori. Eventualmente definita da parametri per  in modo da minimizzare il numero di persone   distanza inferiore alla minima globale. Es. Autodistribuire i distanziatori o randomizzarli.

# Analisi
## Ambiente 
Distanza Minima Globale
Visualizzatore di persone.distanza < Globale.distanza

## Agenti
* Persone: 
    * Parametri:
	    - Numero 
	    - Cono visivo
	    - Distanza di attrazione minima & massima
	    - Azioni
    * Azioni:
        - Movimento randomico che tende verso le altre persone
        - Se viene visto un distanziatore e sono vicine ad altre persone si allontanano fino ad essere alla distanza minima globale
* Distanziatori
    * Parametri:
        - Cono Visivo ( + ampio rispetto alle persone )
        - Distanza Minima Globale da far rispettare 
    * Azioni: 
        - 1° Stazionario
        - 2° Random
        - 3° Giro

Inserire immagine di riferimento.

# Consegna
È necessario svolgere una relazione da consegnare assieme al progetto e una piccola presentazione da presentare in sede d'esame.

## Relazione 
La relazione deve contenere:

- descrizione del problema e delle ipotesi adottate

- l'algoritmo e le caratteristiche della soluzione

- discussione della complessità/efficienza stimata

- dati di esempio ed eventuali test comparativi sulle prestazioni



## Possibili implementazioni / Fatti su cui pensare
Ragionare sul random degree nell'attuale funzione di movimento
Ha senso tenerlo? Senza sembra essere miglire.

Decidere se conviene fare un esecuzione per volta e permettere il cambio dei parametri solo prima dell'esecuzione.

Impostare  i movimenti  in funzioni separate

Modificare e semplificare i movimenti

Si potrebbe fare che invece di cohere gli agenti "persone" potrebbero incontrarsi, fermarsi per simulare un assembramento e se visti dagli agente "distanziatore" si allontano in direzioni casuali 
turn 270 fd 1
si girano di gradi random e vanno avanti.
