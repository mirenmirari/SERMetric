# PISNER

PISNER (Plena inclusión Spanish News Easy-to-Read) is a parallel dataset for E2R text adaptation in Spanish.
This dataset is based on news articles published on the [Plena inclusión](https://www.plenainclusion.org/noticias/) and [Plena inclusión La Rioja](https://www.plenainclusionlarioja.org/actualidad/noticias) websites until February 4, 2025.
Both websites publish news item in two versions: a standard text and its corresponding E2R adaptation, produced and validated by experts in the field.
The dataset contains 1,180 valid text pairs. Table 1 presents descriptive statistics of the dataset.
It is publicly available on [Hugging Face](https://huggingface.co/datasets/mirari/PISNER) and it is divided into two parts: 80% for training and 20% for testing, corresponding to 944 and 236 news items, respectively.

|  | Sentences | Words   | Average words/sentences | Special character | Average syllables|
| --- | :----: |:---:|:---:|:---:|:---:|
|Standard text | 21,007 | 545,996 | 29.03 | 69.278 | 2.15 |
| Easy-to-Read text | 11,497 | 160,972 | 16.15 | 19.449 | 2.11 |

# SERMetric

SERMetric is an [open-source library](https://pypi.org/project/sermetric/) for evaluating how easy-to-read a text is. It supports a wide variety of indexes and allows the user to easily combine them.

To evaluate readability, different types of indexes can be considered. Orthographic indexes measure writing aspects such as the number of puntuacion marks. Syllabic indexes focus on the syllabic structure of words. Lexical indexes analyse vocabulary-related properties, including lexical richness and the frequency of common or rare words. Syntactic indexes capture the complexity of grammatical structures. The Fernández-Huerta formula estimate the overall difficulty of a text. Finally, cosine similarity measures textual similarity between two texts.

pointsIndex: it is the number of points in the text divided by the number of words.

newParagraphIndex: it is the number of new paragraphs in the text divided by the number of words.

CommaIndex: the number of commas in the text divided by the number of words.

extensionIndex: ratio between the number of syllables in lexical words and the number of lexical words, lexical words being understood as nouns, verbs, adjectives and adverbs.

triPoliIndex: ratio of the number of trisyllabic and polysyllabic words to the number of lexical words.

lexicTriPoliIndex: ratio of the number of trisyllabic and polysyllabic lexical words to the numberof lexical words.

diversityIndex: ratio between the number of different words in the text and the total number of words.

lexicalFreqIndex: ratio between the number of low-frequency lexical words and the number of lexical words. The “Corpus de la Real Academia Española” (CREA) and the ‘Gran diccionario del uso del español actual’ will be used as a reference.

wordForPhraseIndex: quotient resulting from the division between the number of words in the text and the number of sentences.

sentenceComplexityIndex: the result of dividing the number of sentences by the number of propositions.

complexityIndex: quotient between the number of low-frequency syllables and the total number of syllables (reference: ‘Diccionario de frecuencias de las unidades lingüísticas del castellano’)

fernandezHuerta: is the result of 206.84-0.6P-1.02F, where P is the number of syllables per 100 words and F is the number of sentences per 100 words.
