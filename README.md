
```markdown
# MAZO_RAG: 
Our POC is a Streamlit application designed to extract and analyze text from PDF documents, leveraging the advanced capabilities of Google's Generative AI, specifically the Gemini-PRO model. This uses a Retrieval-Augmented Generation (RAG) framework to offer precise, context-aware answers to user queries based on the content of uploaded documents.

## Features

- **Instant Insights**: Extracts and analyses text from uploaded PDF documents to provide instant insights.
- **Retrieval-Augmented Generation**: Utilizes Google's Generative AI model Gemini-PRO for high-quality, contextually relevant answers.
- **Secure API Key Input**: Ensures secure entry of Google API keys for accessing generative AI models.

## Getting Started

### Prerequisites

- Google API Key: Obtain a Google API key to interact with Google's Generative AI models. Visit [Google API Key Setup](https://makersuite.google.com/app/apikey) to get your key.
- Streamlit: This application is built with Streamlit. Ensure you have Streamlit installed in your environment.

### Installation

```bash
pip install -r requirements.txt
```

### How to Use

1. **Start the Application**: Launch the Streamlit application by running the command:
    ```bash
    streamlit run <script_name.py>

2. **Enter Your Google API Key**: Securely enter your Google API key when prompted. This key enables the application to access Google's Generative AI models.

3. **Upload PDF Documents**: You can upload one or multiple PDF documents. The application will analyze the content of these documents to respond to queries.

4. **Ask Questions**: Once the documents are processed, you can ask any question related to the content of the uploaded documents.

### Technical Overview

- **PDF Processing**: Utilizes `PyPDF2` for extracting text from PDF documents.
- **Text Chunking**: Employs the `RecursiveCharacterTextSplitter` from LangChain for dividing the extracted text into manageable chunks.
- **Vector Store Creation**: Uses `FAISS` for creating a searchable vector store from text chunks.
- **Answer Generation**: Leverages `ChatGoogleGenerativeAI` from LangChain for generating answers to user queries using the context provided by the uploaded documents.

