# Sample Search Filter Assistant

A Retrieval-Augmented Generation (RAG) system that helps users understand and effectively use sample search filters through natural language queries.

## Overview

This project implements a RAG-based chatbot designed to answer questions about sample search filtering capabilities. Users can ask questions in plain English about how to configure, apply, and troubleshoot filters, and receive accurate, contextual responses based on the sample search documentation and best practices.

## Features

- **Natural Language Queries**: Ask questions about filters in conversational language
- **Contextual Responses**: Get accurate answers based on Deep Analytics documentation
- **Filter Examples**: Receive practical examples and code snippets
- **Interactive Q&A**: Engage in follow-up questions for deeper understanding
- **Search Functionality**: Find specific filter types and use cases quickly

## Use Cases

- Learning how to create complex filter expressions
- Understanding filter syntax and operators
- Troubleshooting filter performance issues
- Discovering advanced filtering techniques
- Getting examples for specific data scenarios

## Getting Started

### Prerequisites

```bash
python >= 3.8
pip install -r requirements.txt
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/sample-search-rag.git
cd sample-search-rag
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

4. Initialize the vector database:
```bash
python setup_database.py
```

### Usage

Start the application:
```bash
python app.py
```

Then interact with the system by asking questions like:
- "How do I filter search results by date range?"
- "What's the syntax for combining multiple search filter conditions?"
- "How can I filter null values in sample searches?"
- "Show me examples of regex search filters"

## Example Queries

**Basic Filtering:**
```
Q: How do I create a simple text search filter?
A: To create a text filter in sample search, use the 'contains' operator...
```

**Advanced Filtering:**
```
Q: How do I combine date and category search filters?
A: You can combine search filters using logical operators (AND, OR)...
```

**Performance Optimization:**
```
Q: My search filters are running slowly, how can I optimize them?
A: Here are several strategies to improve search filter performance...
```

## Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   User Query    │───▶│   RAG System     │───▶│   Response      │
└─────────────────┘    └──────────────────┘    └─────────────────┘
                              │
                              ▼
                       ┌──────────────────┐
                       │  Vector Database │
                       │  (Documentation) │
                       └──────────────────┘
```

The system consists of:
- **Query Processing**: Natural language understanding and intent recognition
- **Retrieval System**: Vector-based search through sample search filter documentation
- **Generation Component**: Context-aware response generation
- **Knowledge Base**: Embedded sample search filter documentation and examples

## Configuration

Key configuration options in `.env`:

```env
# Vector Database
VECTOR_DB_PATH=./data/vectordb
EMBEDDING_MODEL=sentence-transformers/all-MiniLM-L6-v2

# LLM Configuration
LLM_MODEL=gpt-3.5-turbo
MAX_TOKENS=500
TEMPERATURE=0.1

# Retrieval Settings
TOP_K_RESULTS=5
SIMILARITY_THRESHOLD=0.7
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Adding New Documentation

To add new filter documentation:

1. Place new documents in `./data/docs/`
2. Run the ingestion script: `python ingest_docs.py`
3. Test the new knowledge with sample queries

## Roadmap

- [ ] Support for visual filter builder integration
- [ ] Multi-language query support
- [ ] Advanced analytics on common questions
- [ ] Integration with sample search API for live examples
- [ ] Mobile-responsive web interface

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For questions and support:
- Create an issue in this repository
- Check the [documentation](./docs/)
- Contact the development team

## Acknowledgments

- Sample search team for comprehensive documentation
- Open source RAG frameworks and libraries
- Community contributors and testers
