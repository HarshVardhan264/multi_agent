# ResearchMind - Multi-Agent AI Research System

A sophisticated multi-agent AI system that collaborates to produce comprehensive research reports on any topic. Four specialized agents work together to search, scrape, analyze, and critique research content.

## 🎯 Features

- **Search Agent**: Finds recent, reliable, and detailed information using web search
- **Reader Agent**: Scrapes and processes content from URLs for deeper analysis
- **Writer Agent**: Compiles research into structured, professional reports
- **Critic Agent**: Reviews and provides constructive feedback on generated reports

## 🏗️ Project Structure

```
multi_agent/
├── agents.py          # Agent definitions and LLM chains
├── tools.py           # Web search and URL scraping tools
├── pipeline.py        # Research pipeline orchestration (CLI)
├── app.py             # Streamlit web application interface
├── requirements.txt   # Python dependencies
└── README.md          # This file
```

## 📋 Prerequisites

- Python 3.8+
- Mistral AI API key
- Tavily API key

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd multi_agent
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   # On Windows
   .venv\Scripts\activate
   # On macOS/Linux
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   Create a `.env` file in the project root:
   ```
   MISTRAL_API_KEY=your_mistral_api_key
   TAVILY_API_KEY=your_tavily_api_key
   ```

## 📖 Usage

### CLI Mode (Command Line)

Run the research pipeline from the terminal:

```bash
python pipeline.py
```

Enter your research topic when prompted, and the system will:
1. Search for relevant information
2. Scrape detailed content from top sources
3. Generate a comprehensive report
4. Provide critical feedback

### Web UI Mode (Streamlit)

Launch the interactive web interface:

```bash
streamlit run app.py
```

Then navigate to `http://localhost:8501` in your browser to access the ResearchMind interface with:
- Beautiful, modern UI
- Real-time pipeline visualization
- Interactive result panels
- Professional report display

## 🔧 Components

### `agents.py`
- **build_search_agent()**: Creates an agent with web search capability
- **build_reader_agent()**: Creates an agent with URL scraping capability
- **writer_chain**: Generates structured research reports
- **critic_chain**: Evaluates and provides feedback on reports

### `tools.py`
- **web_search(query)**: Searches the web and returns results with URLs and snippets
- **scrape_url(url)**: Fetches and cleans text content from a given URL

### `pipeline.py`
- **run_research_pipeline(topic)**: Orchestrates the complete research workflow

## 📦 Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| langchain | 0.1.11 | LLM framework |
| langchain-core | 0.1.33 | Core LangChain components |
| langchain-community | 0.0.29 | Community integrations |
| langchain-mistralai | 0.0.13 | Mistral AI integration |
| mistralai | 0.0.14 | Mistral API client |
| tavily-python | 0.3.3 | Web search API |
| beautifulsoup4 | 4.12.2 | HTML parsing |
| requests | 2.31.0 | HTTP library |
| lxml | 4.9.3 | XML processing |
| python-dotenv | 1.0.0 | Environment variables |
| streamlit | 1.31.1 | Web UI framework |
| rich | 13.7.0 | Terminal formatting |

## 🔐 API Keys

### Mistral AI
1. Sign up at [Mistral AI](https://mistral.ai/)
2. Create an API key from your dashboard
3. Add to `.env`: `MISTRAL_API_KEY=your_key`

### Tavily
1. Sign up at [Tavily](https://tavily.com/)
2. Get your API key
3. Add to `.env`: `TAVILY_API_KEY=your_key`

## 📊 Workflow

```
User Input (Topic)
    ↓
[Search Agent] → Web Search Results
    ↓
[Reader Agent] → Scraped Content
    ↓
[Writer Chain] → Research Report
    ↓
[Critic Chain] → Feedback & Score
    ↓
Final Output
```

## 🎨 UI Highlights

The Streamlit interface features:
- Custom dark theme with orange accents
- Step-by-step pipeline visualization
- Real-time status updates
- Professional typography
- Responsive mobile design
- Detailed result panels

## 🛠️ Troubleshooting

**Invalid API Key**
- Verify your API keys in `.env`
- Ensure keys have appropriate permissions

**Web Scraping Failures**
- Some websites may block scraping
- Check internet connection
- Try alternative URLs

**LLM Response Issues**
- Check Mistral API status
- Verify model availability (`mistral-large-latest`)
- Review API rate limits

## 📝 Example Output

The system generates reports with:
- Clear introduction
- Minimum 3 key findings with explanations
- Structured conclusions
- Source citations
- Critical evaluation score
- Strengths and improvement areas

## 🔄 Future Enhancements

- Multi-language support
- Document export (PDF, DOCX)
- Advanced caching system
- Batch research processing
- Custom report templates
- Integration with more LLM providers

---
**Built with** ❤️ using LangChain, Mistral AI, and Streamlit
