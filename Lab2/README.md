# Unsupervised Learning
## Application 1: Content-based film recommendation system
Based on what user like, the algorithm will simply pick items with similar content to recommend him.
![MicrosoftTeams-image](https://user-images.githubusercontent.com/50949470/111079410-97508f00-8502-11eb-9dc5-4d55c79ff454.png)

### Dataset preview
Consists of 42,306 movie plot summaries extracted from Wikipedia and aligned metadata extracted from Freebase. For more info click [here](http://www.cs.cmu.edu/~ark/personas/)

### Description - Steps
* Convert corpus to TF-IDF representation. (Term Frequency–Inverse Document Frequency is a numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus.)
* Remove common words, pronouns, articles, names etc.
* Natural Language Processing (NLP)
* Stemming and Lemmatization techniques with Porter, Lancaster και Snowball.

### Example result
```
Input movie: "The Ward", in categories ["Thriller", "Psychological thriller", "Horror", "Haunted House Film", "Supernatural"]
1) Recommended: "Day of the Dead 2: Contagium", in categories ["Zombie Film", "Horror"]
2) Recommended: "Forget Me Not", in categories ["Thriller", "Horror", "Teen"]
3) Recommended: "Shake, Rattle & Roll 13", in categories ["Thriller", "Drama", "Horror"]
4) Recommended: "Room 6", in categories ["Horror"]
```

## Application 2: Topological and semantic representation of movies using Self-Organizing Map
We make a two-dimensional map (grid), where movies of the dataset displayed in a spatially coherent way in terms of their content and their genre.<br>
![68747470733a2f2f692e696d6775722e636f6d2f5a3446647572442e6a7067](https://user-images.githubusercontent.com/50949470/111079327-3b860600-8502-11eb-9071-22d09e94ee57.jpg)

### Description - Steps
* Creating the dataset: Each film is represented in the Vector Space Model by the features of TF-IDF and its genres.
* Training the Self-Organizing Map (SOM) using [Somoclu](https://somoclu.readthedocs.io/en/stable/index.html) library.
* Clustering using k-Means scikit-learn algorithm.
* SOM visualization using the Unified Distance Matrix (U-matrix).
* SOM optimization using different numbers of neurons (grid size) and clusters.

### Results - Semantic Interpretation of Clusters
For the final-optimal SOM produced for our dataset, we make data exploration for clusters which have topological relevance to surrounding areas. We also study the topological properties of SOM and whether or not they have incorporated semantic information about movies, through TF-IDF representation and genres.
