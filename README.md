### Dependence 
Our codes in this package have been tested with
  1. Python 3.7
  2. RDFLib 4.2.2
  3. gensim 3.8.0
  4. scikit-learn 0.21.2
  5. nltk 3.5
  6. OWLready 0.25
  
 Acknowledgement: 
 codes under rdf2vec/, which mainly implement walking strategies over RDF graph, 
 come from [pyRDF2Vec](https://github.com/IBCNServices/pyRDF2Vec) (version 0.0.3, accessed in 03/2020), with some updates made.

### Standalone Application
The standalone application (v0.1.0) can be run by the two main programs.

1. OWL2Vec\_Standalone.py

    This program will embed one ontology. It can be configured by the configuration file default.cfg. See the examples and comments in default.cfg for the usage.

    Running example: ```python --config_file default.cfg```

    Note: Different from the experimental codes, the standalone program has implemented all OWL ontology relevant procedures in python with Owlready, but it also allows the user to use pre-calculated annotations/axioms/entities/projection for generating the corpus. 

2. OWL2Vec\_Standalone_Multi.py

    This program will embed multiple ontologies into one language model, where the documents from multiple ontologies will be merged. One use case example is embedding all the conference relevant ontologies of the OAEI conference track by once.

    Running example: ```python --config_file default_multi.cfg```

    Note: Different from OWL2Vec\_Standalone.py, this program for multiple ontologies does NOT allow the pre-calculated or external annotations/axioms/entities/projection.

### Experiment Codes
The folder **experiments/** includes data and codes used in our paper "OWL2Vec\*: Embedding OWL Ontologies". 
Note the ontology relevant operations in the experiment codes, such as annotation extraction and ontology projection, are implemented by Java OWL APIs.
For a pure python implementation, please use the standalone application.

### Publication
Chen, Jiaoyan, Pan Hu, Ernesto Jimenez-Ruiz, Ole Magnus Holter, Denvar Antonyrajah, and Ian Horrocks. [****OWL2Vec\*: Embedding of OWL ontologies****](https://arxiv.org/abs/2009.14654). Machine Learning, Springer, 2021. (accepted).
