# Entity Alignment between Knowledge Graphs
An open-source framework for aligning the same real-world entities in different knowledge graphs.

# Content
1. KBA.ipynb
2. data/

# Requirement
1. Python (>=2.7)
2. Numpy (>=1.13.3)
3. TensorFlow (>=1.4.1)
4. CUDA (>=9.0)
5. Matplotlib (>=2.0.0)
6. scikit-learn (>=0.18)

# Predicate alignment
To obtain the best entity alignment performance, our model requires a predicate alignment pre-processing step as follows:

1. Install python-Levenshtein
        
        pip install python-Levenshtein
        
2. Compute the similarity of all possible predicate pairs between two KGs. To compute the similarity, you can use the following command:
        
        import difflib
        ...
        pred_similarity=difflib.SequenceMatcher("predicate_1", "predicate_2").ratio()
        ...
        
3. Filter the predicate similarity (*pred_similarity*) using a certain threshold. We use the threshold of 0.95.
4. Manually check the final result.

# References
Bayu Distiawan Trisedya, Jianzhong Qi, Rui Zhang. [**Entity Alignment between Knowledge Graphs Using Attribute Embeddings.**] AAAI 2019.