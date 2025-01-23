# Customer Support Chatbot

This project implements a customer support chatbot for Swiss Airlines using LangChain, LangGraph, and Google Gemini.

## Features

* **Flight Information Retrieval:** The chatbot can retrieve flight information for users based on their passenger ID.
* **Company Policy Lookup:** The chatbot can consult company policies to check whether certain options are permitted.
* **Flight Updates and Cancellations:** The chatbot can update or cancel flights for users based on their requests.
* **Car Rental Bookings:** The chatbot can book car rentals for users based on their preferences.
* **Hotel Bookings:** The chatbot can book hotels for users based on their preferences.
* **Trip Recommendations:** The chatbot can recommend trips to users based on their interests.
* **Excursion Bookings:** The chatbot can book excursions for users based on their preferences.

## Architecture

The chatbot is implemented using a state graph and several specialized assistants. The primary assistant handles general Q&A and delegates specialized tasks to other assistants.

## Usage

To use the chatbot, you will need to install the required packages:
Use code with caution
bash !pip install --quiet --upgrade langchain langgraph langchain_community langchain-google-genai tavily-python langchain_huggingface sentence_transformers

 
You will also need to set the following environment variables:
Use code with caution
bash os.environ["LANGCHAIN_PROJECT"] = "Customer-Support-Chatbot" os.environ["LANGCHAIN_TRACING_V2"] = "true" os.environ["LANGCHAIN_API_KEY"] = userdata.get("langchai_api_key") os.environ["GOOGLE_API_KEY"] = userdata.get("Gemini_Api_Key") os.environ["TAVILY_API_KEY"]=userdata.get("tavily_api_key")

 
Once the environment is set up, you can start the chatbot by running the following command:
Use code with caution
python from langgraph.runner import ChatSession

session = ChatSession(builder, print_event=_print_event) session.run({"messages": [("user", "hello!")]})

 
## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any suggestions or improvements.

## License

This project is licensed under the MIT License.
Use code with caution
