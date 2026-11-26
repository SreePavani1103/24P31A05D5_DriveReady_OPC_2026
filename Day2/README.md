Sweet Crumbs Home Bakery Chatbot
About the Project
In this task, I improved the bakery chatbot by adding more features. The chatbot can answer customer questions about the menu, prices, cake orders and eggless options. It can also remember the customer's name and order during the conversation. I added a price calculation function and made the chatbot interactive so customers can continue chatting with it.
Objective
The objective of this task is to build a chatbot that can handle basic bakery enquiries, calculate order prices, remember conversation details and provide helpful responses to customers.
Technologies Used
- Python
- Groq API
- OpenAI Python Library
- Google Colab
- GPT-OSS 20B
Implementation
 1. Setting Up the API
I installed the required OpenAI library and used the Groq API to connect with the language model. The API key is accessed through Google Colab Secrets.
2. Creating the Menu
I created a dictionary containing the bakery items and their prices.

| Item | Price |
|---|---:|
| Plum Cake | ₹500 |
| Chocolate Cake | ₹650 |
| Cupcake | ₹80 |
3. Creating the System Prompt
I provided instructions to the chatbot about its role and behavior. It is instructed to:
- Act as a friendly assistant for Sweet Crumbs Home Bakery.
- Provide menu details and prices.
- Inform customers about the 24-hour advance booking requirement.
- Mention that eggless versions are available.
- Avoid promising delivery times.
- Remember the customer's name and order during the conversation.
- Respond in English or Telugu based on the customer's language.
- Keep responses under 50 words.
4. Creating the Price Calculation Function
I created a function called `get_price()` that calculates the total price based on the item and quantity ordered.
for example, the price of 6 cupcakes is calculated as:
₹80 × 6 = ₹480
I also added a logging decorator that displays the function call and its result.
5. Maintaining Conversation History
I created a `history` list to store the system instructions, customer messages and chatbot responses. This allows the chatbot to refer to previous messages and remember details such as the customer's name and order.
I also used `MAX_TURNS` to limit the number of recent messages sent to the model.
6. Creating the Chat Function
I created a function called `chat()` that accepts the customer's message, adds it to the conversation history and sends the messages to the LLM.
The model generates a response, which is displayed to the customer and stored in the conversation history.
7. Handling Errors
I added error handling for API rate limits and connection problems. If the API is busy or unavailable, the chatbot displays a message asking the customer to try again later.
8. Running the Chatbot
I used a `while` loop to make the chatbot interactive. Customers can continuously enter messages and receive responses. They can type `bye`, `exit` or `quit` to end the conversation.
How to Run
1. Open the notebook in Google Colab.
2. Install the required libraries.
3. Add the Groq API key in Colab Secrets as `GROQ_API_KEY`.
4. Run the notebook cells in order.
5. Start interacting with the chatbot through the input prompt.
6. Type `bye`, `exit` or `quit` to end the chat.
Sample Output
```text
Total for 6 cupcakes: 480

You: Hi my name is Pavani

Bot: Hi Pavani! What would you like to order?

You: I want an eggless chocolate cake

Bot: Got it, Pavani! Eggless chocolate cake, ₹650.
We need 24-hour notice.

You: What is the price for 2?

Bot: Two eggless chocolate cakes will be ₹1,300.

You: What did I order?

Bot: You ordered an eggless chocolate cake.
```
Conclusion
Through this task, I learned how to create an interactive chatbot using an LLM. I implemented menu-based price calculation, conversation history, customer detail remembering, logging and error handling. This helped me understand how a chatbot can maintain a conversation and provide more useful responses based on previous messages.
