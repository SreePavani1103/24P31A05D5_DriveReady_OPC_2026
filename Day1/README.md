# Sweet Crumbs Home Bakery AI Assistant

## About the Project
In this project, I created a simple AI chatbot for Sweet Crumbs Home Bakery. The chatbot helps customers by answering basic questions about cake orders, availability, and bakery information. I used LangChain and Groq to connect the chatbot with an LLM and make it respond based on the instructions provided.

## Objective
The main aim of this project is to build a chatbot that can answer customer queries in a helpful and polite manner while following the bakery's rules.

## Technologies Used
- Python
- LangChain
- Groq API
- Google Colab
- GPT-OSS 120B
- Llama Prompt Guard

## Implementation

### 1. Installing the Required Library
I started by installing the `langchain_groq` library and importing `ChatGroq` to connect with the Groq language model.

### 2. Setting Up the API Key
I used Google Colab Secrets to store and access my Groq API key instead of directly adding it to the notebook.

### 3. Initializing the LLM
I initialized the language model using the `openai/gpt-oss-120b` model. I set the temperature to 0 so that the responses are more consistent.

### 4. Defining the Chatbot Instructions
I created a system prompt to tell the chatbot how it should behave. I provided some basic information about the bakery and added instructions such as:

- Cakes are made to order.
- Orders should be placed at least 24 hours in advance.
- Eggless cakes are also available.
- The chatbot should not promise delivery times.
- Responses should be polite and within 60 words.

### 5. Creating the Chatbot Function
I created a function called `ask()` that takes a question from the customer and sends it to the LLM along with the system instructions. The model generates a response, which is then returned to the user.

### 6. Testing the Chatbot
I tested the chatbot by asking whether an order could be received the next day. It generated a response explaining the 24-hour notice requirement without promising a specific delivery time.

### 7. Testing Prompt Guard
I also tested the Llama Prompt Guard model using a sample prompt that tries to ignore the previous instructions. The model returned a safety score for the given prompt.

## How to Run
1. Open the notebook in Google Colab.
2. Install the required library.
3. Add your Groq API key in Colab Secrets using the name `GROQ_API_KEY`.
4. Run the notebook cells one by one.
5. Ask questions using the `ask()` function.

Example:

```python
print(ask("Can I get my order tomorrow?"))
```

## Output
The chatbot responds to customer questions based on the instructions given in the system prompt. It provides information about cake orders, advance booking and eggless options while avoiding false promises about delivery timings.

The Prompt Guard model also returns a safety score when tested with the sample prompt.

## Conclusion
Through this project, I learned how to connect an LLM using Groq, create system prompts and build a simple chatbot using LangChain. I also explored Prompt Guard to understand how prompts can be checked for potential safety issues. This project gave me a basic understanding of building AI-powered applications.

