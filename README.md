# Custom Chatbot Project

This project is a part of my **BERTELSMANN next Gen Tech Booster Generative AI Nanodegree Program by Udacity**

This project demonstrates how to build a custom chatbot using a dataset of fictional character descriptions. The chatbot leverages OpenAI's language models to answer questions about characters, simulate their personalities, and provide interactive storytelling experiences. The project is implemented in a Jupyter Notebook using Python, pandas, and the OpenAI API.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Setup Instructions](#setup-instructions)
- [Notebook Structure](#notebook-structure)
- [Project Flow & Evaluation](#project-flow--evaluation)
- [How It Works](#how-it-works)
- [Example Usage](#example-usage)
- [Customization](#customization)
- [License](#license)

## Project Overview
This project uses a dataset (`character_descriptions.csv`) containing detailed descriptions of fictional characters from various media (theater, television, film, etc.). The chatbot is designed to:
- Answer user questions about these characters.
- Reference specific character details in its responses.
- Simulate character personalities and backgrounds.
- Compare chatbot performance with and without custom context.
- Use embedding-based relevance to select the most appropriate context for each user question.

## Dataset
- **File:** `character_descriptions.csv`
- **Contents:** Each row describes a fictional character, including their name, description, medium, and setting.
- **Purpose:** Provides rich, structured information for the chatbot to use as context when answering questions.

## Setup Instructions
1. **Clone the repository or download the project files.**
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Obtain an OpenAI API key** and set it in the notebook where indicated (`YOUR_API_KEY`).
   - **Security Note:** Never share your API key publicly. Store it securely and consider using environment variables or secrets management for production use.
4. **Open `project.ipynb` in VS Code or Jupyter Notebook.**

## Notebook Structure
The notebook is organized as follows:
- **Project Introduction & Dataset Justification:** Overview, scenario, and why the dataset is appropriate.
- **Data Wrangling:** Loads the dataset and prepares a combined `text` column for each character.
- **Embedding Generation:** Uses OpenAI's Embedding API to generate vector representations for each character description, enabling relevance-based context selection.
- **Custom Query Completion:** Defines helper functions to query the OpenAI API with and without custom context.
- **Performance Demonstration:** Shows example questions and compares basic vs. custom completions.
- **Interactive Chatbot Loop:** Allows users to interact with the chatbot in real time by typing questions. The chatbot dynamically selects the most relevant context for each question using cosine similarity between embeddings.
- **Evaluation:** Compares model answers before and after using the custom dataset, highlighting improvements.

## Project Flow & Evaluation
- The project follows a step-by-step approach:
  1. Data loading and wrangling
  2. Embedding generation and storage
  3. Relevance ranking using cosine similarity
  4. Prompt construction with token counting
  5. Custom and basic completions
  6. Interactive chatbot loop
  7. Evaluation and analysis

## How It Works
- The chatbot uses OpenAI's Completion API.
- For each user question, the system computes an embedding and ranks all character descriptions by cosine similarity.
- The most relevant descriptions are included in the prompt, ensuring answers are grounded in the dataset.
- The chatbot is interactive and can be used directly in the notebook.

## Example Usage
- Ask questions like:
  - "Who is Emily and what is her personality like?"
  - "Which character is a retired soldier and what challenges does he face?"
- The chatbot will reference specific details from the dataset in its answers.

## Customization
- You can adapt the dataset or prompt construction logic for other domains or data sources.
- The embedding-based context selection can be reused for other retrieval-augmented generation tasks.

## License
See [LICENSE](LICENSE) for details.
