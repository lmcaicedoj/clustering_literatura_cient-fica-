# clustering_literatura_cientfica
Resumen: Técnicas de minería de datos basados en clustering y análisis de tendencias en el conjunto de datos de investigación abierta de COVID-19 (CORD-19) con el fin de identificar patrones emergentes y tendencias significativas en la literatura científica relacionada con COVID-19, SARS-CoV-2 y coronavirus.

Este Proyecto de  "Clustering de artículos academicos sobre COVID19" consiste en identificar cluster 
y temas comunes entre un conjunto considerable de documentos.
En este caso particular se estudiaron 50 mil documentos. 
El notebook de Jupyter esta dividido en las siguientes secciones: 
(0) Instalacion e importe de librerias: 
Aqui se instalaron librerias como Sentece-transformers, torch, nltk, langdetect, sparknlp, gensim y WordCloud. 

(1) Lectura y Extracion de datos:
Aqui se leyo el archivo donde estaban todos los datos de interes "metadata.csv". 

(2) Seleccion y limpieza del data set de interes:
Aqui se utilizaron varias librerias para escoger solamente los abstracts de los documentos escritos en el idioma ingles.
Se obtuvo un total de documentos con esas caracteristicas de 49127.

(3) Preprocesamiento: 
Aqui se utilizaron varias librerias para conversion de texto a minusculas y eliminacion de caracteres no alfabeticos y stopwords.

(4) Tokenizacion de Oraciones y Computo de Embeddings: 
En esta etapa, se toma el texto completo y se divide en oraciones individuales. Esto generalmente se hace para facilitar el procesamiento y análisis del texto. Luego, los embeddings son representaciones numéricas de palabras o frases que capturan información semántica. En esta etapa, se asignan	vectores numéricos a cada palabra o token en el texto, de manera que palabras similares tengan representaciones similares en el espacio vectorial. Esto puede hacerse utilizando modelos de word embeddings pre-entrenados como Word2Vec, GloVe o embeddings contextuales como BERT.

(5) Preparacion de vectores numericos:
En esta etapa, los vectores numéricos obtenidos en la etapa anterior se preparan para su posterior procesamiento. Esto puede incluir normalización, reducción de dimensionalidad (por ejemplo, mediante técnicas como PCA o t-SNE), o cualquier otro preprocesamiento necesario para adaptar los datos a los algoritmos que se utilizarán en las etapas posteriores.

(6) Clusterizacion: La clusterización es un proceso mediante el cual se agrupan datos similares en grupos o clústeres. En el contexto del procesamiento de texto, se utilizan algoritmos de clusterización para agrupar documentos o texto similar en categorías o temas. Algunos algoritmos comunes para la clusterización de texto incluyen el clustering k-means usado en este proyecto.
	
(7) Distribucion de Topicos: Aplicacion de Latent Dirichlet Allocation(LDA)
LDA es un modelo probabilístico ampliamente utilizado en el análisis de texto para identificar tópicos latentes en un conjunto de documentos. En esta etapa, se aplica el modelo LDA a los documentos o texto para descubrir la distribución de tópicos en cada documento y las palabras clave asociadas a cada tópico. Esto permite comprender la estructura temática subyacente en el corpus de texto y categorizar los documentos en función de los tópicos identificados.


Nota: Es importante resaltar que este codigo se corrio en la plataforma en la nube de AZURE, donde se consumieron recursos de USD$100 aproximadamente.
Estos recursos se utilizaron para el adjuste del codigo y correrlo varias veces hasta obtener todas las graficas deseadas. 

