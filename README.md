# Regression-Analysis
Progetto finalizzato per sviluppare dei modelli di predizione su un dataset relativo a misure svolte su campioni di biomassa prelevati da centrali elettriche che usano la biomassa come carburante.
## Ambiente di sviluppo
Rapid Miner
## Dataset
Il dataset utilizzato è un foglio in formato Excel (.xlsx) composto da 5217 record (righe) relativi alle singole misurazioni effettuate in laboratorio e dai seguenti 18 attributi (colonne), in elenco, corrispondenti ai vari parametri misurati durante ciascuna combustione:
- ID CAMPIONE
- CENTRALE
- INFO (campo descrittivo)
- MATERIALE (descrive la tipologia di biomassa)
- GRUPPO ISO (raggruppa diversi materiali)
- DATA RICEVIMENTO (campo descrittivo)
- UMIDITA’
- PCN
- CENERI
- PCS
- PCI
- CARBONIO
- IDROGENO
- AZOTO
- OSSIGENO
- CLORO
- ZOLFO
- UMIDITA’ DI CORREZIONE
## Goals
Il nostro progetto si propone di raggiungere i 3 seguenti Goal:
1. dato il valore della feature CENERI predire per ogni materiale i valori di PCS, PCI, Azoto, Cloro e Zolfo [quindi un modello di regressione per ogni materiale e per ognuna delle 5 feature indicate].
2. dati i valori delle feature CENERI, CARBONIO, IDROGENO E AZOTO, per ogni materiale predire i valori di PCS, PCI, CLORO e ZOLFO [anche in questo caso diversi modelli di regressione].
3. date tutte le feature relative a misure, per ogni materiale predire i valori di PCS,PCI, CLORO e ZOLFO.
Con l’obiettivo finale di individuare i modelli di predizione che restituiscano, per ognuno dei Goal, i risultati migliori, secondo le misure di “Root Mean Squared Error” (“RMSE”) e relativa varianza (standard deviation). (si veda il punto 6b della sezione “Implementazione”).
## Algoritmi utilizzati
Si è optato per l’utilizzo degli algoritmi:
- Decision Tree;
- Random Forest;
- SVMdot;
- SVMradial;
- SVMpolynomial;

con generazione del modello di predizione tramite addestramento basato su X-Fold Cross Validation, su cui sono stati utilizzati 10 Folds.
