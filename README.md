# Agentic AI Research Assistant 🔬

> A production-ready research assistant agent built with LangChain that autonomously researches topics, gathers information from multiple sources, and generates comprehensive reports.

## Overview

This project demonstrates core concepts of **Agentic AI** including:
- **Agent Architecture**: Planning, reasoning, and decision-making
- **Tool Use**: Integrating external APIs and functions
- **Memory Systems**: Context management across interactions
- **Multi-step Workflows**: Complex task decomposition and execution

## Features ✨

✅ Autonomous research across multiple information sources
✅ Smart question decomposition and sub-research
✅ Intelligent source evaluation and synthesis
✅ Long-term memory and context management
✅ Configurable research depth and breadth
✅ Structured report generation

## Architecture

```
User Query
    ↓
[Planner Agent] - Breaks down research into sub-questions
    ↓
[Researcher Agent] - Gathers information from multiple sources
    ↓
[Analyzer Agent] - Evaluates and synthesizes findings
    ↓
[Writer Agent] - Generates comprehensive report
    ↓
Structured Report Output
```

## Getting Started

### Prerequisites
- Python 3.9+
- OpenAI API key (or other supported LLM)
- Internet connection for web search

### Installation

1. Clone this repository:
```bash
git clone https://github.com/Ashish1896/agentic-ai-research-assistant.git
cd agentic-ai-research-assistant
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env and add your API keys
```

### Quick Start

```python
from research_assistant import ResearchAgent

# Initialize the agent
agent = ResearchAgent()

# Run research
result = agent.research("Latest developments in quantum computing")

# Get structured report
print(result["report"])
```

## Project Structure

```
.
├── research_assistant/
│   ├── __init__.py
│   ├── agent.py          # Main agent logic
│   ├── tools.py          # Tool definitions
│   ├── prompts.py        # System prompts
│   └── utils.py          # Utility functions
├── examples/
│   └── basic_research.py
├── tests/
│   └── test_agent.py
├── requirements.txt
├── .env.example
├── .gitignore
└── README.md
```

## Usage Examples

### Basic Research

```python
from research_assistant import ResearchAgent

agent = ResearchAgent(
    model="gpt-4",
    research_depth="comprehensive",
    source_limit=10
)

result = agent.research("AI agents in 2026")
print(result["report"])
print(result["sources"])
```

### Multi-topic Research

```python
topics = [
    "LangChain framework",
    "AutoGPT capabilities",
    "Multi-agent systems"
]

for topic in topics:
    result = agent.research(topic)
    # Process results...
```

## Key Technologies

- **LangChain**: Agent orchestration and workflow
- **OpenAI GPT-4**: Language understanding and generation
- **Tavily Search API**: Information retrieval
- **Python**: Core implementation language

## Contributing

Contributions are welcome! Here's how to contribute:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

## Roadmap 🚀

- [ ] Multi-agent collaboration
- [ ] Real-time research streaming
- [ ] Custom knowledge base integration
- [ ] Advanced reasoning with chain-of-thought
- [ ] API endpoint for integration
- [ ] Web interface

## Learning Resources

- [LangChain Documentation](https://docs.langchain.com)
- [OpenAI API Reference](https://platform.openai.com/docs)
- [Agentic AI Design Patterns](https://www.anthropic.com/research)

## Author

**Ashish Kumar Sahoo**
- B.Tech CSE (Final Year) at ITER, SOA University
- Full-stack developer passionate about agentic AI
- Open source contributor

## License

MIT License - see LICENSE file for details

## Disclaimer

This project is for educational and research purposes. Ensure compliance with API terms of service and rate limits.
