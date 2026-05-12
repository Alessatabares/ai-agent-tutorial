# AI Agent Tutorial

This project is a beginner-friendly LangChain agent that can research a user query, use external tools, return a structured response, and save research output to a text file.

## Project Goal

The goal of this project is to understand the architecture of a basic AI agent from scratch.

The agent can:

- Receive a research question from the terminal
- Use a language model
- Use external tools such as Wikipedia, web search, and file saving
- Return a structured response using a Pydantic model
- Save research output into `research_output.txt`

## Workflow Architecture

```text
User
 ↓
Terminal input
 ↓
main.py
 ↓
AgentExecutor
 ↓
LangChain Agent
 ├── LLM
 ├── Prompt
 ├── Tools
 │   ├── search_tool
 │   ├── wiki_tool
 │   └── save_tool
 └── Agent Scratchpad
 ↓
Raw agent response
 ↓
PydanticOutputParser
 ↓
Structured ResearchResponse

