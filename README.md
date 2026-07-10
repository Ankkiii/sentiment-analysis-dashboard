# Sentiment Analysis Dashboard

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-blueviolet?style=for-the-badge)

## Overview

This project presents a lightweight Streamlit dashboard engineered for real-time sentiment analysis of review data. It leverages a lexicon-based model to efficiently classify text sentiments (positive, neutral, negative) and visualizes their distribution. The solution is designed to be simple and efficient, consciously avoiding heavyweight dependencies to ensure quick setup and execution for immediate data insights.

## Features

*   **Interactive Streamlit Dashboard:** Provides an intuitive web interface for users to upload review data and visualize sentiment.
*   **Lexicon-Based Sentiment Classification:** Implements a performant, rule-based approach to categorize review sentiment without the need for extensive model training.
*   **Sentiment Distribution Visualization:** Generates clear, interactive charts showing the proportions of positive, neutral, and negative sentiments within the analyzed dataset.
*   **Lightweight Architecture:** Built with minimal external dependencies, ensuring a fast and easily deployable application.
*   **Data Analysis Capabilities:** Utilizes `pandas` for efficient data handling, cleaning, and preparation before sentiment scoring.

## Tech Stack

| Technology      | Description                                                    |
| :-------------- | :------------------------------------------------------------- |
| Python          | Core programming language for application logic and data processing. |
| NLP             | Natural Language Processing techniques for text analysis.      |
| Streamlit       | Framework for creating interactive web applications and dashboards with ease. |
| pandas          | Data manipulation and analysis library for structured datasets. |
| Data Analysis   | General approach for extracting meaningful insights from data. |

## Installation

To get this project up and running locally, follow these steps:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/sentiment-analysis-dashboard.git
    cd sentiment-analysis-dashboard
    ```

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

## Usage

After installation, you can launch the Streamlit dashboard using the following command:

```bash
streamlit run app.py

This command will open the Sentiment Analysis Dashboard in your default web browser, typically at `http://localhost:8501`. You can then upload a CSV file containing reviews (e.g., `sample_reviews.csv`) to analyze its sentiment.

![Dashboard Screenshot](path/to/your/screenshot.png)
_A screenshot of the Sentiment Analysis Dashboard in action, displaying sentiment distribution._

## Project Structure

```
.
├── app.py                 # Main Streamlit application file, handles UI and data loading.
├── sentiment.py           # Contains the core logic for lexicon-based sentiment analysis.
├── sample_reviews.csv     # An example dataset of reviews for testing and demonstration.
├── test_sentiment.py      # Unit tests for the sentiment analysis functions in sentiment.py.
└── requirements.txt       # Lists all Python dependencies required for the project.

## Interview Q&A

### Q1: You chose a lexicon-based model over a machine learning model for sentiment analysis. What were the key reasons behind this decision, and what are its main advantages and limitations in this context?

**A1:** The primary reasons for selecting a lexicon-based model were simplicity, computational efficiency, and minimizing heavyweight dependencies, which aligns with the project's goal of a lightweight dashboard. Lexicon models are quick to implement, require no training data, and are very performant for basic positive/negative/neutral sentiment classification, making them ideal for immediate results and ease of deployment. The main advantage is speed and resource efficiency. However, a key limitation is precision; these models often struggle with nuances like sarcasm, double negatives, idiomatic expressions, and context-specific sentiment that a sophisticated, trained ML model could capture. For this project, the aim was to demonstrate the core concept of sentiment analysis effectively without the overhead of complex model training and management.

### Q2: How does this dashboard handle new or different datasets of reviews? Are there any data formatting requirements users should be aware of when uploading their own CSV files?

**A2:** The dashboard is designed to be flexible for various review datasets. It expects a CSV file where one of the columns contains the review text. By default, it will attempt to identify a column named `review` or `text`, but the `app.py` logic can be easily extended or modified to allow users to select the correct text column from a dropdown after upload. Users should ensure their CSV is well-formed and that the column containing the review text is clearly identifiable. While the current implementation includes basic error handling for file uploads, more robust validation could be added to guide users on expected formats or missing columns, thereby improving user experience.

### Q3: Given that this project avoids "heavyweight deps," how would you approach scaling this sentiment analysis solution for a much larger volume of data (e.g., millions of reviews per day) or for more nuanced sentiment detection in a production environment?

**A3:** For significantly larger data volumes or a production setting requiring more nuanced sentiment detection, the "no heavyweight deps" constraint would need to be relaxed. First, I would separate the data processing and sentiment analysis logic into a robust backend service. For large volumes, I'd integrate distributed processing frameworks like Apache Spark or Dask to handle data ingestion, parallel processing, and sentiment scoring efficiently. For enhanced accuracy and nuance, I would replace the lexicon model with a pre-trained transformer-based model (e.g., BERT, RoBERTa) from libraries like Hugging Face Transformers, potentially fine-tuning it on domain-specific data if available. The Streamlit dashboard would then serve as a responsive front-end, interacting with this powerful, scalable backend via an API, ensuring that the user interface remains fast and interactive while the heavy computational lifting occurs elsewhere.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
