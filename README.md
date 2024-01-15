# Spotify Million Playlist Dataset Challenge

Project demonstrates the following:
1. Strong understanding of Neural Networks and parameter optimization - both conceptually and in practice.
2. Strong mastery of Machine Learning concepts and mathematical principles - with the ability to properly apply different concepts to derive unique solutions.
3. Ability to conceptualize and find innovative solutions

---

The Spotify Million Playlist Dataset Challenge, hosted on AIcrowd, was to create an automatic playlist continuation program - which when given a seed track or list of seed tracks, the algorithm could predict the subsequent tracks in the playlist. 

This page consists of the report (with a hypothetical business case) aswell as the project code.

Link to code: [here](https://colab.research.google.com/drive/1h4QGD_gicP77keDdxGj_pRei-dbSfxBI?usp=sharing)
---

SUMMARY: Due to resource limitations, we were required to find a creative and innovative solution to accomplish this task, and did so with a unique blend of mathematical concepts. First, we constructed a co-occurrence matrix of every song in the database, which practically documented how often songs appeared together. Then utilizing a property of an item-to-item collaborative filtering system - similar to what is used on Netflix - we constructed the cosine similarity matrix for every song utilizing the co-occurrence matrix. Next, we constructed a feedforward neural network for multi-class classification - using the sparse-categorical crossentropy loss function. However, the loss function was testing the ability of the model to predict the top song, which is not really what we were after. Instead, we tuned the parameters utilizing the top 500 and top 100 song accuracy scores in the test data - which fits more practically with the purpose of the challenge. The top 5 performing neural networks are graphed below, with the best performing model achieving outstanding performance of 96% top 500 accuracy and 90% top 100 accuracy.

![mindBlownGraph1](https://github.com/logan-desmet/SpotifyMillionPlaylistDatasetChallenge/assets/150872110/ca519ea6-3361-47fc-ab3c-770b8c09a9ae)

---

### Note: Please download code file or visit colab file located [here](https://colab.research.google.com/drive/1h4QGD_gicP77keDdxGj_pRei-dbSfxBI?usp=sharing): - do not view the code directly on github as it is not formatted properly.
