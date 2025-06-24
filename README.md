# AWS Bedrock LangChain Chatbot 📚🤖

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![AWS](https://img.shields.io/badge/AWS-Bedrock-orange.svg)
![LangChain](https://img.shields.io/badge/LangChain-0.1.0-blue.svg)

A powerful PDF chatbot powered by AWS Bedrock and LangChain, supporting multiple LLM models including Claude and Llama2.

## Features ✨

- 📄 Chat with PDF documents using natural language
- ⚡ Powered by AWS Bedrock's Titan embeddings
- 🤖 Multiple LLM backends (Claude via AI21 and Llama2)
- 🔍 Semantic search with FAISS vector store
- 🎨 Streamlit-based user interface
- 🔄 Automatic text chunking and vector store updating

## Technologies Used 🛠️

- <img src="https://aws.amazon.com/favicon.ico" width="16"> **AWS Bedrock** (Titan embeddings, Claude, Llama2)
- <img src="https://python.langchain.com/img/favicon.ico" width="16"> **LangChain** (RAG pipeline, text splitting)
- <img src="https://streamlit.io/favicon.ico" width="16"> **Streamlit** (Web UI)
- <img src="https://faiss.ai/favicon.ico" width="16"> **FAISS** (Vector similarity search)
- <img src="https://boto3.amazonaws.com/v1/documentation/api/latest/_static/favicon.ico" width="16"> **Boto3** (AWS SDK for Python)

## Installation ⚙️

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Hari-Kec/AWS-Bedrock--Langchain-Chatbot.git
   cd AWS-Bedrock--Langchain-Chatbot
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure AWS credentials**:
   ```bash
   aws configure
   ```
   Or set environment variables:
   ```bash
   export AWS_ACCESS_KEY_ID=your_access_key
   export AWS_SECRET_ACCESS_KEY=your_secret_key
   export AWS_DEFAULT_REGION=your_region
   ```

4. **Add PDF files**:
   Place your PDF documents in the `data/` directory

## Usage 🚀

1. **Run the application**:
   ```bash
   streamlit run main.py
   ```

2. **Update vector store** (first time or when adding new documents):
   - Click "Vectors Update" in the sidebar

3. **Ask questions**:
   - Enter your question in the text input
   - Choose either "Claude Output" or "Llama2 Output" button

## Project Structure 📂

```
AWS-Bedrock--Langchain-Chatbot/
├── data/                   # Directory for PDF documents
├── faiss_index/            # Generated vector store
├── main.py                 # Main application script
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

## Configuration ⚙️

### Environment Variables
Set these in your environment or `.env` file:
```
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_DEFAULT_REGION=your_region (e.g., us-east-1)
```

### Customizing the Prompt
Edit the `prompt_template` in `main.py` to change the chatbot's response behavior:
```python
prompt_template = """
Human: Use the following pieces of context to provide a 
concise answer to the question at the end...
"""
```

## Supported Models 🧠

- **Embeddings**: Amazon Titan Embed Text v1
- **LLMs**:
  - Claude (via AI21 J2 Mid)
  - Llama2 70B Chat

## License 📜

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing 🤝

Contributions are welcome! Please open an issue or submit a pull request.

## Acknowledgments 🙏

- AWS for the Bedrock service
- LangChain team for the amazing framework
- Meta for Llama2 model
- Anthropic for Claude model
