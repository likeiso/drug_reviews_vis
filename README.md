# Assessment and Interactive Visualization of Semantic Similarity in User Reviews of Medications

Disclaimer: This project does not provide medical advice. It is intended for informational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. 

This project uses a dataset from Kaggle https://www.kaggle.com/rohanharode07/webmd-drug-reviews-dataset
The dataset provides user reviews on specific drugs along with related conditions, side effects, age, sex, and ratings reflecting overall patient satisfaction.
Data was acquired by scraping WebMD site (https://www.webmd.com/drugs/2/index). There are around 0.36 million rows of unique reviews and is updated till Mar 2020.

During EDA the distribution of length of reviews and number of reviews per drug were studied with help of histograms.

In order to select meaningful reviews for the training corpus reviews with lengths, less than 200 characters and more than 2000 characters were removed. Also, drugs with less than 20 reviews were deleted. The training corpus consists of documents and tags. In this case, each drug review is a document, and each review was tagged with that drug’s name.

This project is utilizing Gensim's doc2vec model. The model builds a space where each drug has its vector based upon the words within the collection of all reviews of that drug.

The model is capable of finding similar drugs based on semantic similarity of reviews. Also, it is possible to perform vector math with word vectors. Please see the notebook for examples.

To visualize the semantic similarity, a network graph of document embeddings was built. In this graph, nodes represent drugs, their color - number of reviews and edges similarity between drugs.

The final visualization is available here: https://oleksii.pythonanywhere.com/doc2vec
