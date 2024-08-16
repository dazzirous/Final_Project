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
