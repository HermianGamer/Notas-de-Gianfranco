  
When using any LLM API, it's important to keep track of how many tokens you're consuming. Most APIs provide metadata about token usage in their responses, which can help you to monitor your consumption – and to try to avoid hitting rate limits.

The [`GenerateContentResponse`](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentResponse) object returned by the Gemini API includes a [`usage_metadata`](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentResponseDict.usage_metadata) property. The `usage_metadata` in turn has both:

- a `prompt_token_count` property, showing the number of tokens in the _prompt_ that was sent to the model; and
- a `candidates_token_count` property, showing the number of tokens in the model's _response_.

Let's make sure we can keep track of our usage, printing it along with the response if desired.