# Questions during learning LangChain

## LangChain core and community's difference?

* Q1: How may versions of tools?

    Desc:
    ```
    from langchain.tools import GooglePlacesTool

    from langchain_community.tools.google_finance import GoogleFinanceQueryRun

    from langchain_community.utilities.google_finance import GoogleFinanceAPIWrapper§[

    from langchain_core.tools import tool

    ```
    
    REF:

    https://python.langchain.com/docs/contributing/code

* Q2: How many `tool & tools` object in LangChain's ecosystem? How to 

    - langchain.tools

        * There is no `.run()` method in decorator `@tools`

        * There is `.run()` menthos under `from langchain.tools import GooglePlacesTool`

    - langchain_core    ~~~   There is `.run()` method

    - langchain_community

        * There is `.run()` method in `from langchain_community.tools.google_finance import GoogleFinanceQueryRun`

    Answer:

    - [Langchain Opensource code for `core/community/langchain`](https://github.com/langchain-ai/langchain/tree/master/libs)

* Q3: what is `runnable` datatype? Does `agent` is a `runnable` datatype?

    - Source code: `/Users/wanglei/github/langchain/libs/langchain/langchain/agents/openai_tools/base.py`

* Q4: How to `rum custom functions`? what are the  differences between using `RunnableLambda` and `tools`?

* Q5: Does `Retrieval` could be a `tool`?

    Yes, it coule be wrapped as a tool with `from langchain.tools.retriever import create_retriever_tool`


## LangChain's Chain

* Q1: What are the differences between `from langchain.chains import ConversationChain` and `LLMChain`?

* Q2: What are the differences between these two `ChatOpenAI` classes? `from langchain.chat_models import ChatOpenAI' -- `from langchain_openai import ChatOpenAI`


## LangChain's Sourcecode

* Python Libries:

    - Pydantic

        * [【2.1】Pydantic使用方法](https://blog.csdn.net/Chimengmeng/article/details/133648966)

        * What is being used in LangChain:

            - BaseModel

            - Field


## LangChian ReAct:

* [ReAct: Synergizing Reasoning and Acting in Language Models](https://react-lm.github.io/)

  - reasoning (e.g. chain-of-thought prompting): : reasoning traces help the model induce, track, and update action plans as well as handle exceptions

  - acting (e.g. action plan generation): actions allow it to interface with external sources, such as knowledge bases or environments, to gather additional information. 
