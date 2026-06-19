# penguins-analysis-project
# Analisi Statistica e Predittiva sul Palmer Penguins Dataset

Analisi dati end-to-end sul celebre dataset *Palmer Penguins*, sviluppata a conclusione del corso professionale ["Elementi di Data Analytics"](https://immaginazioneelavoro.it/prodotto/elementi-di-data-analytics/).

## Competenze Tecniche Dimostrate

* **Linguaggio e Stack:** Python (Pandas, NumPy, Matplotlib, Seaborn).
* **Statistica e Inferenza:** SciPy, Statsmodels.
* **Data Cleaning:** Individuazione dei NaN, rimozione mirata e Data Imputation basata su metriche statistiche (classificazione *nearest-centroid* tramite z-score).
* **Data Transformation:** Discretizzazione di variabili continue tramite la regola di Sturges e codifica di variabili categoriche.
* **Analisi Bivariata e Statistica:** Test Chi-Quadro, V di Cramer, Indice Eta-Quadro (η²), Covarianza e Correlazione lineare (Pearson).
* **Machine Learning:** Regressione Lineare Semplice (OLS).


## Struttura del Progetto

1. **Importazione e analisi esplorativa:** Caricamento del dataset e studio iniziale della fisionomia dei dati, identificando le variabili biometriche (becco, pinne, massa corporea), le variabili categoriche (specie, isola, sesso) e la presenza di record incompleti.
2. **Visualizzazioni esplorative:** Studio grafico delle distribuzioni per sesso e specie tramite scatterplot e istogrammi. In questa fase è stato identificato e analizzato il **Paradosso di Simpson** nella relazione tra lunghezza e altezza del becco, dove la segmentazione per specie inverte il trend complessivo dei dati.
3. **Preparazione dei dati (tipi, codifiche, classi):** Controllo della consistenza dei tipi di dato, codifica delle variabili categoriche e discretizzazione delle variabili continue (utilizzando la **Regola di Sturges** per determinare il numero ottimale di intervalli/bin).
4. **Pulizia dei dati (missing value):** Gestione avanzata dei dati mancanti. Invece di una cancellazione generica, i valori nulli relativi al sesso dei pinguini sono stati imputati applicando una classificazione *nearest-centroid* basata sullo z-score della massa corporea rispetto alle distribuzioni note per specie e sesso.
5. **Analisi statistica (covarianza, correlazione, indipendenza, eta quadro):** Quantificazione matematica delle relazioni tra variabili:
   * Covarianza e correlazione lineare di Pearson per i tratti biometrici.
   * Test del **Chi-Quadro** e **V di Cramer** per misurare la dipendenza tra l'isola di provenienza e la specie.
   * Calcolo dell'indice **Eta-Quadro ($\eta^2$)** per quantificare quanta varianza della massa corporea sia spiegata rispettivamente dal sesso e dalla specie.
6. **Regressione lineare:** Sviluppo, calcolo e visualizzazione di un modello di regressione lineare semplice (OLS) per stimare la lunghezza della pinna in base alla massa corporea. La retta stimata è stata validata attraverso lo studio del coefficiente $R^2$ e l'analisi visiva dei residui.
7. **Conclusioni:** Sintesi dei principali insight emersi dal punto di vista biologico e statistico (es. la forte associazione tra specie e habitat specifico, e il fatto che la specie spieghi la varianza del peso in misura molto maggiore rispetto al sesso), validando l'efficacia dei modelli applicati sul dataset finale.
