# Objetivos

### 1. Aprender como representar un documento como un vector.


### 2. Conocer algunas aplicaciones de textmining tales como:

    2.1 Categorización de noticias.

    2.2 Recuperación de información.

    2.3 Descubrimiento de tópicos.


# Introducción

#### ¿Por qué los datos no estructurados son tan importantes?

Las empresas están tomando decisiones solo con el 20% de la información a la que tienen acceso, ya que el 80% de su información es no estructurada y no se puede utilizar completamente. Las compañías han tratado de darle sentido a los datos no estructurados por años, pero solo un 78% afirma que tienen poca o nula información de sus datos no estructurados.

http://fredrikstenbeck.com/unstructured-data-important/

Fuentes de datos no estructurados en las empresas:
1. Medios de comunicación social. Ej: mención de una compañía o un producto en redes sociales.
2. Fuentes internas. Ej: Presentaciones, material de marketing y ventas, informes, correo electrónico, etc.
3. Contenido generado por el cliente. Ej: Comentarios en línea, historial de navegación, correos electrónicos a un equipo de soporte e incluso llamadas telefónicas al servicio al cliente.

#### ¿Cómo trabajamos con datos no estructurados?

**Embedding**: Llevar datos a una representación númerica. Los modelos trabajan con representaciones númericas!.
Además, con vectores tenemos nociones de distancia y podemos calcular similitud (o disimilitud) entre vectores.

En *text mining* existen dos tipos de *Embedding*, basados en frecuencia y en predicción.

Algunas *keywords*:

1. **Documento (D)**: se refiere a una observación de tipo texto. Ej: comentario, relato, email, etc.
2. **Corpus (C)**: colección de documentos, corresponde al conjunto de datos.
3. **Vocabulario (V)**: corresponde a un conjunto de términos (tokens únicos normalizados) dentro del corpus que sobrevivieron a un procesamiento.
4. **Tokenization**: dividir el texto en entidades significativa llamadas tokens, si cada token es una palabra se habla de unigrams, si cada token son pares de palabras se habla de bigrams, tres palabras son trigrams, así hasta n-grams. En términos más computines es pasar de un string a una lista de strings.
Ejemplo de unigrams:

*'Buenos días estudiantes buenos' = ['Buenos', 'diás', 'estudiantes', 'buenos']*


## Requisitos

```python
- python                    3.7
- numpy                     1.16
- pandas                    0.24
- matplotlib                3.1
- scikit-learn              0.21
- numba                     0.44
- joblib                    0.13
- gensim                    3.4
- nltk                      3.4
- spacy                     2.1
- pyemd                     0.5
- pyldavis                  2.1
```

## Notas

1. Para el capítulo de Information Retrieval es necesario descargar ``FastText embeddings from SBWC`` en el siguiente link de descarga https://github.com/dccuchile/spanish-word-embeddings.
  - Existen dos formas de cargar los vectores, primero es cargar todos los vectores desde el archivo binario (.bin) en su formato nativo de FastText (**opción recomendada**). Esta opción es más demandante en recursos (tiempo y memoria), pero es mucho más versatil por ejemplo para obtener vectores para palabras que no se ecuentran en el vocabulario.
  - La segunda forma, mucho más rápida, es cargar sólo una parte de los vectores. Para esto usamos el formato nativo de word2vec y cargamos una cantidad fija de vectores (se pueden cargar vectores generados por diversos métodos como FastText).

2. Para visualizar en el repo la visualización de LDA ir a http://htmlpreview.github.io/ y pegar la url de ``lda.html`` que esta en la carpeta ``/img``.
