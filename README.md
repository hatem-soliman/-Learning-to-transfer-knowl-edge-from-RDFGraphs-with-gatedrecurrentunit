# -Learning-to-transfer-knowl-edge-from-RDF-Graphs-with-gated-recurrent-unit
The speedy evolution of the Internet has brought up practical issues such as the problem of information retrieval. Several methods have been proposed to solve this issue. Such approaches retrieve the information by using SPARQL queries over the Resource Description Framework (RDF) content which requires a precise match concerning the query structure and the RDF content. In this work, we developed a transfer learning-based neural learning method that helps to search RDF graphs to provide probabilistic reasoning between the queries and their results. The problem is formulated as a classification task where RDF graphs are preprocessed to abstract the N-Triples, then encode the abstracted N-triples into a transitional state that is suitable for neural transfer learning. Next, we fine-tune the neural learner to learn the semantic relationships between the N-triples. To validate the proposed approach, we employ ten-fold cross-validation. The results have shown that the anticipated approach is accurate by acquiring the average accuracy, recall, precision, and f-measure.

Overview

The suggested method performs the estimation of RDF graph information retrieval in the following manner:

(1) The history-data of RDF graphs are first validated and then reused for the purpose of model training.
(2) Next to abstract a generalized feature state, we perform lemmatization, word inflection, and stop word removal.
(3) Then we make a global vocabulary system to limit the out-of-vocabulary words.
(4) Afterwards, we convert the abstracted features into vector encoded form that can be used for model training purposes.
(5) Finally, we train transfer learning-based neural model that learned to predict RDF graphs being retrieved.

Preprocessing

It is vital to validate the syntax of each RDF graph thus, we use the Apache Jena API http:/jena.apache.org/) to validate each RDF graph. Next, the valid RDF graphs are loaded into the model to transform it from RDF to N-triple serialization. We analyze all the documents for feature extraction and to build the classification model for information retrieval. We employ the natural language preprocessing techniques (Word inflection, lemmatization, and Stop word removal) to normalize the abstracted features. We employ the
Natural Language Toolkit (NLTK - http://www.nltk.org/) of Python for these tasks. To transform words into their base-form that are superlative and comparative we utilize lemmatization. The Word inflection singularize a given word into its base form and as the name suggests stop word removal helps to remove the stop words. Next for the model training purpose, we build a global vocabulary system in which each unique word corresponds to a positive integer value that helps to transform the features into a vectorized shape that is suitable for model preparation. The vectorization process results in an n-dimension matrix. in which each row represents.

Deep Transfer Learning

In transfer learning, the information learned during solving one problem is transferred and fine-tuned for another related problem. In recent years, transfer learning methods have applied in several fields such as metric learning, machine learning, image and text classification and dimensional reduction. The pre-trained neural model is then used to transfer knowledge from RDF graphs. The model is trained for information recovery prediction of RDF graphs with the blend of word2vec embedding technique combined with convolutional neural network (CNN) for the succeeding causes, we choose the convolutionary neural network: 1) it is capable of learning deep semantic relationship among terms;
2) by applying different filter sizes And avoids the gradient issue of the repeated neural network.

Fine tuning with Gated Recurrent Unit

An important understanding of the anticipated approach is to freezing the knowing information and then fine-tune it with fresh knowledge. For this purpose, we utilize the GRU based recurrent neural network. The GRU learner pays consideration to the RDF-specific features to accomplish optimum performance. The dataset is compiled from DBpedia (https:/wiki.dbpedia.org/data-set-30). The 2016-10 DBpedia release comprises 13 billion kinds of information. Of these, 1.7 billion were obtained from the Wikipedia English edition.
