# OpenAi_LLM_Langchain

```
from secret_key import openapi_key
import os
os.environ['OPENAI_API_KEY'] =openapi_key `
``


```from langchain.llms import OpenAI

llm = OpenAI(temperature=0.6)
name = llm("I want to open a restaurant for Indian food. Suggest a fancy name for this.")
print(name)
```

```
from langchain.prompts import PromptTemplate

prompt_template_name = PromptTemplate(
    input_variable = ['cuisine'],
    template = "I want to open a restaurant for {cuisine} food. Suggest a fancy name for this."
)
```
```
from lanchain.chains import LLMChain

chain == LLMChain(llm=llm, prompt=prompt_template_name)
chain.run("Mexican`")
```
