
# G.E.V.I.R

# Project Name
Deductive analysis of PERC Proceedings articles at scale using text embeddings

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Description

Our repository and the notebooks and data contained should be read in relation to the research paper *Using Text Embeddings for Deductive Qualitative Research at Scale in Physics Education*, by Tor Ole Odden, Halvor Tyseng, Jonas Timmann Mjaaland, Markus Fleten Kreutzer, and Anders Malthe-Sørenssen at the University of Oslo, Norway. The article is available on arXiv and is currently under submission to Physical Review Physics Education Research. The notebook acts as supplementary material for interested readers to reproduce the results and to understand the methodology used in the paper. Most of the figures in the article are produced in the notebook. 

------------

Qualitative analysis is a cornerstone of social science research, used in fields as diverse as education research, sociology, history, and business. Traditional qualitative analysis, however, is time consuming, labor intensive, and difficult to scale and replicate. To tackle these issues, we have devised a fast, replicable, and scalable technique for deductive, qualitative research on text-data, by utilizing novel advances in machine learning and artificial intelligence.
 
To prove the concept, we thematically analyze 23 years of the Physics Education Research Conference proceedings literature. First, using a natural language processing technique known as embedding, we create vector-based representations of texts in a high-dimensional meaning space. Then we define topics, derived from a review of the physics education research literature by Docktor and Mestre (2014). To project these topics into the meaning space, we define them as centroids of representative domain-expert determined articles’ embedding vector. Thereafter, we calculate the distances between every article and centroid, and use the inverted, scaled distances between these centroids and articles to create a topic model. Based on this analysis, we critically discuss the features, uses, and limitations of this method and argue that it holds promise for flexible deductive qualitative analysis of a wide variety of text-based data that avoids many of the drawbacks inherent to prior NLP methods.

Our methodology is based on the following steps:
0. Collect, clean and prepare our data
1. Use a pre-trained text embedding model to transform the text of the papers into vectors
2. Define the different topics you want to explore
3. For each topic pick out a number of articles that are representative of the topic
4. Calculate the mean of the representative articles in the topic, this will be the representative vector of the topic called centroid
5. For each article in you dataset, calculate the distance in vector space from our embedded article to the centroid of the topic
6. Transform this distances into scores, by scaling, inverting and normalization
7. Do analysis of your data by utilizing the scores

### Table of contents
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
## Installation

To run the notebook, numpy version 1.26.1 is required. There are also several imports, notably: 

    # Basic imports
    import numpy as np
    import matplotlib.pyplot as plt
    import pickle
    import pandas as pd
    import scipy as sc

    # Special imports for plots
    import string
    import seaborn as sns
    import matplotlib.patches as mpatches
    from matplotlib.ticker import PercentFormatter
    import matplotlib.colors as mcolors

## Usage

The notebooks run as they are. Enter a notebook by clicking on it, and press "Run All" on the top banner. 

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

Any and all questions can be sent to either: 

halvorty@uio.no
markusfk@uio.no
jonastm@uio.no

