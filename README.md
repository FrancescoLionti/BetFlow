# BetFlow: Analisi di Satoshi Dice (Bitcoin Betting)
**Studente:** Francesco Lionti 
**Corso:** Laboratorio di WebScraping

## Breve Introduzione
Questo progetto consiste in un'analisi approfondita di Satoshi Dice, uno dei primi e più celebri servizi di betting basati su Bitcoin. Sfruttando tecniche avanzate di data processing, network analysis e web scraping, l'analisi si concentra sul traffico on-chain dell'anno 2012 per esplorare l'impatto del servizio sull'intero ecosistema Bitcoin. 

Il progetto affronta diverse sfide analitiche, tra cui:
* **Ottimizzazione delle risorse:** Riduzione dell'impronta in RAM dei dataset di grandi dimensioni tramite tecniche di data downcasting e l'uso del motore di parsing PyArrow in C++.
* **Analisi dei volumi e dei comportamenti:** Studio dell'incidenza delle scommesse sul traffico globale (che nel 2012 arrivava a toccare picchi giornalieri superiori al 40% del traffico totale Bitcoin) e analisi della reattività del servizio (latenza tra bet e payout).
* **Individuazione di Bot/Script:** Analisi degli intervalli temporali tra giocate consecutive, che ha rivelato un ecosistema dominato da scommesse automatizzate ad altissima frequenza (intervalli sub-minuto).
* **Network Analysis e De-anonimizzazione:** Ricostruzione delle catene di transazioni (che obbediscono a una distribuzione a Power Law) e scraping dinamico tramite Selenium e fake_useragent su WalletExplorer.com per de-anonimizzare e individuare le macro-entità dominanti della rete.

## Documentazione (Relazione di Progetto)
Per comprendere a fondo l'architettura del codice, le logiche di merge tra i dataframe, le scelte tecniche (metriche, aggregazioni, studio delle distribuzioni logaritmiche) e l'interpretazione completa dei risultati e dei grafici generati, si prega di leggere il file: 

**BetFlow_Lionti_Francesco.pdf**

La relazione contiene tutti i dettagli sull'implementazione, dallo smoothing delle serie storiche alla configurazione del browser (headless) per superare i sistemi anti-scraping.

## Requisiti 
Il progetto è sviluppato interamente su Jupyter Notebook.

## Download del Dataset e Avvio
A causa delle dimensioni elevate, il dataset completo originale non è incluso direttamente in questa repository per evitare limiti di caricamento.

Per eseguire correttamente il notebook, segui questi passaggi:

1. Scarica il dataset completo dal seguente link Google Drive: 
   https://drive.google.com/drive/folders/10HjNX1Uds5Kpz9OkCOFyZstSNbjbAl5C?usp=sharing
2. Estrai i file scaricati e posizionali nella cartella prevista dal notebook (es. crea una cartella `dataset/` nella stessa directory del file `.ipynb`).
3. Avvia l'ambiente Jupyter aprendo il terminale nella directory del progetto ed eseguendo:
   ```bash
   jupyter notebook
   ```
4. Apri il file .ipynb dall'interfaccia web di Jupyter, assicurati che i percorsi di lettura dei file puntino alla cartella in cui hai salvato il dataset e, infine, esegui le celle in ordine sequenziale.
