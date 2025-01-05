# Getting Started with LangChain in a Python Dev Container using VS Code Remote Explorer

This guide will help you set up a development environment for LangChain using a Python-based development container and VS Code Remote Explorer.

---

## Prerequisites

1. **Install Poetry**: Poetry is a dependency management tool for Python. Install it using the following command:

   ```bash
   curl -sSL https://install.python-poetry.org | python3 -
   ```

   For detailed installation instructions, refer to the [official Poetry documentation](https://python-poetry.org/docs/#installing-with-the-official-installer).

2. **OpenAI API Key**: Obtain an API key from [OpenAI](https://platform.openai.com/api-keys).

3. **VS Code**: Ensure you have Visual Studio Code installed with the Remote Explorer extension.

---

## Setting Up LangChain

### Step 1: Install LangChain

1. Initialize a new Poetry project or navigate to an existing Poetry project directory.
2. Install LangChain and related dependencies using Poetry:

   ```bash
   poetry add langchain-core
   poetry add langchain-community
   poetry add langchain-openai
   ```

3. Install Python dotenv for managing environment variables:

   ```bash
   poetry add python-dotenv
   ```

### Step 2: Create a Python File

1. Create a `main.py` file in your project directory.
2. Add your Python code to this file.

---

## Core LangChain Concepts and Imports

Here are some of the core LangChain concepts and their corresponding imports:

```python
from langchain_core.messages import AIMessage, HumanMessage, ToolMessage, BaseMessage
from langchain_core.tools import tool
from langchain_core.prompts import ChatPromptTemplate
from langchain_core.runnables import Runnable, RunnableConfig
from langchain_core.utils.function_calling import convert_to_openai_function
from langgraph.prebuilt import ToolNode
from langgraph.graph import END, StateGraph, START
from langgraph.prebuilt import tools_condition
from langgraph.graph.message import AnyMessage, add_messages
from langgraph.graph import MessagesState, StateGraph, START
from langchain.agents import Tool
from langchain.utilities import GoogleSerperAPIWrapper
from langchain.chains import APIChain
from langchain.vectorstores import FAISS
from langchain.embeddings import OpenAIEmbeddings
from langchain.callbacks.base import AsyncCallbackHandler
from langchain.callbacks.manager import AsyncCallbackManager
from langchain.chains.conversation.memory import ConversationBufferMemory
from langchain.memory import ConversationBufferWindowMemory
from langchain.text_splitter import CharacterTextSplitter
from langchain.docstore.document import Document
from langchain.vectorstores import FAISS
from langchain.memory import ConversationBufferMemory
```

---

## Useful Resources

- **LangChain Documentation**: [LangChain Documentation](https://python.langchain.com/v0.1/docs/get_started/installation/)
- **Poetry Documentation**: [Poetry Documentation](https://python-poetry.org/docs/)
- **OpenAI API**: [OpenAI API](https://platform.openai.com/api-keys)

---

With this setup, you are ready to start developing with LangChain in a Python-based development container using VS Code Remote Explorer. Happy coding!
