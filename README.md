# ChatWithSQL

ChatWithSQL is an interactive Streamlit application that allows users to query a MySQL database using natural language. The application leverages language models to translate user queries into SQL and provide natural language responses.

## Features

- Connect to a MySQL database
- Ask questions about your data in natural language
- Get SQL queries and natural language responses
- Interactive chat interface

## Prerequisites

- Python 3.7+
- MySQL database

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/Rakif215/chatwithsql.git
   cd chatwithsql
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up your environment variables:
   Create a `.env` file in the root directory and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

## Usage

1. Start the Streamlit application:
   ```
   streamlit run src/app.py
   ```

2. Open your web browser and navigate to the URL provided by Streamlit (usually `http://localhost:8501`).

3. In the sidebar, enter your MySQL database connection details:
   - Host
   - Port
   - User
   - Password
   - Database name

4. Click the "Connect" button to establish a connection to your database.

5. Once connected, you can start chatting with the AI about your database. Ask questions in natural language, and the AI will provide responses based on your data.

## How it Works

1. The user inputs a question about the database.
2. The application uses a language model to convert the question into a SQL query.
3. The SQL query is executed against the connected MySQL database.
4. Another language model processes the SQL results and generates a natural language response.
5. The response is displayed to the user in the chat interface.

## Customization

- To use a different language model, modify the `llm` variable in the `get_sql_chain` and `get_response` functions.
- You can adjust the prompt templates in the `template` variables to change how the AI interprets questions and formulates responses.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
