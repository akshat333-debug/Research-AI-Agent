# Research AI Agent

Small LangChain tool-calling agent that answers a research query using web search and Wikipedia, then returns a structured, Pydantic-validated result (topic, summary, sources, tools used) and can save it to a text file.

Built as a learning project for the LangChain agent/tool-calling stack.

## Stack

- LangChain `create_tool_calling_agent` + `AgentExecutor`
- Anthropic Claude (swappable with OpenAI via `langchain-openai`)
- Tools: DuckDuckGo search, Wikipedia, save-to-file
- `PydanticOutputParser` for structured output

## Run

```bash
pip install -r requirements.txt
cp sample.env .env   # add ANTHROPIC_API_KEY (or OPENAI_API_KEY)
python main.py
```

Output is appended to `research_output.txt` with a timestamp.
