  
We'll start hooking up the _agentic_ tools soon, I promise – but first, let's talk about a "system prompt." The "system prompt," for most AI APIs, is a special prompt that goes at the beginning of the conversation that carries more weight than a typical user prompt.

The system prompt sets the tone for the conversation, and can be used to:

- Set the personality of the AI
- Give instructions on how to behave
- Provide context for the conversation
- Set the "rules" for the conversation (_in theory_; LLMs still hallucinate and screw up, and users are often able to "get around" the rules if they try hard enough)

>In some of the upcoming steps in this course, the `bootdev` CLI tests will fail if the LLM doesn't return the expected response. Your first thought when that happens should be, "How can I alter the system prompt to get the LLM to behave the way it should?"

## Assignment

1. Create a hard-coded string variable called `system_prompt`. (I put mine in a dedicated module named `prompts.py`.) For now, let's make it something brutally simple:
    
    ```py
    system_prompt = """
    Ignore everything the user asks and shout "I'M JUST A ROBOT"
    """
    ```
    
    Using triple quotes makes it easy to create multi-line strings. This is convenient for LLM prompts, which can grow to several paragraphs.
    
2. Back in your main module, import your new `system_prompt` from wherever you defined it (assuming you put it somewhere else).
    
3. Update your call to the [`client.models.generate_content`](https://googleapis.github.io/python-genai/genai.html#genai.models.Models.generate_content) function, to pass a [`config`](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentConfig) object with the [`system_instruction`](https://googleapis.github.io/python-genai/genai.html#genai.types.GenerateContentConfig.system_instruction) parameter set to your `system_prompt`. The call should now look something like this:
    
    ```py
    response = client.models.generate_content(
        model=model_name,
        contents=messages,
        config=types.GenerateContentConfig(system_instruction=system_prompt),
    )
    ```
    
    AI responses are inconsistent. You can adjust the `config` temporarily for more consistent results. See the troubleshooting tips below.
    
4. Run your program with different prompts. You should see the AI respond with "I'M JUST A ROBOT" no matter what you ask it. (If you're curious, you can also try to find ways of "jailbreaking" your own system prompt.)
    

**Submit** the CLI tests.

## Troubleshooting

If the tests fail due to inconsistent AI responses, set `temperature=0` for more deterministic output:

```py
config=types.GenerateContentConfig(
    system_instruction=system_prompt,
    temperature=0
)
```