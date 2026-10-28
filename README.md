# my-poc

# Project 1: Portfolio Manager Research Assistant using RAG

## POC (Proof of Concept)

### Objective

The objective of this POC is to optimise the time portfolio managers spend researching investment-related documents, financial reports, investment policies, and market research materials. The solution enables users to ask natural-language questions and receive context-aware answers with supporting document references, reducing manual document searching and information retrieval effort.

### Approach

1. Collect sample investment research reports, fund documents, and financial publications in PDF or text format.
2. Extract document content and split it into manageable, overlapping chunks while retaining metadata such as document name and page number.
3. Generate embeddings for the chunks and store them in a persistent ChromaDB vector database.
4. Accept natural-language research queries from the portfolio manager and retrieve the most relevant document passages using semantic similarity search.
5. Pass the retrieved context and user query to a locally running Llama model through Ollama.
6. Generate concise, context-grounded answers with source references and allow the assistant to indicate when the available documents do not contain sufficient information.
7. Evaluate retrieval relevance, answer quality, and research task completion time against a manual-search baseline.

### Tech Stack

- **Language/Framework:** Python, optional Streamlit for the user interface
- **LLM:** Llama 3.x via Ollama
- **Vector Database:** ChromaDB
- **Embeddings:** Local embedding model such as `nomic-embed-text` through Ollama
- **Document Processing:** PyMuPDF or a suitable PDF loader
- **Supporting Libraries:** ChromaDB client, Ollama integration, and optionally LlamaIndex

### Steps to Run

1. Clone the project repository.
2. Create and activate a Python virtual environment.
3. Install the dependencies listed in `requirements.txt`.
4. Install Ollama and download the required Llama and embedding models.
5. Place permitted sample research documents in the designated data folder.
6. Configure the model names and ChromaDB persistence directory.
7. Run the document ingestion/indexing script to create the vector index.
8. Start the query interface or application and ask research questions.

### Results / Screenshots

- **Expected output:** Concise answers to investment research questions, supported by relevant passages and document references.
- **Evaluation:** Compare average research-task completion time, retrieval relevance, and answer correctness before and after using the assistant. Report measured results only after testing.


# Project 2: Crypto Trading POC

## POC (Proof of Concept)

### Objective

The objective of this POC is to demonstrate the core workflow of a cryptocurrency trading application, including market information access, trade-related operations, transaction tracking, and user interaction with a crypto-focused application. The implementation scope follows the original Crypto Trading POC discussion.

### Approach

1. Define the core crypto trading use case and user journey.
2. Design a simple interface for interacting with the selected cryptocurrency functionality.
3. Integrate the relevant market-data source or blockchain interface, depending on the original implementation.
4. Implement the trade or transaction workflow using test data or a test network where applicable.
5. Validate inputs, handle failed requests or transactions, and display transaction status.
6. Test the main user journey and document the application flow, technical design, and limitations.

### Tech Stack

- **Language/Framework:** Python or JavaScript, depending on the original implementation
- **Application Interface:** Web interface or command-line interface
- **Integration:** Relevant crypto market-data API or blockchain/Web3 libraries, depending on the implemented scope
- **Testing:** Sample data and test-network transactions, if applicable

### Steps to Run

1. Open or clone the original project repository.
2. Create and activate the required development environment.
3. Install the dependencies specified by the project.
4. Configure the required API credentials or blockchain test-network settings, if applicable.
5. Run the application using the original project instructions.
6. Execute the supported crypto workflow and inspect the output or transaction status.

### Results / Screenshots

- **Validation:** Document the actual features tested, successful test cases, and known limitations.

**Implementation note:** This is a structured draft based on the shared Crypto Trading POC reference. Update the technical stack, workflow, and run commands to match the actual implementation before publishing.

# Project 3: Llama-Powered AI Email Agent

## POC (Proof of Concept)

### Objective

The objective of this POC is to reduce the time spent manually managing emails by using a locally running Llama model to understand email content, summarise conversations, prioritise messages, and generate context-aware reply drafts. The agent assists with repetitive email tasks while retaining human oversight for outgoing communications.

### Approach

1. Connect the application to an email source through an authorised email API or IMAP integration.
2. Retrieve selected emails and extract the sender, subject, message body, timestamp, and relevant thread context.
3. Use the Llama model running through Ollama to classify email intent, identify priority, and summarise lengthy conversations.
4. Generate suggested replies based on the email content, requested tone, and available context.
5. Provide a simple interface to review email summaries, priority labels, and suggested replies.
6. Add controlled tool execution for supported actions such as searching emails, retrieving thread details, and creating reply drafts.
7. Require explicit user approval before sending emails or performing other consequential actions.
8. Evaluate classification accuracy, reply-draft usefulness, and time saved on representative email tasks.

### Tech Stack

- **Language/Framework:** Python, Streamlit for the user interface
- **LLM:** Llama 3.x via Ollama
- **Email Integration:** Gmail API with OAuth 2.0, or IMAP/SMTP where appropriate
- **Processing:** Python email and text-processing libraries
- **Agent Logic:** Python functions for email search, summarisation, classification, and reply drafting
- **Configuration:** Environment variables for settings; credentials stored securely

### Steps to Run

1. Clone the project repository.
2. Create and activate a Python virtual environment.
3. Install dependencies from `requirements.txt`.
4. Install Ollama and download the selected Llama model.
5. Configure the email integration and required authorisation.
6. Set the model and application settings in the environment configuration.
7. Start the application using the repository's run instructions.
8. Test email summarisation, classification, reply drafting, and approval-controlled actions using sample or authorised emails.

### Results / Screenshots

- **Evaluation:** Measure email handling time, classification accuracy, draft acceptance rate, and the number of manual steps reduced.
