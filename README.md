# PersonalRAG 🤖

A streamlined RAG (Retrieval-Augmented Generation) system for your personal documents with PDF support. PersonalRAG helps you quickly find and retrieve information from your knowledge base using natural language queries.

## ✨ Features

- **📄 Multi-format Support**: Automatically converts PDFs to markdown for seamless indexing
- **🔍 Smart Retrieval**: Advanced vector search with 35 document context retrieval
- **💬 Conversational Interface**: Modern Gradio-based chat interface
- **📚 Organized Knowledge**: Supports structured document organization by type
- **⚡ Auto-conversion**: Drop PDFs anywhere in your knowledge base - they're automatically converted
- **🎯 Accurate Responses**: Optimized chunking and prompting for precise answers

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Azure OpenAI API access
- Required Python packages (see requirements below)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd personal-knowledge-worker
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   ```bash
   cp env_template.txt .env
   # Edit .env with your Azure OpenAI credentials
   ```

4. **Run the notebook**
   ```bash
   jupyter notebook personal_coder.ipynb
   ```

## 📁 Project Structure

```
personal-knowledge-worker/
├── personal_coder.ipynb          # Main RAG system notebook
├── my-knowledge-worker-data/     # Your knowledge base
│   ├── documents/                # Personal documents
│   │   ├── work/                # Work-related files
│   │   ├── learning/            # Educational content
│   │   ├── personal-notes/      # Personal notes
│   │   └── reference/           # Reference materials
│   ├── projects/                # Project documentation
│   └── emails/                  # Email content
├── vector_db/                   # Vector database storage
├── env_template.txt             # Environment variables template
└── README.md                    # This file
```

## 🔧 Configuration

### Environment Variables

Create a `.env` file with your Azure OpenAI credentials:

```env
# Azure OpenAI Configuration
AZURE_OPENAI_ENDPOINT=your_endpoint_here
AZURE_OPENAI_API_KEY=your_api_key_here
AZURE_OPENAI_API_VERSION=2024-02-15-preview
AZURE_OPENAI_DEPLOYMENT=your_deployment_name
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=your_embedding_deployment

# Azure Chat OpenAI Configuration
AZURE_CHATOPENAI_DEPLOYMENT=your_chat_deployment
AZURE_CHATOPENAI_ENDPOINT=your_chat_endpoint
AZURE_CHATOPENAI_API_KEY=your_chat_api_key
AZURE_CHATOPENAI_API_VERSION=2024-02-15-preview
```

### System Settings

- **Retrieval**: 35 documents per query
- **Chunk Size**: 1000 characters
- **Chunk Overlap**: 300 characters
- **Model**: Azure OpenAI GPT-4
- **Embeddings**: Azure OpenAI text-embedding-ada-002

## 📖 Usage

### Adding Documents

1. **PDFs**: Drop any PDF file into any folder in `my-knowledge-worker-data/`
   - They're automatically converted to markdown
   - Original PDFs are preserved
   - No manual conversion needed

2. **Markdown Files**: Place `.md` files directly in your knowledge base folders
   - Supports any markdown content
   - Automatically indexed on next run

3. **Organize by Type**: Use the folder structure to categorize your content
   - `documents/work/` - Work-related content
   - `documents/learning/` - Educational materials
   - `projects/` - Project documentation

### Querying Your Knowledge Base

Launch the Gradio interface and ask questions like:

- "What is my work experience?"
- "Tell me about my projects"
- "What skills do I have?"
- "Summarize my resume"
- "What are my achievements?"

## 🛠️ Technical Details

### Architecture

- **Vector Database**: ChromaDB for efficient similarity search
- **Embeddings**: Azure OpenAI text-embedding-ada-002 (1536 dimensions)
- **LLM**: Azure OpenAI GPT-4 for response generation
- **Text Processing**: LangChain RecursiveCharacterTextSplitter
- **PDF Processing**: pdfplumber for reliable text extraction

### Performance Optimizations

- **Smart Database Management**: Reuses existing vector database
- **Efficient Chunking**: 300-character overlap for context preservation
- **Batch Processing**: Processes multiple documents efficiently
- **Error Recovery**: Handles corrupted databases gracefully

## 🔄 Workflow

1. **Document Processing**: PDFs are auto-converted to markdown
2. **Text Chunking**: Documents are split into 1000-character chunks
3. **Embedding Generation**: Chunks are converted to vector embeddings
4. **Vector Storage**: Embeddings stored in ChromaDB
5. **Query Processing**: Natural language queries are vectorized
6. **Similarity Search**: Most relevant chunks are retrieved
7. **Response Generation**: LLM generates answers based on context

## 📊 Features in Detail

### Auto PDF Conversion
- Scans all subdirectories for PDF files
- Converts to markdown with proper formatting
- Skips already converted files
- Preserves original PDFs

### Smart Retrieval
- Retrieves 35 most relevant document chunks
- Uses semantic similarity search
- Maintains conversation context
- Handles multiple document types

### Modern Interface
- Clean, professional Gradio interface
- Real-time chat experience
- Example questions for quick start
- Responsive design

## 🚨 Troubleshooting

### Common Issues

1. **Environment Variables Not Loading**
   - Check `.env` file format
   - Ensure no spaces around `=`
   - Verify file is in project root

2. **PDF Conversion Errors**
   - Install pdfplumber: `pip install pdfplumber`
   - Check PDF file integrity
   - Ensure file permissions

3. **Vector Database Issues**
   - Delete `vector_db/` folder to rebuild
   - Check disk space
   - Verify ChromaDB installation

4. **API Errors**
   - Verify Azure OpenAI credentials
   - Check API quotas and limits
   - Ensure correct deployment names

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Hardik**
- Email: hardik216730@gmail.com
- LinkedIn: [Your LinkedIn Profile]
- GitHub: [Your GitHub Profile]

## 🙏 Acknowledgments

- LangChain for the RAG framework
- ChromaDB for vector storage
- Gradio for the user interface
- Azure OpenAI for embeddings and language models

---

**PersonalRAG** - Your intelligent personal knowledge assistant! 🚀
