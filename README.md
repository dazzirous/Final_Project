# **American History Q&A Project**

## **Team Members**
- **[Brian]**
- **[Jaime]**
- **[Eric]**

## **Project Name**
**American History Q&A with Wikipedia**

## **High-Level Goal**
The goal of this project is to create an AI-powered Q&A system that answers questions about American History using Wikipedia as a knowledge base. The system will retrieve relevant content from Wikipedia and use a pre-trained transformer model to generate accurate answers to user queries.

## **Proposed Dataset**
- **Source:** Wikipedia API  
- **Focus:** Articles related to key events, figures, and themes in American History (e.g., American Revolution, Civil War, Declaration of Independence).

## **Summary Plan**

### **Algorithm/Library:**
- **Wikipedia API:** To retrieve relevant American History content based on user queries.
- **Hugging Face Transformers:** Specifically, the `distilbert-base-cased-distilled-squad` model, to perform question answering on the retrieved content.
  
### **Front End and Tools:**
- **Gradio:** A simple interface for users to input questions and view answers.
- **Python Libraries:** 
  - `wikipediaapi` for Wikipedia content retrieval.
  - `transformers` for implementing the Q&A model.
  
### **Approach:**
1. **Wikipedia Content Retrieval:** Use the Wikipedia API to fetch summaries of relevant American History topics.
2. **Q&A Model:** Utilize the pre-trained DistilBERT model fine-tuned on SQuAD to answer questions based on the retrieved content.
3. **User Interface:** Develop a simple user interface using Gradio to allow users to interact with the model.
4. **Integration:** Integrate all components and perform testing to ensure accuracy and usability.

### **Challenges** 
One of the key challenges we faced was that the model sometimes struggled with answering straightforward questions, often requiring additional guidance to reframe its responses effectively. This highlighted the model's limitations in handling simple queries without explicit direction.

Another significant issue occurred when we accepted a pull request that inadvertently broke the model. Following this, we could no longer access the model and encountered errors whenever we attempted to interact with any requests in Git. As a result, we had to scrap the existing code and replace it with new code that not only improved functionality but also focused on more specific tasks. However, this change had unintended consequences: it disrupted Brian's code, which had been working fine prior to the update. This setback requires us to revisit and debug the affected parts to restore their functionality.

Despite these challenges, we did observe that the chatbot performed well when asked consecutive questions, demonstrating its ability to handle sequential interactions effectively.

# Wikipedia Article QA and Sentiment Analysis

This project retrieves Wikipedia articles from a specified category, applies question-answering using a BERT model, and performs sentiment analysis on the answers. The project is designed to showcase basic NLP techniques using Python, Hugging Face Transformers, and Gradio for building a simple user interface.

## Table of Contents

- [Dependencies](#dependencies)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Features](#features)
- [Future Improvements](#future-improvements)
- [License](#license)

## Dependencies

To run this project, you will need the following Python libraries:

- `requests`: For making HTTP requests to the Wikipedia API.
- `pandas`: For handling and manipulating tabular data.
- `nltk`: For natural language processing tasks such as tokenization and stopword removal.
- `transformers`: For using pre-trained models like BERT for question-answering.
- `gradio`: For creating a user-friendly web interface.

Ensure that you have Python 3.7 or later installed. You can install the required dependencies using pip:

```bash
pip install requests pandas nltk transformers gradio
```

Additionally, you need to download some NLTK resources:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

## Usage

To use the application:

1. **Retrieve Wikipedia Articles:**
   The script retrieves articles from a specified Wikipedia category. You can specify the category by setting the `category_name` variable.

   Example:
   ```python
   category_name = "American Revolution"
   df_articles = get_articles_from_category(category_name)
   ```

   This will return a pandas DataFrame containing the titles, descriptions, and content of articles in the specified category.

2. **Question-Answering and Sentiment Analysis:**
   The application uses a pre-trained BERT model to answer questions based on the summaries of the articles. It also analyzes the sentiment of the answers using the VADER sentiment analyzer.

   Example:
   ```python
   question = "What was the main cause of the American Revolution?"
   answer, analysis = get_answer_and_sentiment(question)
   print("Answer:", answer)
   print("Sentiment Analysis:", analysis)
   ```

3. **Run the Gradio Interface:**
   You can interact with the model through a web interface powered by Gradio.
   ```python
   interface.launch()
   ```

## Project Structure

- `get_articles_from_category()`: A function that retrieves articles from a specified Wikipedia category and returns them in a pandas DataFrame.
- `get_answer_and_sentiment()`: A function that answers a question based on article summaries and analyzes the sentiment of the answer.
- Gradio Interface: A simple user interface for interacting with the model.

## Features

- **Article Retrieval:** Fetches articles from a specified Wikipedia category.
- **Question-Answering:** Uses BERT to answer questions based on article content.
- **Sentiment Analysis:** Analyzes the sentiment of the answers using VADER.
- **Web Interface:** A Gradio-powered interface for easy interaction.

## Future Improvements

- Improve the accuracy and speed of the question-answering model.
- Enhance the user interface with more options and better styling.
- Add support for more languages and Wikipedia categories.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

This version replaces the "Installation" section with the "Dependencies" section, making it more aligned with the dependencies required for your project.
