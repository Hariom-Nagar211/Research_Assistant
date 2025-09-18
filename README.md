# 🔍 AI Research Assistant

An intelligent research assistant powered by LangChain, LangGraph, and modern AI technologies. This application conducts comprehensive research on any topic by orchestrating web searches, content analysis, and report generation through a structured workflow.

## ✨ Features

- **🤖 AI-Powered Research**: Leverages Groq's fast LLM inference for intelligent analysis
- **🔍 Advanced Web Search**: Uses Tavily's search API for comprehensive information gathering  
- **📊 Structured Workflow**: Multi-step process with planning, searching, analysis, and reporting
- **📄 Professional Reports**: Generates detailed research reports with key findings and recommendations
- **💾 Research History**: Maintains a history of all research queries and results
- **🔐 Secure API Management**: Environment-based API key configuration
- **🎨 Modern UI**: Clean, responsive Streamlit interface

## 🏗️ Architecture

The application uses a **LangGraph workflow** with four main stages:

1. **📋 Research Planner**: Analyzes queries and creates research strategies
2. **🔍 Web Searcher**: Performs advanced web searches using Tavily
3. **📊 Content Analyzer**: Processes and analyzes search results
4. **📄 Report Generator**: Creates comprehensive research reports

## 🛠️ Technology Stack

- **Frontend**: Streamlit
- **AI Framework**: LangChain + LangGraph
- **LLM Provider**: Groq (llama-3.3-70b-versatile)
- **Search Engine**: Tavily Search API
- **Language**: Python 3.8+
- **State Management**: LangGraph MemorySaver

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Groq API key ([Get one here](https://console.groq.com))
- Tavily API key ([Get one here](https://tavily.com))

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Research_Assistant
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   
   Create a `.env` file in the project root:
   ```env
   GROQ_API_KEY=gsk_your_actual_groq_api_key_here
   TAVILY_API_KEY=tvly-your_actual_tavily_api_key_here
   ```

5. **Run the application**
   ```bash
   streamlit run app.py
   ```

6. **Open your browser** to `http://localhost:8501`

## 📋 Usage

1. **Enter your research query** in the text area
2. **Click "Start Research"** to begin the automated research process
3. **View the generated report** with:
   - Executive Summary
   - Key Findings
   - Detailed Analysis
   - Source References
   - Recommendations
4. **Access research history** from previous queries

### Example Queries

- "Latest developments in artificial intelligence and machine learning"
- "Climate change impact on renewable energy adoption"
- "Cybersecurity trends and best practices for 2024"
- "Market analysis of electric vehicle industry"

## 🔧 Configuration

### API Keys

The application requires two API keys:

- **Groq API Key**: For LLM inference (format: `gsk_...`)
- **Tavily API Key**: For web search (format: `tvly-...`)

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `GROQ_API_KEY` | Groq API key for LLM access | Yes |
| `TAVILY_API_KEY` | Tavily API key for web search | Yes |

### Deployment

For deployment on platforms like Streamlit Cloud, Heroku, or Railway:

1. Set the environment variables in your platform's settings
2. Ensure all dependencies are listed in `requirements.txt`
3. The application will automatically validate API keys on startup

## 📁 Project Structure

```
Research_Assistant/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── .env                  # Environment variables (not in git)
├── .gitignore           # Git ignore rules
├── README.md            # This file
└── .venv/               # Virtual environment (not in git)
```

## 🔍 How It Works

### Workflow Details

1. **Planning Phase**: The AI analyzes your query and creates a research strategy
2. **Search Phase**: Performs targeted web searches using Tavily's advanced search
3. **Analysis Phase**: Processes and extracts key insights from search results
4. **Report Phase**: Generates a structured, professional research report

### Key Components

- **`ResearchAssistantAgent`**: Main orchestrator class
- **`AgentState`**: Workflow state management
- **`analyze_research_content`**: Content analysis tool
- **API validation**: Ensures keys are valid before processing

## 🛡️ Security

- API keys are stored in environment variables
- No sensitive data is logged or stored permanently
- All external API calls are properly authenticated
- Input validation prevents malicious queries

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Troubleshooting

### Common Issues

**API Key Errors**
- Ensure your API keys are correctly formatted
- Check that environment variables are properly set
- Verify your API keys are active and have sufficient credits

**Installation Issues**
- Make sure you're using Python 3.8+
- Try upgrading pip: `pip install --upgrade pip`
- Use a fresh virtual environment

**Search Failures**
- Check your internet connection
- Verify Tavily API key has search permissions
- Try simpler, more specific queries

### Getting Help

- Check the [Issues](../../issues) page for common problems
- Create a new issue with detailed error information
- Include your Python version and operating system

## 🙏 Acknowledgments

- [LangChain](https://langchain.com) for the AI framework
- [LangGraph](https://langgraph.com) for workflow orchestration
- [Groq](https://groq.com) for fast LLM inference
- [Tavily](https://tavily.com) for advanced web search
- [Streamlit](https://streamlit.io) for the web interface

---

**Made with ❤️ for researchers, analysts, and curious minds everywhere!**
