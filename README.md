## 🧠 Local llama 3.1 with rersonal memory

This Streamlit application implements a fully local ChatGPT-like experience using Llama 3.1, featuring personalized memory storage for each user. All components, including the language model, embeddings, and vector store, run locally without requiring external API keys.

### Features

- Fully local implementation with no external API dependencies
- Powered by llama 3.1 via Ollama
- Personal memory space for each user
- Local embedding generation using Nomic Embed
- Vector storage with Qdrant

### How to get Started?

1. Install the required Python packages

```bash
pip install uv
uv --native-tls sync
```

2. Install and start [Qdrant](https://qdrant.tech/documentation/guides/installation/) vector database locally

```bash
docker pull qdrant/qdrant
docker run -d -p 6333:6333 qdrant/qdrant
```

4. Install [Ollama](https://ollama.com/download) and pull [llama 3.1](https://ollama.com/library/llama3.1) and [embeddings](https://ollama.com/library/nomic-embed-text)

```bash
ollama pull llama3.1:latest
ollama pull nomic-ai/nomic-embed:latest
```

5. Run ollama server

```bash
ollama serve
```

6. Run the Streamlit App

```bash
uv --native-tls run streamlit run local_llama_memory.py
```

## Acknowledgements

- running with [litellm](https://github.com/BerriAI/litellm)
- memory layer for AI agents and assistsants [mem0](https://github.com/mem0ai/mem0)
- UI powered by [Streamlit](https://github.com/streamlit/streamlit)
- LLM powered by [Ollama](https://github.com/ollama/ollama)
- Model [llama3.1](https://ollama.com/library/llama3.1)
- Embeddings [nomic-embed](https://ollama.com/library/nomic-embed-text)
- vector similarity search engine and vector database [quadrant](https://github.com/qdrant/qdrant)
