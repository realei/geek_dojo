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

## LangChain's Sourcecode

* Python Libries:

    - Pydantic

        * [【2.1】Pydantic使用方法](https://blog.csdn.net/Chimengmeng/article/details/133648966)

        * What is being used in LangChain:

            - BaseModel

            - Field
