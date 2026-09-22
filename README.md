# 🎮 Player Count Forecasting

Progetto di **Intelligenza Artificiale** dedicato al **Time Series Forecasting** del numero di giocatori attivi nei videogiochi distribuiti sulla piattaforma Steam.

L'obiettivo è prevedere l'evoluzione del **player count giornaliero** di un gioco su un **orizzonte temporale di 14 giorni**, confrontando diverse architetture di forecasting.

## 🎯 Obiettivo

Il numero di giocatori attivi di un videogioco può variare significativamente nel tempo ed è influenzato da diversi fattori, tra cui:

* aggiornamenti del gioco;
* eventi speciali;
* promozioni e variazioni di prezzo;
* andamento delle recensioni;
* pattern temporali e stagionali.

Il progetto studia la capacità di diversi modelli di **deep learning per il forecasting** di catturare queste dinamiche e prevedere l'andamento futuro del player count.

## 🤖 Modelli confrontati

Sono stati confrontati tre modelli di forecasting:

### TCN — Temporal Convolutional Network

Architettura basata su **Convolutional Neural Networks (CNN)** progettata per l'analisi di sequenze temporali.

Le convoluzioni temporali permettono di analizzare finestre temporali estese e di catturare dipendenze tra osservazioni distanti nel tempo.

### N-BEATSx

Estensione di **N-BEATS** che integra **variabili esogene** oltre alla serie temporale principale.

Questo permette al modello di utilizzare informazioni aggiuntive, come prezzo e andamento delle recensioni, durante la previsione.

### N-HiTS

Evoluzione di N-BEATS che utilizza una struttura **gerarchica e multi-risoluzione** per analizzare pattern temporali a diverse scale.

L'approccio permette di catturare sia dinamiche a breve termine sia pattern distribuiti su intervalli temporali più lunghi.

## 📊 Dataset

### Fonte

I dati sono stati raccolti da **SteamDB**:

[SteamDB](https://steamdb.info)

### Copertura

Il dataset comprende circa **350 videogiochi Steam**.

Per ciascun gioco sono stati utilizzati dati storici relativi a:

* **player count** giornaliero/orario;
* numero di **recensioni positive** giornaliere;
* numero di **recensioni negative** giornaliere;
* **prezzo** giornaliero in euro;
* **markers**, ovvero  eventi speciali spesso associati a picchi positivi o negativi dell’attività dei giocatori.

I dati vengono organizzati come serie temporali per ciascun videogioco, permettendo di studiare sia l'evoluzione temporale del singolo gioco sia la capacità dei modelli di generalizzare tra giochi differenti.


## 🧪 Confronto dei modelli

Le tre architetture vengono addestrate e valutate sullo stesso problema di forecasting, permettendo di confrontarne le capacità predittive.

Il notebook contiene il codice necessario per:

* preparazione e preprocessing dei dati;
* costruzione delle serie temporali;
* addestramento dei modelli;
* generazione delle previsioni;
* valutazione delle performance;
* confronto dei risultati ottenuti.

## 📓 Notebook

Il repository include il notebook:

```text
Steam_Player_Count_Forecasting.ipynb
```
Il notebook contiene l'implementazione completa dell'esperimento e i risultati ottenuti.
