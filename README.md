# ArticleInsight

ArticleInsight is a web-based tool designed for extracting relevant information from news articles. It allows users to input URLs of news articles, processes them to extract content, and enables querying of the content to get precise answers.

## Features

- **URL Input**: Users can input up to three URLs of news articles to extract information.
- **Text Extraction**: The tool processes the content from the URLs, extracts the text, and splits it into manageable chunks for further processing.
- **Embedding & Search**: Articles are embedded using a state-of-the-art model to facilitate efficient search and retrieval of relevant information.
- **Question Answering**: Users can ask questions related to the articles, and the tool provides answers by searching through the article content.
- **Source Tracking**: After answering a query, the tool lists the top sources used to find the answer.

## Requirements

- Python 3.7+
- Streamlit
- LangChain
- Sentence Transformers
- HuggingFace Transformers
- Numpy

## Installation

To run ArticleInsight locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/ArticleInsight.git
    ```

2. Navigate to the project directory:
    ```bash
    cd ArticleInsight
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the application:
    ```bash
    streamlit run app.py
    ```

The web interface will open in your default browser, allowing you to input URLs and query the articles for answers.

## How It Works

1. **URL Input**: The sidebar allows the user to input up to three URLs of news articles.
2. **Data Extraction**: Upon clicking the "Process URLs" button, the content from these URLs is extracted and split into chunks for further analysis.
3. **Embedding & Search**: The content is embedded using a pre-trained SentenceTransformer model, which converts the text into numerical vectors for efficient similarity matching.
4. **Querying**: Once the embedding is completed, users can input questions related to the content, and the tool retrieves the top relevant answers using a HuggingFace question-answering pipeline.
5. **Results**: The best answer and its sources are displayed in the main window.

### Example Workflow

1. Input three URLs in the sidebar (news article URLs).
2. Click the "Process URLs" button.
3. Once the URLs are processed, type a question in the query field (e.g., "What is the main topic of the article?").
4. The tool will display the best answer from the relevant article(s) along with the sources.
