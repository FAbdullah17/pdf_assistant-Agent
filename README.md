# PDF Assistant

PDF Assistant is a Python-based application designed to interact with a knowledge base extracted from PDF documents. It provides conversational capabilities using advanced AI tools, a PostgreSQL vector database, and a CLI with Markdown support.

## Features

- **Knowledge Base**: Extract and store data from PDF files for conversational interaction.
- **Semantic Search**: Leverage pgvector for efficient vector-based semantic search.
- **Chat History Management**: Store and retrieve chat sessions using PostgreSQL.
- **Command-Line Interface**: Interact with the assistant directly using a CLI with Markdown formatting.

## Prerequisites

- Python 3.8 or higher
- PostgreSQL database
- A valid Groq API key

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/FAbdullah17/pdf_assistant-Agent.git
   cd pdf_assistant-Agent
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Configure environment variables:
   - Create a `.env` file in the root directory with the following content:
     ```
     GROQ_API_KEY=your-groq-api-key
     ```
   - Replace `your-groq-api-key` with your actual API key.

5. Set up your PostgreSQL database and update the `db_url` in the script to match your database credentials.

## Usage

Run the assistant script with the following commands:

1. **Start the Assistant**:
   ```bash
   python <script_name>.py
   ```

2. **Start a New Conversation**:
   ```bash
   python <script_name>.py --new
   ```

3. **Specify a User**:
   ```bash
   python <script_name>.py --user <username>
   ```

Replace `<script_name>` with the name of the Python script.

## How It Works

1. **Knowledge Base Setup**:
   - The `PDFUrlKnowledgeBase` loads content from the specified PDF URLs and stores it in a vector database using `pgvector`.

2. **Storage**:
   - The PostgreSQL database is used to store chat sessions and retrieve run history with `PgAssistantStorage`.

3. **Assistant Initialization**:
   - The assistant can search the knowledge base, read previous chat history, and provide responses based on the PDF content.

4. **Command-Line Interaction**:
   - Users can interact with the assistant via a CLI that supports Markdown formatting.

## Dependencies

The project requires the following Python libraries:
- `phidata`
- `python-dotenv`
- `yfinance`
- `packaging`
- `duckduckgo-search`
- `fastapi`
- `uvicorn`
- `groq`
- `openai`
- `sqlalchemy`
- `pgvector`
- `psycopg[binary]`
- `pypdf`

Install them using:
```bash
pip install -r requirements.txt
```

## Customization

- **Add New PDFs**: Update the `urls` parameter in the `PDFUrlKnowledgeBase` initialization to include additional PDFs.
- **Database Configuration**: Modify the `db_url` variable to connect to your PostgreSQL instance.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Fork the repository, create a feature branch, and submit a pull request.

## Contact

For questions or support, please create an issue on the GitHub repository.
