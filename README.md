# progettoSoar
Progetto SOAR per il corso di Intelligenza Artificiale e Laboratorio - Unito 2022.

## Descrizione progetto

Viene implementato un agente intelligente sviluppato tramite l'architettura cognitiva SOAR in grado di scappare
da una stanza tramite apprendimento per rinforzo (Reinforcement Learning).

L’agente SOAR è prigioniero in un ambiente dove l’unica via d’uscita è una finestra in vetro posta a
3,5 metri di altezza (l’agente è un robot di altezza 150 cm).
La finestra in vetro è blindata ma ha un punto debole alle estremità. Questo vuol dire che, se colpita
con precisione alle estremità, il vetro si può frantumare.
L’agente ha a disposizione i seguenti oggetti che potrebbero tornargli utili per realizzare il suo
obiettivo: una molla, una rametto in legno, ciottoli e pietre. Due tronchi d’albero dello stesso
diametro da 1 metro di altezza ciascuno. L’agente può decidere di creare nuovi oggetti a partire da
quelli che ha a disposizione ma parte da una tabula rasa (non sa quale combinazione va bene).
Nel corso dei suoi tentativi di interazione imparerà i seguenti rinforzi per gli oggetti:
- (Molla + Rametto di legno) = +1
- (Pietre + Rametto di legno) = -1
- (Pietre + Molla) = -1

Ci sono inoltre una serie di rinforzi su altre azioni (es: movimento, posa di un oggetto, scomposizioni di oggetti composti, ecc...) che permettono
all'agente di frantumare la finestra e riuscire a scappare posizionando i due tronchi vicino all'uscita, uno sopra l'altro, per poi arrampicarsi.

Inoltre prevengono esecuzioni con un numero di iterazioni troppo elevate per raggiungere il goal, indirizzando l'agente a prediligere un azione
piuttosto che un'altra tramite i rewards.

Molte scelte implementative sono frutto della mia mente, in riferimento alla fisica (degli oggetti e del robot) e al buon senso.

## Come eseguire

Installare SOAR da https://soar.eecs.umich.edu/. Una volta installato si può proseguire con le esecuzioni.

Per eseguire il codice caricare il file su Soar (tramite il menù 'File --> Load Source File') e premere il tasto Run dell'interfaccia.

Se si vogliono eseguire più Run è necessario inizializzare l’agente al termine di una Run premendo sul pulsante Init-soar e successivamente si può rieseguire.