GreenNest AI Plant Assistant
About the Project
In this task, I developed an AI assistant for GreenNest, an indoor plant business. It helps customers with plant prices, availability, plant-care suggestions and order enquiries using an LLM.
Technologies Used
- Python
- LangChain
- Groq API
- Google Colab
- GPT-OSS 20B
Implementation
- Connected the LLM using Groq API and LangChain.
- Created a system prompt with plant details, prices and business rules.
- Added a test function to check chatbot responses using a CSV file.
- Improved the system prompt to ensure product prices are mentioned correctly.
- Created a function to calculate the total price of plants and decorative pots.
- Added tools to check plant stock and calculate order prices.
- Created a LangChain AI agent that uses these tools to answer customer order queries.
How to Run
1. Open the notebook in Google Colab.
2. Install the required libraries.
3. Add the Groq API key in Colab Secrets.
4. Run the cells in order.
5. Test the chatbot using the provided questions or agent queries.
Conclusion
Through this task, I learned how to create an AI agent using LangChain, connect tools to an LLM, check product availability, calculate prices and test chatbot responses.
