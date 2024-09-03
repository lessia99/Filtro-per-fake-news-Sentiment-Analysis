# Filtro-per-fake-news-Sentiment-Analysis

Il problema delle fake news è cresciuto esponenzialmente nell'ultimo decennio a causa della crescente diffusione dei social network, il governo degli Stati Uniti ha deciso di muoversi a tal proposito, incaricando un'azienda di realizzare un plug-in per chrome in grado di riconoscere se una notizia è falsa. L'obiettivo è quello di realizzare il modello in grado di riconoscere le notizie false, che poi il team di machine learning enginner e web developer metterà in produzione. Si hanno a disposizione due raccolte di notizie, una contenente solo notizie false e l'altra contenente solo notizie vere, si utilizzeranno per addestrare il modello.

Da un'accurata analisi, si può rispondere a domande come:
1. le fake news sono più frequenti in una determinata categoria?
2. per ogni categoria, ci sono argomenti che sono più soggetti alle fake news?
3. I titoli delle fake news presentano dei pattern?

## Data
1. **datasets**:I dataset usati sono uno contente solo notizie vere, True.csv, e uno solo notizie false, Fake.csv. Si possono scaricare al seguente link:

(DA GUARDARE)

2. **Fake_news_detection.ipynb**: file che contiene l'analisi

## Dettagli analisi e modelli usati

Dopo aver scaricato i file e averli caricati, estraggo dal dataset fake le variabili 'title', 'text','subkect' che mi serviranno per il modello. 

1. **Data preprocessing**:
  - Topic modelling sul dataset fake, in particolare eseguo la LDA.
  - Concateno le notizie false e vere, e creo una nuova colonna 'label', true=1 fake=0, così da avere un nuovo dataset. Controllo che i dati siano bilanciati.
  - Analisi preliminari: controllo eventuali valori nulli, capisco come è strutturato il dataset.
2.**WORD CLOUD**: controllo la frequenza delle parole nel dataset fake e in quello true.
3.**Classificazione**:
    - divido il dataset in train e test
    - converto il testo in vettore tramite Tf-idf Vectorizer
4. **Modello Multinomiale NB**
4. **Regressione Logistica**
5. **Decision Tree**

Per valutare tutti e tre i modelli ho usato l'accuracy e la matrice di cofusione.

## Prerequisiti e utilizzo

- Ultima versione di Python disponibile
- per caricare e usare i file, runnare le seguenti  righe all'interno del notebook:

!wget https://proai-datasets.s3.eu-west-3.amazonaws.com/fake_news.zip
!unzip fake_news.zip

- Installare e/o importare le seguenti librerie
  - pandas
  - genim
  - nltk
  - pprint
  - seaborn
  - matplotlib.pyplot
  - wordcloud
  - sklearn
 
All'iterno del notebook si troveranno i commenti e le conclusioni finali.
   
## Contatti
Per domande, suggerimenti o feedback, contattatemi pure alla mail alessiaagostini53@gmail.com.

https://proai-datasets.s3.eu-west-3.amazonaws.com/fake_news.zip

