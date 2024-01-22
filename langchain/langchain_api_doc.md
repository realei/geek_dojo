# Questions in LangChain Official Documents

## [Agents Quickstart](https://python.langchain.com/docs/modules/agents/quick_start)

* `tools = [search, retriever_tool]` -> `tools` + `Prompts`  -> `agent = create_openai_functions_agent(llm, tools, prompt)`

    1. Q1: how the `default Prompts` route between different `tools`(search, retriever_tool)? 

        * the prompt is: [hwchase17/openai-functions-agent](https://smith.langchain.com/hub/hwchase17/openai-functions-agent?organizationId=4590a671-97e8-51fe-b2cd-08c5f96b45b6)
