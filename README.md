# Heart Disease Diagnosis — Decision Tree

Analisi predittiva su un dataset clinico ("Heart Disease", UCI Machine Learning Repository, 303 soggetti, 14 variabili) volta a identificare i migliori predittori demografici, fisiologici e biologici della presenza di malattia cardiaca.

## Contenuto

- `analysis.Rmd` — codice R completo: pulizia dati, analisi esplorativa, correlazioni, modello Decision Tree (rpart), tuning degli iperparametri, valutazione delle performance
- `report.pdf` — report finale con grafici e commento dei risultati
- `data/heart.csv` — dataset utilizzato

## Metodo

- Preprocessing e gestione missing values
- Analisi esplorativa (distribuzioni, relazioni fra variabili, matrice di correlazione)
- Modello Decision Tree (`tidymodels` + `rpart`), con cross-validation 10-fold
- Tuning di `cost_complexity`, `tree_depth`, `min_n`
- Valutazione tramite accuracy, ROC AUC, matrice di confusione

## Risultati principali

- Accuracy sul test set: ~0.82, ROC AUC: ~0.88
- Le variabili più predittive sono risultate la talassemia (tipo di difetto), il numero di vasi principali visibili con fluoroscopia e la depressione del segmento ST

## Strumenti

R, tidyverse, tidymodels, rpart, ggplot2, corrplot
