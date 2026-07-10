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

