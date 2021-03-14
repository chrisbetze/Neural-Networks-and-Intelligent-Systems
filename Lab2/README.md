# Unsupervised Learning
## Application 1: Content-based film recommendation system
Based on what user like, the algorithm will simply pick items with similar content to recommend him.
![MicrosoftTeams-image](https://user-images.githubusercontent.com/50949470/111079410-97508f00-8502-11eb-9dc5-4d55c79ff454.png)

### Dataset preview
Consists of 42,306 movie plot summaries extracted from Wikipedia and aligned metadata extracted from Freebase.

### Discription - Steps
* Convert corpus to TF-IDF representation. (Term Frequency–Inverse Document Frequency is a numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus.)
* Remove common words, pronouns, articles, names etc.
* Natural Language Processing
* Stemming and Lemmatization techniques with Porter, Lancaster και Snowball.

### Example result
```
Input movie: "The Ward", in categories ["Thriller", "Psychological thriller", "Horror", "Haunted House Film", "Supernatural"]
1) Recommended: "Day of the Dead 2: Contagium", in categories ["Zombie Film", "Horror"]
2) Recommended: "Forget Me Not", in categories ["Thriller", "Horror", "Teen"]
3) Recommended: "Shake, Rattle & Roll 13", in categories ["Thriller", "Drama", "Horror"]
4) Recommended: "Room 6", in categories ["Horror"]
```

## Application 2: Topological and semantic representation of films using Self-Organizing Map
![68747470733a2f2f692e696d6775722e636f6d2f5a3446647572442e6a7067](https://user-images.githubusercontent.com/50949470/111079327-3b860600-8502-11eb-9071-22d09e94ee57.jpg)
