# Wikipedia Search Engine

A custom information retrieval project that builds a search engine over a curated Wikipedia dataset and evaluates ranking strategies on topical Wikipedia articles. The project explores classic retrieval methods, text preprocessing, dataset construction, and relevance-based ranking using techniques commonly used in search and recommendation systems.

## Overview

This repository contains a notebook-based workflow for:

- Collecting a focused set of Wikipedia articles across major technology topics
- Building a document corpus from article titles and content
- Cleaning and preprocessing text for IR pipelines
- Evaluating search quality with multiple ranking strategies
- Exploring retrieval models such as TF-IDF, BM25, and language-model scoring
- Preparing a dataset summary for downstream analysis

The project is designed as a practical study in information retrieval and search ranking, using real Wikipedia content and a topical corpus spanning domains including artificial intelligence, machine learning, cloud computing, cybersecurity, and blockchain.

## Project Goals

- Build a searchable corpus from Wikipedia articles
- Investigate how retrieval models rank results for different queries
- Compare lexical and statistical ranking methods
- Demonstrate document processing and relevance scoring in Python
- Make the dataset and notebook easy to explore and extend

## Dataset

The project uses a curated collection of Wikipedia pages stored in the repository as Excel files:

- `Information Retrieval Dataset.xlsx` — the main article corpus with title, content, and link columns
- `Dataset Summary.xlsx` — summary statistics per topic
- `Dataset Summary.pdf` — a PDF version of the summary

The corpus includes multiple topic clusters, each containing several relevant article pages. The project aggregates around 120 article records across 12 technology-focused themes.

## Repository Structure

```text
Wikipedia-Search-Engineen-/
├── Phase_1.ipynb              # Main notebook for data collection and IR experiments
├── Information Retrieval Dataset.xlsx
├── Dataset Summary.xlsx
├── Dataset Summary.pdf
├── requirements.txt           # Python dependencies
├── information_retrieval.py   # Placeholder / support file for retrieval logic
├── README.md                  # Project documentation
└── .gitignore                 # (if present in the repo)
```

## Key Concepts Covered

### 1. Data Collection

The notebook queries Wikipedia for topic-based searches and extracts article metadata, including:

- article title
- article text
- canonical Wikipedia URL

### 2. Text Preprocessing

The workflow includes:

- lowercasing
- tokenization
- stopword filtering
- alpha-token extraction
- term normalization for retrieval experiments

### 3. Ranking Models

The project demonstrates several ranking paradigms, including:

- Vector Space Model with TF-IDF
- BM25 ranking
- Language modeling with Dirichlet smoothing
- Exploration of graph-aware ranking ideas such as PageRank-inspired traversal

### 4. Evaluation Perspective

The notebook inspects:

- total words per topic
- unique word counts
- percentage of unique words
- stopword statistics
- ranked document output for sample queries

## Technology Stack

- Python
- pandas
- NumPy
- scikit-learn
- rank_bm25
- spaCy
- NLTK
- Wikipedia API
- openpyxl

## Installation

1. Clone the repository:

```bash
git clone https://github.com/mohammad-shahwan/Wikipedia-Search-Engineen-.git
cd Wikipedia-Search-Engineen-
```

2. Create and activate a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. If you are using spaCy language models, install the English model as needed:

```bash
python -m spacy download en_core_web_sm
```

## Usage

Open the notebook:

```bash
jupyter notebook Phase_1.ipynb
```

From there, you can:

- review the corpus construction steps
- rerun the preprocessing pipeline
- test custom queries
- inspect ranking results across different models
- extend the project with new topics or search features

## Example Query

The notebook includes examples such as:

```python
machine learning algorithms in artificial intelligence
```

and compares retrieval results across models, showing how different ranking strategies surface relevant documents.

## Why This Project Matters

This project demonstrates how to turn a general-purpose information source like Wikipedia into a lightweight, teachable search engine pipeline. It is a strong example of:

- web data collection
- text mining
- information retrieval
- query processing
- ranking evaluation
- practical NLP in Python

It is especially useful for students or developers learning how large-scale search systems work at a conceptual and implementation level.

## Future Improvements

Potential next steps for this project include:

- implementing a real web UI or command-line search interface
- adding PageRank or graph-based link analysis more explicitly
- expanding the dataset with more topics and deeper article collections
- integrating query expansion and spell correction
- comparing retrieval quality with benchmark queries
- exporting the ranked results to a dashboard or API

## License

This project does not currently include a license file. If you plan to share or extend it publicly, consider adding an open-source license such as MIT or Apache 2.0.

## Acknowledgements

- Wikipedia for providing the article corpus used in this project
- The Python ecosystem for NLP and information retrieval libraries
- The open-source research community for ranking and search methodologies

## Author

Built and maintained by Mohammad Shahwan.

## Contact

For questions, suggestions, or collaboration opportunities, feel free to reach out through the GitHub repository.
