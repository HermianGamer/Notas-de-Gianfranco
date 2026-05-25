

- client = genai.Client(): Client object
- response = client.models.generate_content(model, contents): GenerateContentResponse object
- config=types.GenerateContentConfig(): configuration for the model

---
GenerateContentResponse object properties:
- [.text](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentResponse.text): string of the LLMs response
- .usage_metadata: metadata of the response
- [.function_calls](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentResponse.function_calls): functions called by the LLM, returns a list of [`FunctionCall`](https://googleapis.github.io/python-genai/genai.html#genai.types.FunctionCall) objects