Here is a merged version of the two README files:

---

# Maternal Health Care Chatbot 🏥👶

## Project Overview

This Maternal Health Care Chatbot is an innovative AI-powered solution designed to provide accessible, context-aware information about maternal health. Utilizing advanced retrieval-augmented generation (RAG) techniques, the chatbot leverages machine learning to extract and synthesize relevant information from medical documents.

### Key Features
- Context-aware medical information retrieval
- Lightweight, memory-efficient design
- Streamlit-based interactive interface
- Supports PDF document ingestion and querying
- Flexible embedding and language model integration

## Technology Stack

- **Language**: Python
- **Vector Database**: Chroma
- **Embedding Generation**: Custom Claude-based embedding
- **UI Framework**: Streamlit
- **Local Language Model**: Ollama (TinyLlama)
- **Key Libraries**: 
  - LangChain
  - Anthropic
  - NumPy

## Project Architecture

### Components
1. **Document Ingestion** (`populate_database.py`)
   - Converts PDF documents into embeddings
   - Creates a semantic vector database
   - Supports document chunk management

2. **Embedding Generation** (`embedding.py`)
   - Custom embedding generation using Claude
   - Semantic vector representation of medical text
   - Adaptable to different computational environments

3. **Query Processing** (`query_data.py`)
   - Retrieval-Augmented Generation (RAG) implementation
   - Semantic search across medical documents
   - Contextually grounded response generation

---

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/Mvng-ii/Maternal_Health_Care_Chatbot.git
cd maternal-health-chatbot
```

### 2. Python Virtual Environment Setup
```bash
# Create a virtual environment
python -m venv maternal_health_env

# Activate the virtual environment
# On Windows
maternal_health_env\Scripts\activate
# On macOS/Linux
source maternal_health_env/bin/activate
```

### 3. Core Python Package Installations
```bash
# Upgrade pip
pip install --upgrade pip

# Install core requirements
pip install \
    streamlit \
    langchain \
    langchain-community \
    chromadb \
    anthropic \
    python-dotenv \
    numpy
```

### 4. Ollama Installation

#### Windows
1. Download Ollama Installer:
   - Visit: https://ollama.com/download/windows
   - Run the installer
   - Restart your computer after installation

#### macOS
```bash
# Using Homebrew
brew install ollama

# Or direct download from website
# Visit: https://ollama.com/download/mac
```

#### Linux
```bash
# Download and install
curl https://ollama.ai/install.sh | sh
```

### 5. Pull TinyLlama Model
```bash
# After installing Ollama
ollama pull tinyllama
```

### 6. Additional LangChain Installations
```bash
# Install specific LangChain components
pip install \
    langchain-chroma \
    langchain-openai \
    langchain-anthropic
```

### 7. Set Up Environment Variables
Create a `.env` file in the project root:
```
ANTHROPIC_API_KEY=your_anthropic_api_key_here
```

---

### 8. Install Dependencies
```bash
pip install -r requirements.txt
```

### 9. Prepare Document Database
```bash
python populate_database.py
# Optional: Use --reset flag to clear existing database
python populate_database.py --reset
```

---

## Running the Chatbot

### 1. Run the Chatbot
```bash
streamlit run query_data.py
```

---

## Customization

### Changing Embedding Strategy
- Modify `embedding.py` to implement different embedding generation methods.
- Supports pluggable embedding approaches.

### Language Model Alternatives
- Replace Ollama's TinyLlama with other local or API-based models in `query_data.py`.

---

## Troubleshooting Common Installation Issues

### Memory Constraints
- If you encounter memory-related errors, consider:
  1. Using an even smaller model like `llama2:7b`
  2. Increasing system RAM
  3. Closing other memory-intensive applications

### API Key Issues
- Obtain API keys from:
  - Anthropic: https://www.anthropic.com/
  - OpenAI: https://platform.openai.com/

### Model Download Problems
- Slow internet connection might interrupt model download.
- Use `ollama pull tinyllama` with a stable connection.
- Consider downloading models manually from Ollama's website.

---

## Computational Considerations

- Designed for low-resource environments.
- Adaptive to different computational constraints.
- Supports memory-efficient document retrieval.

---

## Limitations

- Dependent on quality and comprehensiveness of source documents.
- Embedding generation requires Anthropic API access.
- Performance varies with document collection.

---

## Future Roadmap

- [ ] Multi-modal document support
- [ ] Enhanced embedding techniques
- [ ] Improved context understanding
- [ ] More sophisticated error handling

---

## Ethical Considerations

- Intended for informational purposes only.
- Not a substitute for professional medical advice.
- Prioritizes user privacy and data protection.

---

## System Requirements

- **Minimum**:
  - 4 GB RAM
  - 10 GB Disk Space
- **Recommended**:
  - 8 GB RAM
  - SSD Storage
  - Multi-core Processor

---

## Version Compatibility
- Tested with:
  - Python 3.9+
  - Ollama v0.1.x
  - LangChain v0.1.x
  - Streamlit v1.2x.x

---

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---

## License

Distributed under the MIT License. See `LICENSE` for more information.

---

**Note**: Always refer to the official documentation for the most up-to-date installation instructions.
