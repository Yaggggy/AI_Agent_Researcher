# AI Research Assistant

An intelligent research assistant powered by Claude AI that helps generate comprehensive research papers by combining information from multiple sources.

## Features

- 🤖 **AI-Powered Research**: Utilizes Claude 3 Sonnet for advanced natural language processing
- 🔍 **Multi-Source Research**: Combines information from:
  - Web searches (DuckDuckGo)
  - Wikipedia articles
  - Custom knowledge base
- 📝 **Structured Output**: Generates well-organized research results including:
  - Topic overview
  - Detailed summary
  - Source citations
  - Tools used in research
- 💾 **Automatic Saving**: Saves research outputs to text files with timestamps
- 🎯 **Interactive**: Responds to user queries in real-time

## How It Works

### Architecture

1. **Input Processing**
   - Takes user research queries through command-line interface
   - Processes natural language questions about any research topic

2. **Research Tools**
   - `search_tool`: Performs web searches using DuckDuckGo
   - `wiki_tool`: Retrieves relevant Wikipedia articles
   - `save_tool`: Saves research outputs to files

3. **AI Processing**
   - Uses LangChain framework for AI agent creation
   - Leverages Claude 3 Sonnet model for:
     - Understanding research queries
     - Synthesizing information
     - Generating structured responses

4. **Output Structure**
   - Returns a structured response containing:
     ```python
     {
         "topic": "Research topic",
         "summary": "Comprehensive research summary",
         "sources": ["Source1", "Source2", ...],
         "tools_used": ["Tool1", "Tool2", ...]
     }
     ```

## Requirements

- Python 3.x
- Anthropic API key
- Required packages:
  - langchain
  - langchain-anthropic
  - langchain-community
  - python-dotenv
  - pydantic
  - wikipedia
  - duckduckgo-search

## Setup

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/Mac
   .venv\Scripts\activate     # Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Create a `.env` file with your Anthropic API key:
   ```
   ANTHROPIC_API_KEY=your_api_key_here
   ```

## Usage

Run the main script:
```bash
python main.py
```

When prompted, enter your research query. For example:
- "Explain quantum computing"
- "Research the history of artificial intelligence"
- "Analyze the impact of social media on society"

The assistant will gather information, generate a structured research response, and save the results to a file.
