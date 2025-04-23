# Project Flow: Build Your Own Custom Chatbot

## 1. Project Overview
- Objective: Build a custom OpenAI chatbot using a scenario and dataset of your choice.
- Approach: Use basic packages (openai, pandas) to manually construct the chatbot, avoiding frameworks like LangChain.
- Goal: Gain a deeper understanding of chatbot construction and prompt engineering.

## 2. Data Source
- File: `character_descriptions.csv`
- Content: Character descriptions from theater, television, and film (name, description, medium, setting).
- Note: All characters are AI-generated.

## 3. Custom Scenario & Dataset Justification
- At the start of the notebook, write a paragraph explaining why this dataset is appropriate for your chatbot scenario.
- Describe a use case where customizing the chatbot with this data is beneficial.

## 4. Implementation Steps
1. **Import Required Libraries**: pandas, openai, numpy, tiktoken, etc.
2. **Load and Explore Dataset**: Read `character_descriptions.csv` and understand its structure.
3. **Data Wrangling**: Combine relevant columns into a single `text` column for each character.
4. **Embedding Generation**: Use OpenAI's Embedding API to generate vector representations for each character description. Save embeddings to avoid repeated API calls.
5. **Relevance Ranking**: For each user question, compute its embedding and rank all character descriptions by cosine similarity.
6. **Prompt Construction**: Use tiktoken to count tokens and construct a prompt that includes the most relevant context within the model's token limit.
7. **Build Chatbot Logic**: Use OpenAI API to generate responses based on user input and the selected context.
8. **Demonstrate Q&A**: Show chatbot responses before and after customization.
9. **Interactive Chatbot Loop**: Allow users to interact with the chatbot in real time, with dynamic context selection for each question.

## 5. Evaluation
- At the end of the notebook, compare model answers before and after using the custom dataset and embedding-based context selection.
- Highlight improvements or changes in chatbot behavior, such as increased relevance and specificity.

## 6. API Key
- The OpenAI API key is provided in project resources (ensure it is loaded securely and not shared publicly).

## 7. Deliverables
- A notebook with:
  - Dataset justification and scenario description
  - Code for loading data, generating embeddings, and building the chatbot
  - Demonstrations of chatbot performance
  - Interactive chatbot loop
  - Analysis of results

---

**Tip:** Think step by step, from data loading to embedding generation, prompt design, chatbot construction, and evaluation. Document your reasoning and results clearly.
