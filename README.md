# Outline
## Introduction
## Distribution and cleaning
- TMDB vote count needs to remove movies with vote_count less than some value.
- something with cofidence intervals maybe
- maybe:(revenue, log)
## Attributes' effect on revenue/rating (generelt linear regression i det her)
### Genders
### Original language
- try with English, probably conclude that english is the most sought after in terms of revenue/rating.
- do it without english
- Linear regression
### Genres
- find top 10/20
- Linear regression
- rød tråd to NLP
## NLP
### CLustering
- Take each cluster assign it a genre
- compare some stuff
### Bag-of-words 
### Word2Vec
### Sentiment analysis
- See if the sentiment has any effect on revenue/rating

## Conclusion


# ADA Template Website
## Usage
1. Fork (copy) this repository by clicking the "Fork" button on the top right corner.
2. Go to "Settings" -> "Pages" in your forked repository. Under "Branch" change "None" to "master" and click "Save".
3. Edit the `_config.yml` file in your forked repository to change the site title (after `title:`) and description (after `description:`).
4. Build your own page by editing this `README.md` (home page) and creating new `.md` files (other pages), formatting is done with standard [GitHub Markdown syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax), we provide an example file `example.md` in the repository.
**Important**: Please include ```--- layout: default ---``` (the first three line in `example.md`) at the beginning of your every newly created `.md` file.
5. Add your new `.md` files to the site by editing the `_config.yml` file in your forked repository. Under `navigation:` add a new pair of `- title:` and `url:`, and fill their value with your page name and `.md` file name. Remember to remove the `- title:` and `url:` pair for the example page.
6. Go back to "Settings" -> "Pages" to find your website link.
