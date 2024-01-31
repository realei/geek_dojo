# Questions in LangChain Official Documents

## [Agents Quickstart](https://python.langchain.com/docs/modules/agents/quick_start)

* `tools = [search, retriever_tool]` -> `tools` + `Prompts`  -> `agent = create_openai_functions_agent(llm, tools, prompt)`

    1. Q1: how the `default Prompts` route between different `tools`(search, retriever_tool)? 

        * the prompt is: [hwchase17/openai-functions-agent](https://smith.langchain.com/hub/hwchase17/openai-functions-agent?organizationId=4590a671-97e8-51fe-b2cd-08c5f96b45b6)

    2. Q2: what is "OpanAI Functions"? What is `open-source model that has been finetuned for function calling and exposes the same functions parameters as OpenAI`"
        
        * Questions Ref: [Agent Types](https://python.langchain.com/docs/modules/agents/agent_types) 

        * [LangChain之Chain为何物](https://zhuanlan.zhihu.com/p/634313377)

            - PromptTemplate

            - 模型（LLM或ChatModel）

            - OutputParser（输出解析器，可选）

        * [一文学会 OpenAI 的函数调用功能 Function Calling](https://zhuanlan.zhihu.com/p/641239259)
            
            - 函数 （Function Calling) 描述 --- 这对于 llm 非常重要， llm 用函数描述来识别函数 （Function Calling) 是否适合回答用户的请求。
            
            - `Chains` -> `Tools` -> `Agent`

## LangChain's Chains

* Chains

    - LCEL Chains (LangChain Expression Language --- LCEL)

    - Legacy Chains

## LangChain's example:  [Tool use](https://python.langchain.com/docs/use_cases/tool_use/)

    * [Create a custom tool](https://python.langchain.com/docs/modules/agents/tools/)    

## LangChain Opensource Contributor

* [Contgributing](https://python.langchain.com/docs/contributing/)
